# Credit Risk Classification

## Overview

For this project, I created a Logistic Regression Model to predict a borrower's loan status (creditworthiness) based on factors such as loan size, interest rate, income, debt to income, number of accounts, derogatory marks, and total debt.

I then used the sklearn.metrics library to generate a confusion matrix and a classification report to evalute the model's effectiveness. You can see the script for this model in the credit_risk_classification.ipynb file in this repository.

Based on the results, I would recommend to use this model to help evaluate risk. You can see a deeper analysis and explanation of my recommendation below in this README.


## Conclusions and Written Analysis

The primary question we want to answer through analyzing the machine learning model results is this: Should this company use this model to predict whether a loan is healthy or high-risk? This will ultimately inform whether or not the company should make a loan to the borrower.

Below is a summary of the accuracy scores generated by the classification report:

* Class 0 (negative, indicating a healthy loan)
    * The precision score of 1.00 indicates the highest level of precision, meaning that of all predicted negatives, close to 100% are correctly classified as negative/healthy.
    * The recall score of 1.00 indicates the highest possible recall score, meaning that of all actual negatives, close to 100% are correctly classified as negative/healthy.
    * The F1-Score of 1.00 indicates the highest possible F1-score, indicating a good balance between precision and recall and that both are close to 100% accurate.
* Class 1 (positive, indicating a high-risk loan)
    * The precision score of 0.87 indicates a decently high level of precision, meaning that of all predicted positives, around 87% are correctly classified as positive/high-risk. Around 13% are falsely classified as high-risk when they are actually healthy. While this is not as risky as false negatives, it still means that the company could potentially deny healthy loans and rewarding business opportunities.
    * The recall score of 0.95 indicates a very high recall score, meaning that roughly 95% of all actual high-risk loans are correctly classified as high-risk. The other 5% may be falsely classified as healthy when they are actually high-risk. While this percentage is smaller, the financial impact of even a few high-risk loans could be significant. 
    * The F1-Score of 0.91 indicates a pretty good balance between precision and recall, meaning that both precision and recall are highly accurate.

Based on these results, I would say that the model is extremely effective in predicting both healthy and high-risk loans, although it is slightly more accurate in predicting healthy loans than high-risk ones. 

In this situation, predicting false negatives (loans classified as healthy that are actually high-risk) is what would cause the most harm, but the likelihood of that occuring is minimal (around 5%). Thus, I would recommend that the company uses the model to predict loan risk, with some additional caution and oversight to minimize false negatives even further.