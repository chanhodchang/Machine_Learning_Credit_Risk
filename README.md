# Machine_Learning_Credit_Risk
Using Machine Learning in Python to determine credit risk for different customers.

## Project Overview
Used different resampling methods such as Oversampling, Undersampling, and Combination to predict the credit risk of several potential borrowers. An ensemble analysis was also created using Random Forest and Adaboost to also determine whether potential borrowers have credit risk or not.

## Resources
- Data Sources: LoanStats_2019Q1.csv
- Software: Python 3.8.2, NumPy 1.11, SciPy 0.17, Scikit-learn 0.21

## Analysis

### Resampling
#### Naive Random Oversampling
Balanced Accuracy Score
64.03%
Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 62             | 39              |
| Actually False | 5,317          | 11,787          |
Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.66   |
| Low-Risk  | 17,104 | 1.00      | 0.62   |
Summarized Analysis
Looking at the data, the Balanced Accuracy Score came out to 64.03% which means that it detected 66.03% of risks correctly. Looking at the Classification Report, almost 99% of the High-Risk predicted is actually Low-Risk because of the use of oversampling. Oversampling is when the smaller class is artificially overpopulated to give a better prediction which is why all the High-Risk predicted is actually Low-Risk. This is why the Accuracy Score is around 66.03% because of all the Low-Risk loans that were predicted to be High-Risk.

#### SMOTE Oversampling
Balanced Accuracy Score
65.15%
Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 62             | 39              |
| Actually False | 5,317          | 11,787          |
Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.61   |
| Low-Risk  | 17,104 | 1.00      | 0.69   |
Summarized Analysis
Looking at the data, the Balanced Accuracy Score came out to 65.15% which means that it detected 65.15% of risks correctly. Looking at the Classification Report, almost 99% of the High-Risk predicted is actually Low-Risk because of the use of SMOTEE Oversampling. This type of oversampling has a similar concept to the previous method which means that all the High-Risk predicted is actually Low-Risk. This is why the Accuracy Score is around 65.15% because of all the Low-Risk loans that were predicted to be High-Risk.

#### Undersampling
Balanced Accuracy Score
65.15%
Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 67             | 34              |
| Actually False | 10,217         | 6,887           |
Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.66   |
| Low-Risk  | 17,104 | 1.00      | 0.40   |
Summarized Analysis
Looking at the data, the Balanced Accuracy Score came out to 65.15% which means that it detected 65.15% of risks correctly. Looking at the Classification Report, almost 99% of the High-Risk predicted is actually Low-Risk because of the use of undersampling. Undersampling is when there is a class balance and so the majority class is artificially reduced to balance out the class. Which means that all the Low-Risk predicted are accurate. This is why the Accuracy Score is around 66.03% because of all the Low-Risk loans that were predicted to be High-Risk.

#### Combination (Over and Under) Sampling
Balanced Accuracy Score
53.30%
Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 73             | 28              |
| Actually False | 7,405          | 9,699           |
Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.01      | 0.72   |
| Low-Risk  | 17,104 | 1.00      | 0.57   |
Summarized Analysis
Looking at the data, the Balanced Accuracy Score came out to 53.30% which means that it detected 53.30% of risks correctly. Looking at the Classification Report, almost 99% of the High-Risk predicted is actually Low-Risk because of the use of oversampling. Combination Sampling is exactly what it sounds like, the combination of both Over and Under Sampling. This is why the Accuracy Score is around 53.30% because of all the Low-Risk loans that were predicted to be High-Risk.

#### Resampling Analysis
Looking at the 4 different resampling methods, the one to choose is either the SMOTEE Oversampling or the Undersampling Method as they both result in a 65.15% accuracy socre which is higher than the other 2 scores from the other methods. But between those two methods, Undersampling has a higher Recall at 0.66 for the High-Risk which means that it is looking at a larger sample size and potential more prevelant High-Risks. 

### Ensemble
#### Balanced Random Forest Classifier
Balanced Accuracy Score
78.55%
Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 68             | 33              |
| Actually False | 1,749          | 15,355          |
Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.04      | 0.67   |
| Low-Risk  | 17,104 | 1.00      | 0.90   |
Summarized Analysis
Looking at the data, the Balanced Accuracy Score came out to 78.55% which means that it detected 78.55% of risks correctly. Looking at the Classification Report, almost 99% of the High-Risk predicted is actually Low-Risk because of the use of Balanced Random Forest Classifier. The Random Forest Classifier uses a process of creating multile Decision Trees which creates a vast amount of predictions. These are then used to make a final prediction. The Precision shows that only 4% of High-Risk predicted is a true High-Risk.

#### Easy Ensemble AdaBoost Classifier
Balanced Accuracy Score
93.17%
Confusion Matrix
|                | Predicted True | Predicted False |
|----------------|----------------|-----------------|
| Actually True  | 93             | 8               |
| Actually False | 983            | 16,121          |
Classification Report
|           | Count  | Precision | Recall |
|-----------|--------|-----------|--------|
| High-Risk | 101    | 0.09      | 0.92   |
| Low-Risk  | 17,104 | 1.00      | 0.94   |
Summarized Analysis
Looking at the data, the Balanced Accuracy Score came out to 93.17% which means that it detected 93.17% of risks correctly. Looking at the Classification Report, almost 99% of the High-Risk predicted is actually Low-Risk because of the use of the Easy Ensemble AdaBoost Classifier. The AdaBoost Classifier combines multiple classifiers to create a more accurate classifier. This is why the AdaBoost has the highest Balanced Accuracy Score. 

#### Ensemble Analysis
Looking at the two different Classifiers the obvious choice to select the one with the higher accuracy. And since the AdaBoost Classifier's purpose is to create a higher accuracy, it is the stronger choice. The Random Forest Classifier also has a lower precision and a smaller Recall. This means that the AdaBoost Classifier is the best classifier to choose. 