# Module 20 Challenge Report

## Overview of the Analysis

The analysis performed in this challenge submission consisted of training a classifying regressor to predict whether a loan in a peer-to-peer lending company is healthy or high-risk. The purpose of this analysis was to evaluate the performance of the classifier given the training data, and discuss potential improvements or shortcomings of the resulting model.

The data included information about the borrower and loan, including salaries, number of accounts, size of the loan, and others. It also included a classifiation of each loan whether it was healthy or high-risk. The goal was for the model to be trained on this data, and subsequently be able to predict whether a future loan would be healthy or high-risk. Thus, the analysis included partitioning the data to form different datasets for training and predicting, fitting the model to the data and training it, then predicting a value for `loan_status`. 

The model used was logistic regression via `LogisticRegression` provided by `sklearn.linear_model`.

## Results

* Precision - The precision of the model was noticeably higher when predicting healthy loans than its ability to correctly predict high-risk loans. Precision refers to the proportion of predictions which were correct, so 1.0 for healthy models is quite high.
* Recall - The recall of the model was higher when predicting healthy loans than when predicting high-risk loans, but not by much. Recall refers to the proportion of original data points which were correctly accounted for.
* Accuracy - the F1-scores of both 0 and 1 classes as well as the accuracy of the model in general were high. However, due to the nature of the company, we'd generally prefer for the model to more accurately predict high-risk loans. There is greater loss associated with a false-negative than with a false-positive.

## Summary

The logistic regression model used performed well, but we would need to turn it in order to increase the precision and recall of the y = 1 predictions. We would want our model to be biased towards treating a loan as high-risk, to prevent accruing the loss associated with a defaulted loan. Redundant resources dedicated towards healthy loans incorrectly deemed high-risk would not constitude as great of losses. The model can likely be used but with modifications and perhaps pre-processing.
