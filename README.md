## [1] Overview
- Detection of network traffic anomalies using unsupervised machine learning 

## [2] Features
>> More details in the anomaly_detection_reports.pdf
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
- Criteria of setting a threshold:

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/threshold.png?raw=true)

>> just two examples among 6 combinations, 
1. OCSVM + feature3

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/hp_f3_ocsvm.png?raw=true)

2. Iforest + feature 3

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/f3_iforest_hp.png?raw=true)

## [5] Clustering visualisation and Evaluation
>> just two examples among 6 combinations:
1. OCSVM + feature3

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_E_ocsvm_f3.png?raw=true)
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_CV_ocsvm_f3.png?raw=true)

2. Iforest + feature 3

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_E_iforest_f3.png?raw=true)
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_CV_iforest_f3.png?raw=true)


## [6] Interpretation of the result
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/FGSM.png?raw=true)
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/top_conversation.png?raw=true)

- Attack Timeline
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/attack_timeline.png?raw=true)


## [7] Generating Adversarial samples (FGSM)
- FGSM generates adversarial samples with the error rate of almost 100%. 
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/FGSM.png?raw=true)
