## Overview of the Analysis
The purpose of this analysis was to build a machine learning model that can predict the creditworthiness of borrowers based on historical lending activity. Specifically, the goal was to identify "High-risk" loans (Class 1) and :"Healthy" loans (Class 0). The dataset provided by the bank contained 77,536 entries which contained financial information on borrowers and loans, such as, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.

 The key target variable was the loan status (loan_status), that indicates whether a loan was classified as "Healthy" (0) or "High-risk" (1). The distribution of the target variable (value_counts) reflects a strong inbalance between loan status', as below:

Healthy loans (0): 75,036 
High-risk loans (1): 2,500 

The machine learning process involved several key stages:

Data Preparation: The dataset was split into features (X) and labels (y). Then, it was divided into training and testing sets (80% training, 20% testing).

Model Selection: I chose Logistic Regression as the classification algorithm due to its simplicity and interpretability for binary classification problems.

Model Training: The logistic regression model was trained on the training data, using borrower financial features to predict the loan status.

Evaluation: I generated predictions on the testing data and evaluated the model's performance using accuracy, precision, recall, F1-scores, and a confusion matrix.

## Results
Machine Learning Model 1: Logistic Regression

For Healthy loans (Class 0), the results are below:
-Accuracy: 99%, that is, the model correctly predicted 99% of the loans.
-Precision: 1.00, 100% of loans predicted as healthy were correct. 
-Recall: 1.00, 100% of the actual healthy loans correctly identified.

For High Risk loans (Class 1), the results are below:
-Precision: 0.86, 86%  of the loans predicted as high-risk were correct.
-Recall: 0.91, 91% of actual high-risk loans were correctly identified.
-F1-Score: 0.88, a balance between precision and recall for high-risk loans.


## Summary
The logistic regression model performed exceptionally well for predicting healthy loans (class 0), with perfect precision, recall, and F1-scores. For high-risk loans (Class 1), the performance was strong, with a slight drop in precision (0.86) and recall (0.91).

Given that identifying high-risk loans is the primary objective, the model's high recall for Class 1 (91%) ensures that most high-risk loans are correctly flagged, which is crucial for financial risk management. The high accuracy of 99% further demonstrates the model's overall reliability.

Recommendation: I recommend using the logistic regression model, as it balances both the ability to correctly identify high-risk loans (Class 1) and maintains overall accuracy. However, due to the class imbalance, other methods could be used to further improve performance on predictions of high risk loans.
