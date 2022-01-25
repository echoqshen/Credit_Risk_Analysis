# Credit_Risk_Analysis

## Overview of the analysis:
This exercise is to employ different techniques to train and evaluate different machine learning models to predict credit risk with unbalanced classes. 
Algorithms used in the analysis:
* the oversampling **RandomOverSampler** and **SMOTE** algorithms.
* the undersampling **ClusterCentroids** algorithm to resample the data.
* the combinatorial **SMOTEENN** algorithm to resample the training data.
* **BalancedRandomForestClassifier** and **EasyEnsembleClassifier** to reduce bias.
 
## Results:
We use balanced accuracy score, confusion matrix and imbalanced classification report to compare results.

#### **RandomOverSampler**
<p align="center"> < <img src='https://user-images.githubusercontent.com/90880564/150888883-bf5fbdea-e210-446a-92cc-3b4dd66dd5c3.png?raw=true" alt="Sublime's custom image"/>
<img src="https://user-images.githubusercontent.com/90880564/150879796-ac9d1a7c-c718-411d-a203-5a850549ea49.png?raw=true" alt="Sublime's custom image"/>
</p>

The balanced accuracy score is 62%.\
The high_risk precision is about 1% only with 60% sensitivity which makes a F1 of 2% only.\
Due to the imbalanced number of the low_risk population, its precision is almost 100% with a sensitivity of 65%.

#### **SMOTE**
<p align="center"> <img src='https://user-images.githubusercontent.com/90880564/150889306-0cd2943c-4c6a-44bb-8533-9544e9e2a87d.png?raw=true" alt="Sublime's custom image"/>
<img src='https://user-images.githubusercontent.com/90880564/150889407-bc55ec13-a0d5-4ac6-acbe-caac05dbf50e.png?raw=true" alt="Sublime's custom image"/>
</p>   
                        
The balanced accuracy score is 65%. \
The high_risk precision is about 1% only with 64% sensitivity which makes a F1 of 2% only. \
Due to the imbalanced number of the low_risk population, its precision is almost 100% with a sensitivity of 66%. \
Very similiar result to the previous one.
                        
#### **ClusterCentroids**
<p align="center"> <img src='https://user-images.githubusercontent.com/90880564/150902602-c05a27b8-8aee-4e4b-86db-3b13940f9d81.png?raw=true" alt="Sublime's custom image"/>
</p>

The balanced accuracy score is down to 52%. \
The high_risk precision is about 1% only with 59% sensitivity which makes a F1 of 1% only.\
Due to the imbalanced number of the low_risk population, its precision is almost 100% with a sensitivity of 46%.     

#### combinatorial **SMOTEENN**
<p align="center"> <img src='https://user-images.githubusercontent.com/90880564/150903138-4d353ed2-fcbc-4512-b38e-f3fe8c413168.png?raw=true" alt="Sublime's custom image"/> </p>

The balanced accuracy score is 62%. \
The high_risk precision is about 1% only with 69% sensitivity which makes a F1 of 2%.\
Due to the imbalanced number of the low_risk population, its precision is almost 100% with a sensitivity of 54%.

#### **Balanced Random Forest Classifier**
<p align="center"> <img src='https://user-images.githubusercontent.com/90880564/150904192-4db6b157-2123-4544-a10b-6695abe7943b.png?raw=true" alt="Sublime's custom image"/> </p>

The balanced accuracy score is greatly improved to 79%. \
The high_risk precision is about 4% only with 67% sensitivity which makes a F1 of 7%.\
Due to a lower number of false positives, its precision is almost 100% with a sensitivity of 91%.

#### **Easy Ensemble AdaBoost Classifier**
<p align="center"> <img src='https://user-images.githubusercontent.com/90880564/150904902-5b072f7f-ff0a-483a-a6ab-983c4751a8a3.png?raw=true" alt="Sublime's custom image"/> </p>

The balanced accuracy score is very high at 93%. \
The high_risk precision is about 7% only with 91% sensitivity which makes a F1 of 14%.\
Due to a lower number of false positives, its precision is almost 100% with a sensitivity of 94%.

## Summary:
* All the models we used to predict the credit risk analysis show weak precision in determining if a credit risk is high.\
* The Ensemble models show great improvment specially on the sensitivity of the high risk credits.\
* Even though the EasyEnsembleClassifier model detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk.  It may lead to the bank losing its business opportunities.\
* Maybe there are models the bank can use to predict credit risk other than those above.
