# AzureML-Project 1-Udacity Machine Learning Engineer Nanodegreee Program

## Problem Statement:
The data is a bank marketing dataset.The Problem statement is to predict whether a customer will make a deposit or not (binary classification problem) given a set of attributes. 

## Objective:
The following are the objectives for this project
- To train a logistic regression model in AzureML and tune its hyperparameters using Hyperdrive
- To set AutoML in AzureML and come up with a best model for the probelem
- To compare and contrast the above two approaches. 

## Overall Solutioning:
- The train.py contains a pipeline which gets dataset using TabularDatasetFactory class, pre processes the data , split into train and test sets and accepts hyperparameters "C" and "max_iter" as arguments which will be used in the hyperdrive config setup. 
- In udacity-project.ipynb , a workspace is and an experiment are create. Then a compute cluster is created as a part of initial set up.
    - For Hyper drive ; the parameter estimation policy, the Sklearn estimator , the hyperdrive config file is set up to train the model and find best hyperparameters, report the accuracy on test data and save the best model
    - For AutoML ; the data is imported , AutoML config is created which includes a 5 fold cross validation and run to find best model, find the accuracy on test data and save the best model 

## Hyperdrive setup:

### Parameter Sampling Stratergy:
Random Search was used to find the best value of "C" and "max_iter". The search space for "C" is [0.0001,1000] and serach space for "max_iter" was {75,125}.

### Early Stopping Policy:
A bandit policy of slack factor=0.17 and evaluation_interval=2 is being used. A slack factor=0.17 will terminate the training when if the metric at the current iteration is 17% less than the best performing metric. evaluation_interval=2 means that this evaluation will happen once every 2 iterations.  
