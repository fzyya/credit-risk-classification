# Credit Risk Classification Report

## Overview of the Analysis

The purpose of this analysis is to build a machine learning model to predict the risk of default on loans. Specifically, this model predicts high-risk loans, which can help financial institutions in managing and mitigating the risk associated with lending.

The data used for this analysis contains financial information about loans, including attributes such as loan amount, interest rate, borrower income, and others. The target variable we aimed to predict is `loan_status`, where a value of `0` indicates a healthy loan and a value of `1` indicates a high-risk loan.

### Financial Information and Data Description
- **Target Variable:** `loan_status`
  - `0`: Healthy Loan
  - `1`: High-Risk Loan


### Machine Learning Process & Methods
1. **Data Preparation:** Read the dataset from a CSV file, convert into a Pandas DataFrame, and split the data into features (`X`) and labels (`y`).
2. **Data Splitting:** Split the data into training and testing sets using `train_test_split`.
3. **Model Selection and Training:** Use the `LogisticRegression` algorithm to build and train the model on the training data.
4. **Prediction:** Use the trained model to make predictions on the testing data.
5. **Evaluation:** Evaluate the model's performance using a confusion matrix and classification report to assess accuracy, precision, recall, and F1-score.


### Machine Learning Model Results: Logistic Regression
- **Accuracy:** 99%
- **Precision for Healthy Loans (0):** 1.00
- **Recall for Healthy Loans (0):** 0.99
- **F1-Score for Healthy Loans (0):** 1.00
- **Precision for High-Risk Loans (1):** 0.84
- **Recall for High-Risk Loans (1):** 0.94
- **F1-Score for High-Risk Loans (1):** 0.89
- **Macro Average Precision:** 0.92
- **Macro Average Recall:** 0.97
- **Macro Average F1-Score:** 0.94
- **Weighted Average Precision:** 0.99
- **Weighted Average Recall:** 0.99
- **Weighted Average F1-Score:** 0.99

## Summary

The logistic regression model is highly accurate and performs well in predicting healthy loans ('0'). The precision and recall for healthy loans are both near 1.0, indicating that the model correctly identifies almost all healthy loans while having a very low false positive rate.
The model also performs well on high-risk loans ('1'), with a precision of 0.84 and a recall of 0.94. This means that the model is effective at identifying the majority of high-risk loans, although it has a slightly higher false positive rate compared to healthy loans.

Regardless of how well the model performs, there may be issues with algorithmic bias with impact on lending fairness. Furthermore, the model's lack of transparency and potential for privacy violations should be carefully considered prior to adoption.
