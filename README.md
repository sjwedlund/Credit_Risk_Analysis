# Credit Risk Analysis

## Overview of the Analysis
The purpose of this analysis is to apply machine learning to solve the challenge of credit risk. Credit risk is an inherently unbalanced classification problem, because good loans easily outnumber risky loans. Therefore it is necessary to employ different techniques to train and evaluate models with unbalanced classes. In this challenge, I have used the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Using the credit card dataset from LendingClub, I have oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then I used a combination approach of over- and undersampling using the SMOTEEN algorithm. After that, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Results
### Naive Random Oversampling
<img width="1174" alt="Naive_Random_Oversampling" src="https://user-images.githubusercontent.com/85920136/138639011-03c4ab99-9b0b-4876-9cc6-7a87836535cc.png">
- The balanced accuracy score is 66.3%. The precision of high-risk loans is 1%, and the recall is 64%. 

### SMOTE Oversampling
<img width="1161" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/85920136/138638565-91e7f51a-4e22-4186-ac4f-21f3f1ad9aa5.png">
- The balanced accuracy score is 64.6%. The precision of high-risk loans is again 1%, while the recall this time is 63%. 

### ClusterCentroids
<img width="1165" alt="Cluster_Centroids_Resampler" src="https://user-images.githubusercontent.com/85920136/138639964-a5da340a-1f54-476f-b368-075f6ad9c843.png">
- Using the ClusterCentroids model of Undersampling, the balanced accuracy score is 51%. The precision is of high-risk loans still 1% and the recall is 59%. 

### SMOTEENN
<img width="1161" alt="SMOTEEN" src="https://user-images.githubusercontent.com/85920136/138640653-9997257f-8dc7-471d-96d5-aaa689234c6a.png">
- For this method of combination over and undersampling, the balanced accuracy score is 62.4%. The precision of high-risk loans is 1%, while the recall is 70%. 

### BalancedRandomForestClassifier
<img width="1159" alt="Random_Forest" src="https://user-images.githubusercontent.com/85920136/138641317-d316d56a-adb4-4ee8-a13c-9949d6a94288.png">
- Using the BalancedRandomForestClassifier ensemble method of resampling, the balanced accuracy score is 78.7%. The precision of high-risk loans is a slight improvement at 4%, and the recall of high-risk loans is 67%. 

### EasyEnsemble AdaBoost Classifier
<img width="1159" alt="AdaBoost_Classifier" src="https://user-images.githubusercontent.com/85920136/138641868-9112df12-451d-4459-8cc8-078db50fa000.png">
- Using the EasyEnsemble AdaBoost Classifier model, the balanced accuracy score is 92.5%. The precision of high-risk loans is 7%, and the recall of high-risk loans is 91%. 

## Summary
None of these results were very accurate in predicting high-risk loans. The EasyEnsemble AdaBoost Classifier model was slightly better at detecting high-risk credit, but it also falsely predicted 979 high-risk loans. Therefore, I do not recommend any of these models for predicting credit risk. 


