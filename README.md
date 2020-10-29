## [1] Overview
Detection of network traffic anomalies using unsupervised machine learning 

## [2] Features
- Feature1:
Numeric value (existing + newly generated) + Standardscaler + PCA

- Feature2:
Feature1 + One-hot encoded categorical feature

- Feature3:
Scale (Cumulative features grouped by stream_id + time-based feature) + PCA


## [3] Model
1. Iforest
2. OneclassSVM

## [4] Hyperparameter tuning
>> just two examples among 6 combinations, 
1. OCSVM + feature3
![alt text](https://drive.google.com/file/d/1NprTcGeSJ7H5z2QPSyrB6vKWsA-4aVI9/view)

2. Iforest + feature 3


## [5] Clustering visualisation and Evaluation
>> just two examples among 6 combinations, 
1. OCSVM + feature3
![alt text](https://github.com/kaiyoo/Traffic-Map-App/blob/master/desktopview.PNG?raw=true)

2. Iforest + feature 3


## [6] Generating Adversarial samples (FGSM)
FGSM generates adversarial samples with the error rate of almost 100%. 
