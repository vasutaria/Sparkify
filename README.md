# Sparkify

This is a Data Science Project on Sparkify
Problem:
Determine customer churn for a music streaming company called Sparkify.

Table of Contents

Installation
Project Motivation
File Descriptions
Results
Licensing, Authors, and Acknowledgements
Installation

This project uses the following software and python libraries

Python 3.6
NumPy
Pandas
scikit-learn
matplotlib
Pyspark-2.4.1
You will also need to have software installed to run and execute a Jupyter Notebook

Project Motivation

Sparkify is a music streaming service provider, like Spotify or Pandora. There are millions of users that play their favorite songs through music streaming services either under the free tier or paid subscription model. All users have to register and can upgrade or downgrade their subscription plan any time. There is also an option to cancel service altogether. We need to save the customers before they churn by preparing a ML model that will predict with higher accuracy.

In this project we'll be performing the following tasks:

Data Exploration
Learn about the data
Define Churn and label data based on churn definition
Determine which feature or feature value can be user to defin churn
Feature Engineering
Create features for each user. This data will be used as input to the model
Data transformation, data splitting and model training
Transform feature engineered data.
Split data into training, validation and test data.
Build a machine learning model to train using training data
File Descriptions

Sparkify.ipynb : Jupyter notebook used for this project

Preprocessing:
In order to deal with the imbalance in data I created additonal features. Grouped the number of songs played by the user, number of times the customer gave a thumps up or thumbs down to the song by each user. These features defines the type of customer. If there were more thumbs up that is an indication of a happier customer, number of songs played gives us an idea of the usage and reliance on the application. The ts column was meaningless in the original format so I created a new hour column to show timestamp and then grouped it to understand how many hours a customer was logged in the system.
After data exploration, analysis and visualization below are the features I chose to run my model on. 
+------+-----+-----------+---------+-------------+---------------+
|userId|label|SongsPlayed|HourCount|thumbsUpCount|thumbsDownCount|
+------+-----+-----------+---------+-------------+---------------+
|100010|    0|        275|       26|           17|              5|
|200002|    0|        387|       32|           21|              6|
|   124|    0|       4079|      306|          171|             41|
|    51|    1|       2111|      156|          100|             21|
|     7|    0|        150|       18|            7|              1|
+------+-----+-----------+---------+-------------+---------------+
Because I had more then one feature I used VectorAssember to convert the features in rawFeatures and then applied a standard scaler function to normalize the features. Next I applied Index labels and Feature Indexer to automatically identify categorical features with more then 4 distinct values.
Next I split my data in Training and Testing Sets by 70% and 30% consequently. 
I used the Random Forest Classifier which gave me a F1 Score of 69% and Gradient Boost Classifer which gave me a F1 Score of 64%.

Analyzed the sparkify dataset and come up with new features to predict churn. I then created a machine learning model and tuned it to improve its performance. I was able to achieve F1 score of 69% on the test dataset and 83% on the full dataset.

Enhancement:
I used Cross-Validation (cv) as one of my hyperperameter tuning technique to improve my model. Cross-Validation begins by splitting the dataset into a set of folds which are used as separate training and test datasets. E.g., with k=3k=3 folds, CrossValidator will generate 3 (training, test) dataset pairs, each of which uses 2/3 of the data for training and 1/3 for testing

Conclusion:

There are other possible ways I can improve the model performance by creating additional features, testing additional models, using ensemble methods or by fine tuning parameters. The next step would be to test this model on the big dataset on a cloud server like IBM or Amazon to check the performance. If the results are consistent or better then I would propose the model to be implemented on an experimental phase like A/B Testing where A is the control group and B is the experimental group.
Thats it for now! I have covered the details of my SparkML model and its Implementation and Perfomance. I outlined some ideas on how I can improve this further. If you like to learn more about my Model check out my github: https://github.com/vasutaria/Sparkify.git

If you would like to read my blog on this: https://medium.com/@vaishali.sutaria/churn-a-real-problem-predict-with-spark-7d73b2a1f614

Licensing, Authors, Acknowledgements
Dataset provided by Udacity



