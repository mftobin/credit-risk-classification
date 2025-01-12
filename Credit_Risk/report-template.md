# Module 20 Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* This analysis completed a supervised learning model of lending data to predict if lending to a borrower represents a healthy or high-risk loan. The dataset included 77,536 loan records including the following information: loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt, and whether or not a loan was a healthy or high-risk loan. 

* To complete this analysis, I separated the data into a label (loan_status) and features (all of the other characteristics of the dataset). I then split the data again into a training set and a testing set using sklearn.model_selection and train_test_split. Then I fit a logistic regression model using the training data and and used that regression model to predict loan status on the testing data. 

To analyze the performance of my regression model, I ran a confusion matrix and classifcation report. See below for results.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Predicting healthy loans ('0')
        * precision: 100%
        * recall: 99%
        * f1-score 100%
        * support : 18765
    * Predicting high-risk loans ('1')
        * precision: 84%
        * recall: 99%
        * f1-score: 89%
        * support: 619

## Summary

As you can see from the results above, the model predicts healthy and high-risk loans with good accuracy, however, the model predicts healthy loans at a much higher accuracy level. If the lender is concerned about lending as much as possible, the model could use some improvement to make sure borrowers are not mislabeled as high-risk when they could potentially be a healthy borrower, however if the lender is more risk-averse, the model would do a better job of helping a lender ensure that as many of their loans are "safe loans".

This model could be improved with information about whether or not the borrowers ended up paying their loan fully or if they defaulted.
