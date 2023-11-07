# Homework: Module 2 - Exploratory data analysis

The work of any data scientist is closely related to search and research, so it is very important to learn how to find the information you need and adapt it to your needs.

## Part One: Getting to Know Pandas.

Read the data using the read_html method from the table "Birth rate in the regions of Ukraine (1950—2019)" link (https://uk.wikipedia.org/wiki/%D0%9D%D0%B0%D1%81%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8F_%D0%A3%D0%BA%D1%80%D0%B0%D1%97%D0%BD%D0%B8)

It is necessary to perform:

* Show head of the table
* Define the number of rows and columns in the dataframe
* In the table, replace the value "—" with the value NaN
* Define the types of all columns
* Replace non-numeric column types with numeric ones
* Calculate the percentage of blanks in each column
* Delete the countrywide data from the table, the last row of the table
* Replace missing data in columns with the average values of those columns
* Get a list of regions where the birth rate in 2019 was higher than the average for Ukraine
* Which region had the highest birth rate in 2014?
* Construct a bar chart of birth rates by region in 2019

The work is submitted as a Jupyter file Hw2.1.ipynb

## Part Two: File Analysis

Analyze the 2017_jun_final.csv file (https://drive.google.com/file/d/1JMYqXipZpz9Y5-vyxvLEO2Y1sRBxqu-U/view). The file contains the results of the developer survey in June 2017.

It is necessary to perform:

* Read the file 2017_jun_final.csv
* Read head of the resulting table
* Determine the size of the table
* Define the types of all columns
* Calculate the percentage of blanks in each column
* Remove all blank columns except the "Programming Language" column
* Count again what proportion of gaps are in each column and make sure that only the column "Language.programming" remains
* Delete all rows in the source table
* Define the new size of the table
* Create a new python_data table, which will contain only rows with specialists who specified the Python programming language
* Determine the size of the python_data table
* Group by the "Position" column
* Create a new DataFrame where for the data grouped by the Position column, aggregate the data and find the min and max values in the Salary.monthly column
* Create a function fill_avg_salary that will return the average salary for a month. Use it to create a new column "avg"
* Create descriptive statistics for the new column.
* Save the resulting table in a CSV file

The work is submitted as a Jupyter file Hw2.2.ipynb

## Part Three: Dataset Analysis c Kaggle.com

In this part of the homework, we will delve further into the pandas library and look at more advanced features.

For this exercise, we use data from the Top 50 best-selling books on Amazon over 11 years (from 2009 to 2019). The dataset is publicly available on Kaggle.com (https://www.kaggle.com/datasets/sootersaalu/amazon-top-50-bestselling-books-2009-2019). Download the csv file from the link and move it to the same directory as your work folder (for convenience). After that, go to the task.

To complete this part of the homework, you will not only need to write the code, but also answer the accompanying questions. Where you see the answer in bold: you will need to insert the question into the file and the answer to it.

Example:

What library is used to work with dataframes in python? Answer: pandas

It is necessary to perform:

* Read the csv file (use the read_csv function)
* Output the first five lines (the head function is used)
* Display the dimensions of the dataset (use the shape attribute)
* Answer: How many books does the dataset store?

7 variables (columns) are available for each of the books. Let's take a closer look at them:

Name - the name of the book

Author - the author

User Rating - rating (on a 5-point scale)

Reviews - number of reviews

Price - price (in dollars as of 2020)

Year - the year when the book entered the Top-50 rating

Genre - a genre

To simplify further work, let's tweak the variable names a little. As you can see, here all the names start with a capital letter, and one even contains a space. This is highly undesirable and can be quite inconvenient. Let's change the case to lowercase, and replace the space with an underscore (snake_style). And now we will study a useful data frame attribute: columns (you can simply assign a list of new names to this attribute)

df.columns = ['name', 'author', 'user_rating', 'reviews', 'price', 'year', 'genre']

### Primary data analysis

* Check if all rows have enough data: output the number of gaps (na) in each of the columns
* Answer: Are there gaps in any variables? (Yes No)
* Check what are the unique values in the genre column
* Answer: What are the unique genres?
* Now look at the price distribution: make a histogram
* Determine what our maximum, minimum, average, median price is
* Answer: Maximum price?
* Answer: Minimum price?
* Answer: Average price?
* Answer: Median price?

### Search and sort data

* Answer: What is the highest rating in the dataset?
* Answer: How many books have this rating?
* Answer: Which book has the most reviews?
* Answer: Of the books that made it to the Top 50 in 2015, which book is the most expensive?
* Answer: How many Fiction books were in the Top 50 in 2010?
* Answer: How many books rated 4.9 were ranked in 2010 and 2011?
* Sort by increasing price all the books that made the ranking in 2015 and cost less than $8
* Answer: Which book is last in the sorted list?

### Aggregation of data and connection of tables

The last section of this homework includes more advanced features. But don't worry, pandas makes all operations simple and clear.

* First, let's look at the maximum and minimum prices for each of the genres. Do not take all the columns, select only the ones you need
* Answer: The maximum price for the genre Fiction
* Answer: Minimum price for Fiction genre
* Answer: Maximum price for Non Fiction genre
* Answer: Minimum price for Non Fiction genre
* Now create a new dataframe that will hold the number of books for each author. Do not take all the columns, select only the ones you need
* Answer: What is the size of the table? Answer:
* Answer: Which author has the most books? Answer:
* Answer: How many books by this author? Answer:
* Now create a second dataframe that will hold the average rating for each author (use the groupby and agg functions, use mean to calculate the average). Do not take all the columns, select only the ones you need
* Answer: Which author has the lowest average rating? Answer:
* Answer: What is the average rating of this author? Answer:
* Concatenate the last two dataframes so that the number of books and the average rating are visible for each author (Use the concat function with axis=1). Save the result to a variable
* Sort the dataframe by increasing number of books and increasing rating (use the sort_values function)
* Answer: Which author is first on the list?

The work is submitted as a Jupyter file Hw2.3.ipynb

### Visualization

For each of the previous tasks:

* Hw2.1.ipynb
* Hw2.2.ipynb
* Hw2.3.ipynb

add 3 to 5 graphs of different types of functions of your choice. Designate the graphs so that each graph in your homework is different and not similar to the others. Both matplotlib and seaborn can be used.

Do not forget to add the directive %matplotlib inline to the Jupyter file so that the graphs are built inside the document.