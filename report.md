# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to examine credit risk data from a sample dataset. The analysis will use logistic regression modeling and oversampling to asses loan risk. Will logistic regression prove to be useful in this analysis?

Review of dataset:

The sample data shows loan details such as loan amount, interest, age of borrower, as well as borrow statistics.
"loan_status" is the risk status of the loan. 0 = health, 1 = high-risk

Dataset basics:

Original data counts:
0: 75035
1: 2500

Oversampled data counts:
0: 56271
1: 56271

The model is trying to predict which loans present a healthy amount of risk and which are high-risk.

Steps:

1. Prepare data
2. Separate data columns into the outcome labels
3. Train test split
4. Pick ML model for classification (LogisticRegression)
5. Fit model with training data
6. Use model to make predictions with test data
7. Evaluate predictions by comparing metrics, monfusion matrix, classifications reports etc.


Methods used:

SKLearn LogisticRegression
train_test_split
confusion_matrix
classification_report



## Results

* Machine Learning Model 1:
  * Accuracy: 0.99 
  * Precision (class 0): 1.00, Precision (class 1): 0.85
  * Recall (class 0): 0.99, Recall (class 1): 0.91

* Machine Learning Model 2:
  * Accuracy: 0.99 
  * Precision (class 0): 1.00, Precision (class 1): 0.84
  * Recall (class 0): 0.99, Recall (class 1): 0.99

## Summary

The Logistic Regression model had high precision and recall in its prediction of healthy loans but was lacking when it came to predicting high-risk loans. More data may be needed to increase the precision of predictions in the high-risk category.

When applying the oversampled data, healthy loan predictions were virtually identical. Where things changed was in the high-risk predictions. The model was able to significantly increase the recall score. This would mean that it is more likely to predict all high-risk loans at the risk of more false positives.

Depending on the loan amount or the business model of the leinholder/bank/institution etc..., it may make sense to choose the the oversampled model. If this information is to be used in loan approvals, it would minimize risk at the cost of rejecting more loan inquiries. For example, a low dollar amount loan does not present as large of a potential loss to the leinholder. On the other hand, larger loan amounts present a larger potential loss to leinholder, and the leinholder would be more likely to reject loans of this type.

In the context of minimizing loss, I would recommend the model with the oversampled data. This would likely result in lower defaulted loans.