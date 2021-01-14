## [1] Overview
- Detection of network traffic anomalies using unsupervised machine learning 
- Anomaly_detection.ipynb: [2]~[5]
- Analysis.ipynb: [6] Interpretation of the result 
- Generating_adversarial_samples.ipynb : [7] Generating Adversarial samples (FGSM), this notebook referred to this code (https://github.com/kenhktsui/adversarial_examples/blob/master/adversarial.py)
- Dataset link:
1) https://cloudstor.aarnet.edu.au/plus/s/Hvu7YyCDDG7ByWb
2) https://cloudstor.aarnet.edu.au/plus/s/38CH3I8HbuYkh3r

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

## [4] Hyperparameter tuning (2 examples among 6)
- Criteria of setting a threshold:  Accuracy > 0.88 and Max(TPR-FPR)

1. OCSVM + feature3

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/hp_f3_ocsvm.png)

2. Iforest + feature 3

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/f3_iforest_hp.png)

## [5] Clustering visualisation and Evaluation (2 examples among 6)

1. OCSVM + feature3

>> SCORES:

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_E_ocsvm_f3.png)

>> CLUSTERING:

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_CV_ocsvm_f3.png)

2. Iforest + feature3

>> SCORES:

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_E_iforest_f3.png)

>> CLUSTERING:

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/R_CV_iforest_f3.png)


## [6] Interpretation of the result
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/Interpretation_ocsvm_f3.png)
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/top_conversation.png?raw=true)

- Attack Timeline
![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/attack_timeline.png)


## [7] Generating Adversarial samples (FGSM)
- FGSM generates adversarial samples with the error rate of almost 100%. 

![alt text](https://github.com/kaiyoo/anomaly_detection/blob/main/imgs/FGSM.png)
