Overview

This repository contains python script that uses machine learning to train and evaluate a logisitc regression model evaluating loan risk. The goal of the analysis is to develop and train a model that predicts high-risk loans as part of an assessment of borrowers' creditworthiness. 

The dataset used to complete the analysis contains datapoints on loan size, interest rate, borrower income, DTI ratio , number of open credit accounts, derogatory marks on credit report, total debt, and loan status for over 5,000 unique loan profiles. After data cleaning (removing duplicates, etc.), loan status was isolated as the target variable for which predictions were performed using logistic regression. All other data categories were included as features within the model. 

When building the model, 75% of the data was allocated to training while 25% was split for model testing. Due to different numerical ranges in the dataset, the data was scaled using StandardScaler from SKLearn. Using SKLearn, a logistic regression model was created, trained, and tested. After running this first model, a second model was created following the application of Imbalanced-Learn's RandomOverSampler module to rebalance the sampling (underlying data is imbalanced). This second model was then trained and tested.


Results
First Model (Before Sampling Rebalance): Balanced accuracy of 93.2%. Class precision, recall, f1-score, and support metrics below along with explanation. 
![image](https://user-images.githubusercontent.com/119253324/236711108-043ecf2a-16e4-44af-b79b-755ae46f304a.png)

![image](https://user-images.githubusercontent.com/119253324/236711134-36bb3d0e-30b9-4908-8e79-2738efc2bbfd.png)



Second Model (Post Sampling Rebalance): Balanced accuracy of 93.8%. Class precision, recall, f1-score, and support metrics below along with explanation.
![image](https://user-images.githubusercontent.com/119253324/236711157-3c165817-1c49-4bef-a2fb-fe0ff95dff32.png)

![image](https://user-images.githubusercontent.com/119253324/236711167-a85407a7-62da-42ae-8c2f-c011ffc17913.png)



Summary:
The second model exhibited a higher level of performance and notably improved the model's performance in correctly identifying high-risk loans, which is key to our analysis. 
