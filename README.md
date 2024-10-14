# credit-risk-classification

- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

- Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

- Note: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

- Split the data into training and testing datasets by using train_test_split.

- Create a Logistic Regression Model with the Original Data

Use your knowledge of logistic regression to complete the following steps:

- Fit a logistic regression model by using the training data (X_train and y_train).

- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

- Evaluate the model’s performance by doing the following:

- Generate a confusion matrix.

- Print the classification report.

- Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

# Credit Risk Report

## Overview of the Analysis

The purpose of this analysis is to build evaluate a logistic regression model based on loan risk. The model seeks to identify the creditworthiness of borrowers using historical lending data. In the dataset, the "loan_status" column tags each loan as "healthy" (with a marker of 0) or "high-risk" (with a marker of 1). The model examines the features comprising the dataset, such as loan size, borrower income, etc., to predict whether or not a loan is risky based on past results. After separating the features from the labels (the aforementioned "loan_status" column), I split the data into training and testing datasets. I instantiated a logistic regression model and fit it using the training data, then made predictions using the testing data. Finally, I used a confusion matrix and classification report to display the test results. These results show the overall accuracy of the model, as well as the accuracy in predicting both healthy and high-risk loans.

## Results

The results are classified as follows:

- The accuracy score, which summarizes the overall rate of correct predictions.
- The precision score, which tells us how many predicted positive cases (in this case, high-risk designations) were actually positive. The precision score is also the rate of true positives.
- The recall score, which shows how many of the true positive cases were correctly predicted. A high recall rate indicates a low rate of false negatives, and vice versa.

The model performed as follows: 

- Accuracy score: 0.99 overall.
- Precision score: 1.00 for healthy labels, 0.84 for high-risk labels
- Recall score: 0.99 for healthy labels, 0.94 for high-risk labels.

## Summary

Based on this performance, I would recommend this model. It is quite good at predicting healthy loans: most of the loans that it identified as low-risk were in fact low-risk (a total of 18,655 loans) and only 36 were mis-identified as healthy only to be revealed as risky. This demonstrates a low rate of false negatives: using this model, an institution would be less likely to mistakenly approve a loan for a high-risk customer. Since we are working with finances, ensuring that we avoid false negatives is essential. On the other hand, the model is less adept at predicting risky loans. It correctly designated 583 loans as high-risk, while falsely identifying another 110 as high-risk when they were not. This means that, using the model, an institution may deny a loan to a customer they perceive as high-risk, when they are in fact safe. Although it is not perfect, the model minimizes the likelihood of approving a loan that would negatively affect the bank.
