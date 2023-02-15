# CREDIT RISK ANALYSIS

## Overview of load prediction risk analysis

&ensp;&ensp;The aim of this project is to use supervised machine learning to predict credit risk. The credit risk problem is an inherently unbalanced classification problem where the number of good loans easily outnumbers risky loans. Therefore, we will use different techniques to train and evaluate models with unbalanced classes.

## Data:
 We will used the credit card dataset from LendingClub, a peer-to-peer lending services company. This dataset contains information about various features such as loan amount, interest rate, employment length, credit score , etc. It also contains a binary column indicating whether a loan is risky or not.

 ## Tools :
   We will use the imbalanced-learn and scikit-learn libraries in python to implement the below techniques.

## Purpose and Methodology :

 The purpose of this analysis is to evaluate the different machine learning models to predict credit risk. Credit risk is the risk of a borrower defaulting on their loan payments, and predicting credit risk is crucial for financial instituations to minimize their risk exposure. 
 
  We will employ the following techniques to handle the unbalanced class problem in credit risk prediction:

  1. Oversampling : We will oversample the minority class using the RandomOverSampler and SMOTE algorithms

  2. Undersampling : WE will undersample the majority class using the ClusterCentroid algorithm

  3. Combining Oversampling and Undersampling : WE will use a combinatorial approach of over and under sampling using hte SMOTEENN algorithm.

  We will then compare the performance of the two new machine learning models BalancedRandomForestClassifier and EasyEnsembleClassifier, which reduce bias and predict credit risk.

  We will then evaluate the performace of each model using standard evaluation metrics such as accuracy, precision and recall. We will also use a confusion matrix to visually evaluate the model's performace. Finally generate an imbalanced classfication report which produces the complete report and metrics of all the data.


## Results :

 The results for the six machine learning models with their corresponding metrics are
 
## 1. Resampling Models:

### Naive Random Oversampling :

 - Balanced Accuracy  : 0.6456130066757718<br>
 - Precision(High/Low): 0.01/1.00<br>
 - Recall (High/Low)  : 0.61/0.68<br>

### SMOTE Oversampling :

  - Balanced Accuracy : 0.6234433606890912<br>
  - Precision(High/Low): 0.01/1.00<br>
  - Recall (High/Low) : 0.61/0.64<br>

### ClusterCentroids Undersampling :

  - Balanced Accuracy : 0.5293026900499977<br>
  - Precision(High/Low): 0.01/1.00<br>
  - Recall (High/Low) : 0.61/0.45<br>
  
## 2. SMOTEENN Model:

### Combination (Over and Under) Sampling:

  - Balanced Accuracy : 0.6531287896185101<br>
  - Precision(High/Low): 0.01/1.00<br>
  - Recall (High/Low) : 0.69/0.62<br>

## 3. Ensemble Classifiers:

### Balanced Random Forest Classifier

  - Balanced Accuracy : 0.7885466545953005<br>
  - Precision(High/Low): 0.03/1.00<br>
  - Recall (High/Low) : 0.70/0.87<br>

### Feature Importance (top 5 features):
  - total_rec_prncp<br>
  - total_pymnt_inv<br>
  - total_pymnt<br>
  - last_pymnt_amnt<br>
  - total_rec_int<br>

### Easy Ensemble AdaBoost Classifier

  - Balanced Accuracy  : 0.9316600714093861<br>
  - Precision(High/Low): 0.09/1.00<br>
  - Recall (High/Low)  : 0.92/0.94<br>

   All the models have Precision which is Low for High-risk and High for Low-risk

## Summary  and Recommendation :

&ensp;&ensp;In this credit risk analysis, we used several machine learning models to predict credit risk, including resampling models such as RandomOverSampler, SMOTE, and ClusterCentroids, as well as ensemble classifiers such as BalancedRandomForestClassifier and EasyEnsembleClassifier. The purpose of this analysis was to evaluate the performance of these models in predicting credit risk and to recommend the best model for this task.

&ensp;The results of the machine learning models showed that overall, ensemble classifiers(BalancedRandomForestClassifier and EasyEnsembleClassifier) outperformed the resampling models  in predicting the credit risk.
  
 &ensp;The Easy Ensemble Classfier had the highest balanced accuracy score of 0.93 , with the highest precision and recall scores for both high-risk and low-risk categories. 
    
 &ensp;The Balanced Random Forest Classifier had a balanced accuracy score of 0.79, which is also high, but its performance was not as good as Easy Ensemble classifier.

&ensp;&ensp;Therefore, depending on the specific needs and priorities of the user, either the EasyEnsembleClassifier or the BalancedRandomForestClassifier could be recommended for predicting credit risk. The resampling models had much lower balanaced accuracy scores, which makes them less reliable for redicitng credit risk.

&ensp;However, it should be noted that both models still had relatively low precision scores for high risk, indicating that they may not be the most reliable in accurately identifying high risk borrowers. As such, further analysis and improvements may be necessary to develop a more robust and accurate model for predicting credit risk

