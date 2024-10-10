# Module 12 Report Template

## Overview of the Analysis
The purpose of this analysis was to build a machine learning model that can predict the creditworthiness of borrowers based on historical lending activity. Specifically, the goal was to identify high-risk loans (Class 1) and healthy loans (Class 0) using the following features :

-Loan size
-Interest rate
-Borrower income
-Debt-to-income ratio
-number of accounts
-Derogatory marks
-Total debt.

The dataset contained financial information on borrowers and loans, where the key target variable was the loan status (loan_status), indicating whether a loan was classified as healthy (0) or high-risk (1). 

The distribution of the target variable showed a significant class imbalance:

Healthy loans (0): 75,036 (97%)
High-risk loans (1): 2,500 (3%)

The machine learning process involved several key stages:

Data Preparation: The dataset was split into features (X) and labels (y). Then, it was  divided into training and testing sets (80% training, 20% testing).
Model Selection: I chose Logistic Regression as the classification algorithm due to its simplicity and interpretability for binary classification problems.
Model Training: The logistic regression model was trained on the training data, using borrower financial features to predict the loan status.
Evaluation: I generated predictions on the testing data and evaluated the model's performance using accuracy, precision, recall, F1-scores, and a confusion matrix.

## Results
The logistic regression model performed exceptionally well for predicting healthy loans (class 0), with perfect precision, recall, and F1-scores. With an accuracy of 99% (The model correctly predicted 99% of the loans), indicating that the model is performing very well on the test data.

For high-risk loans (Class 1), the performance was strong, with a slight drop in precision (0.86) and recall (0.91). These are strong valuesgiven the class imbalance, Class 1 had 507 instances counted, and Class 0 had 15,001 instances counted.

Machine Learning Model 1: Logistic Regression

Precision (Class 0): 1.00 — Of the loans predicted as healthy, 100% were correct.
Recall (Class 0): 1.00 — Of the actual healthy loans, 100% were correctly identified.
Precision (Class 1): 0.86 — Of the loans predicted as high-risk, 86% were correct.
Recall (Class 1): 0.91 — Of the actual high-risk loans, 91% were correctly identified.
F1-Score (Class 1): 0.88 — A balance between precision and recall for high-risk loans.

## Summary
The logistic regression model performed exceptionally well for predicting healthy loans (Class 0), with perfect precision, recall, and F1-scores. For high-risk loans (Class 1), the performance was strong, with a slight drop in precision (0.86) and recall (0.91).

Given that identifying high-risk loans is the primary objective, the model's high recall for Class 1 (91%) ensures that most high-risk loans are correctly flagged, which is crucial for financial risk management. The high accuracy of 99% further demonstrates the model's overall reliability.

Recommendation: I recommend using the logistic regression model, as it balances both the ability to correctly identify high-risk loans (Class 1) and maintain overall accuracy. However, due to the class imbalance, you may want to explore methods such as resampling or more advanced techniques to further improve performance on class 1 predictions. 

Future Considerations: It should be noted, however, that there are limitations to the model utilised here and future models could be established (such as Random Forest) to improve the overall performance. 
