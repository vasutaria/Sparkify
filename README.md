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

Analyzed the sparkify dataset and come up with new features to predict churn. I then created a machine learning model and tuned it to improve its performance. I was able to achieve F1 score of 69% on the test dataset and 83% on the full dataset.

Conclusion

There are other possible ways I can improve the model performance by creating additional features, testing additional models, using ensemble methods or by fine tuning parameters. The next step would be to test this model on the big dataset on a cloud server like IBM or Amazon to check the performance. If the results are consistent or better then I would propose the model to be implemented on an experimental phase like A/B Testing where A is the control group and B is the experimental group.
Thats it for now! I have covered the details of my SparkML model and its Implementation and Perfomance. I outlined some ideas on how I can improve this further. If you like to learn more about my Model check out my github: https://github.com/vasutaria/Sparkify.git

If you would like to read my blog on this: https://medium.com/@vaishali.sutaria/churn-a-real-problem-predict-with-spark-7d73b2a1f614

Licensing, Authors, Acknowledgements
Dataset provided by Udacity



