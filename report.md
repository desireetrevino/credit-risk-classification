# Module 12 Report

## Overview of the Analysis

The purpose of this analysis was to train a model to predict creditworthiness of borrowers, or loan risk in other words. Data used was a dataset of historical lending activity form a peer-to-peer lending services company.

The information included in our dataset, with more than 70,000 inputs was:
* Loan size
* Interest rate
* Borrower income
* Debt to income
* Number of accounts
* Derogatory marks
* Total debt
* Loan status - this could be Healthy loan or High risk loan and is what our model aims to predict in the future

In this dataset we had 75,036 healthy loans and 2500 high risk loans.

A Logistic Regression Model was used, with two different data split methods:
  * train_test_split
  * RandomOverSampler


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression model using train_test_split to create the samples:
  * For this model we got:
    * Balanced accuracy score: 0.9520
    * Confussion matrix: 18,663 True positives, 563 True negatives, 56 false positives and 102 false negatives
    * Classification report goes as follows:
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384


* Logistic Regression model using RandomOverSampler to create the samples:
  * For this model we got:
    * Balanced accuracy score: 0.9947
    * Confussion matrix: 55,964 True positives, 55,985 True negatives, 307 false positives and 286 false negatives
    * Classification report goes as follows:
              precision    recall  f1-score   support

           0       0.99      0.99      0.99     56271
           1       0.99      0.99      0.99     56271

    accuracy                           0.99    112542
   macro avg       0.99      0.99      0.99    112542
weighted avg       0.99      0.99      0.99    112542

## Summary

Using RandomOverSampler creates a more accurate model because we have more data to train it. We can see the better performance when we look at the accuracy, but also when we look at the classification report it is important to note that our second model is better at predicting high risk loans.
In this case, we do give more importance to the prediction of high risk loans (1) because those are the ones that with bad consequences for everyone involved.

