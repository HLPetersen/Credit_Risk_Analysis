# Credit Risk Analysis

## Overview of the analysis ##

This is an analysis of credit risk. The csv file is a credit card dataset from LendingClub. It contained 145 pieces of information on 115,775 different loans. Some of the information includes loan, amount, term, interest rate, employment length, income, and so on. The dataset was cleaned and converted to numeric values besides the target feature of low and high risk, and split into testing and training datasets. 

### Purpose of Analysis ###

Credit risk is an unbalanced classification problem, so the purpose of this analysis is to train and evaluate different models to find the model that would best fit the data and predict future risk. 

## Results ##  

### Naive Random Oversampling ###
 <img width="300" alt="CM Random Oversampler AS" src="https://user-images.githubusercontent.com/116980760/225498080-82f7e24e-bee3-4761-9ad6-7b3e0acb0877.PNG"><img width="201" alt="Naive" src="https://user-images.githubusercontent.com/116980760/225499342-ceda4e25-a4d6-4eb4-9e06-ad46697868d7.PNG">
 <img width="300" alt="Random Oversampler AS" src="https://user-images.githubusercontent.com/116980760/225490443-f5fcbc70-e8fe-4c01-9f67-5a0dc4c2fc17.PNG">

- Balanced Accuracy Score : 64.1%
 
- Precision: 99% 
Quality of positive predictions. True positive/total predicted positive
- Recall Score: 68%

### SMOTE Oversampling ###
<img width="300" alt="CM SMOTE AS" src="https://user-images.githubusercontent.com/116980760/225498498-84568c6b-18db-4504-8056-df85fd1fc343.PNG"> <img width="201" alt="smote" src="https://user-images.githubusercontent.com/116980760/225502059-84b4fc6f-349d-441a-9e5f-7081c2206382.PNG"> <img width="300" alt="SMOTE AS" src="https://user-images.githubusercontent.com/116980760/225490481-08ea1f23-3af7-435b-a805-6a9228283b32.PNG">

- Balanced Accuracy Score: 63.7%
- Precision: 99%
- Recall: 68%

### Cluster Centroids Resampler ###
<img width="300" alt="CM ClusterCentroids  AS" src="https://user-images.githubusercontent.com/116980760/225502124-cee9c4e5-dc7b-404c-9c57-49190ed11a10.PNG"><img width="200" alt="CC" src="https://user-images.githubusercontent.com/116980760/225502171-e0f02ef1-f374-47da-b36e-5a75a344e0a1.PNG"> <img width="300" alt="ClusterCentroids  AS" src="https://user-images.githubusercontent.com/116980760/225490374-db110009-9f51-4ee7-ac00-1297aa1113d1.PNG">

- Balanced Accuracy Score: 52.9%
- Precision: 99%
- Recall: 44% 

### SMOTEENN Resampling ###
<img width="300" alt="CM smoteeenn AS" src="https://user-images.githubusercontent.com/116980760/225502304-ecdc1cfb-a8f1-4c46-bab3-3e9865d79a7d.PNG"><img width="200" alt="smoteeemmnnnn" src="https://user-images.githubusercontent.com/116980760/225502251-1b864e3f-1214-42d4-803c-cda8f594259d.PNG"> <img width="300" alt="smoteeenn AS" src="https://user-images.githubusercontent.com/116980760/225490355-7a56d5e3-7537-4dc5-aefa-22d78463bc70.PNG">

- Balanced Accuracy Score: 63.9%
- Precision: 99%
- Recall: 58%

### Balanced Random Forest Classifier ###

<img width="300" alt="CM BalancedRandomForestClassifier AS" src="https://user-images.githubusercontent.com/116980760/225499843-c9bc1072-3b8c-4306-9e14-2d4ca84d4e1d.PNG"><img width="200" alt="forest" src="https://user-images.githubusercontent.com/116980760/225502366-22633cb5-6e57-4596-adf5-3c3052f74af1.PNG"> <img width="300" alt="BalancedRandomForestClassifier AS" src="https://user-images.githubusercontent.com/116980760/225490328-1c5785b6-70db-4d97-a39f-20694246e6a4.PNG">

- Balanced Accuracy Score: 78.8%
- Precision: 99%
- Recall: 91% 

### Easy Ensemble Classifier ###
<img width="300" alt="CM EasyEnsembleClassifier AS" src="https://user-images.githubusercontent.com/116980760/225499972-3301887f-fe84-4095-b153-e79f5fa00e8e.PNG"> <img width="200" alt="easy" src="https://user-images.githubusercontent.com/116980760/225502412-c7a453c5-51ac-495c-93d0-12c37494ab4b.PNG"> <img width="300" alt="EasyEnsembleClassifier AS" src="https://user-images.githubusercontent.com/116980760/225490412-1d840065-86d6-4389-8d85-fa21e3f28fbc.PNG">

- Balanced Accuracy Score: 92.5%
- Precision: 99%
- Recall: 94%

## Summary ##
- Most models had comparable precision.
- The ensemble classifiers had the highest recall.
- The model with highest accuracy also had the highest precision and recall. 
- The model that performed best in classifying risk was the easy ensemble classifier.
- With the ensemble classifier, 979 loans were identified as high risk that were actually low risk, but only 8 were identified as low risk that were actually high risk. If the goal is to minimize the giving out high risk loans, this classifier would be recommended. 
