# AzureML-Project 1-Udacity Machine Learning Engineer Nanodegreee Program

## Problem Statement:
The data is a bank marketing dataset.The Problem statement is to predict whether a customer will make a deposit or not (binary classification problem) given a set of attributes. 

## Objective:
The following are the objectives for this project
- To train a logistic regression model in AzureML and tune its hyperparameters using Hyperdrive
- To set AutoML in AzureML and come up with a best model for the probelem
- To compare and contrast the above two approaches. 

## Overall Solutioning:
- The train.py contains a pipeline which pre processes the data , split into train and test sets and accepts hyperparameters "C" and "max_iter" as arguments which will be used in the hyperdrive config setup. 
- 
