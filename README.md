# Machine_Learning_Credit_Risk
Using Machine Learning in Python to determine credit risk for different customers.

## Project Overview
Used different resampling methods such as Oversampling, Undersampling, and Combination to predict the credit risk of several potential borrowers. An ensemble analysis was also created using Random Forest and Adaboost to also determine whether potential borrowers have credit risk or not.

## Resources
- Data Sources: LoanStats_2019Q1.csv
- Software: Python 3.8.2, NumPy 1.11, SciPy 0.17, Scikit-learn 0.21

## Analysis

## Resampling
### Naive Random Oversampling
- Balanced Accuracy Score
64.03%
- Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 62             | 39              |
| Actually False | 5,317          | 11,787          |
- Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.66   |
| Low-Risk  | 17,104 | 1.00      | 0.62   |
- Summarized Analysis


### SMOTE Oversampling
- Balanced Accuracy Score
65.15%
- Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 62             | 39              |
| Actually False | 5,317          | 11,787          |
- Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.61   |
| Low-Risk  | 17,104 | 1.00      | 0.69   |
- Summarized Analysis


### Undersampling
- Balanced Accuracy Score
65.15%
- Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 67             | 34              |
| Actually False | 10,217         | 6,887           |
- Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.66   |
| Low-Risk  | 17,104 | 1.00      | 0.40   |
- Summarized Analysis


### Combination (Over and Under) Sampling
- Balanced Accuracy Score
53.30%
- Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 73             | 28              |
| Actually False | 7,405          | 9,699           |
- Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.72   |
| Low-Risk  | 17,104 | 1.00      | 0.57   |
- Summarized Analysis


## Ensemble
### Balanced Random Forest Classifier
- Balanced Accuracy Score
78.55%
- Confusion Matrix
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.72   |
| Low-Risk  | 17,104 | 1.00      | 0.57   |
- Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.04      | 0.67   |
| Low-Risk  | 17,104 | 1.00      | 0.90   |
- Summarized Analysis


### Easy Ensemble AdaBoost Classifier
- Balanced Accuracy Score
93.17%
- Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 93             | 8               |
| Actually False | 983            | 16,121          |
- Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.09      | 0.92   |
| Low-Risk  | 17,104 | 1.00      | 0.94   |
- Summarized Analysis
