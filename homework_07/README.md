# Homework: Module 7 - Recommender systems

This time we are going to learn how recommender systems work. We invite you to familiarize yourself with the surprise library (https://surpriselib.com/), which is essentially an add-on to the familiar scikit-learn library for training recommender system models.

Take the movielens dataset (https://surprise.readthedocs.io/en/stable/dataset.html) and build a matrix factorization model. In this library, it is named SVD. Choose the best parameters using cross-validation, also experiment with other calculation algorithms (SVD++, NMF) (https://surprise.readthedocs.io/en/stable/prediction_algorithms_package.html) and choose the one that will be optimal.

You will find hints on exactly how to build this model in the documentation for this library.

### Additional task with an asterisk

For a deeper understanding of the algorithm, we suggest implementing a collaborative filtering algorithm from scratch. For this we can use еру homework from the 3rd module. If we modify the loss function and the calculation of the gradients, we can build a matrix factorization algorithm.

Here (https://colab.research.google.com/drive/1biZdo4pc_Kkm-JvZsuadqDVphfUu1sGk?usp=sharing) are the formulas and the dataset for download. Here are links to movie titles (https://drive.google.com/file/d/12XeO4KXQfbvvTdLFbkYA-BeXzhlNnnuo/view) and ratings (https://drive.google.com/file/d/17V9OhXeZH9Wv17Nkh-Tqxa8svEmRZcIp/view).