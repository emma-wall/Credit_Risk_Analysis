# Credit Risk Analysis

## Overview

This repo uses supervised machine learning to predict credit risk for loans. It evaluates six different models. 

The target variable is loan status, given over 80 various metrics, we want to be able to predict if an applicant will be low or high risk. Looking at the dataset, there is an imbalance with the number of low and high risk cases: low risk - 68,470, high risk - 347. Since there are so many more low risk cases, this might throw off the models, which is why i tried over and under sampling models. 

## Results 

### Random Oversampling 
Accuracy Score: 0.6403

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 67 | 34 |
|Actually False | 6,546 | 10,558 | 

![Random Oversampling](https://user-images.githubusercontent.com/80648379/129507384-c1fb82ff-e124-4010-9b4f-08cb57b2324f.png)


* The accuracy score is 0.64, which means the model predicts the correct classification 64% of the time. 
* The precision is very low for predicting high risk and we can see that there is a large number of false positives, which means the model is unreliable for positive classifications.
* The precision is extremely high for detecting low-risk
* The recall for both high and low risk are similar with scores of 0.62 and 0.66 respectively
* F1 score is very low for high risk and high for low risk, which means the model is good at predicting low risk cases, but not high risk
* Overall, this model is fairly good at predicting low-risk loans, however that might not be very helpful for companies, as they want to be able to identify high risk. 


### SMOTE
Accuracy Score: 0.6515

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 62 | 39 |
|Actually False | 5,317 | 11,787 | 

![SMOTE Oversampling](https://user-images.githubusercontent.com/80648379/129507368-df8aa965-49fa-4f8f-81e0-ffc7e042b53a.png)


* The accuracy score is 0.65, which indicates for overall accuracy, this model is slightly better than the Random Oversampling one. 
* The SMOTE model is very similar to the Random Oversampling model. 
* The recall and F1 score are both a little higher for low risk than the previous model, indicating that the model is better at predicting low risk, which in our case does not help
* When evaluating the model as a whole, it is still not a good predictor for our data. 


### Cluster Centroid Undersampling 
Accuracy Score: 0.5447

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 70 | 31 |
|Actually False | 10,325 | 6,779 | 

![Undersampling](https://user-images.githubusercontent.com/80648379/129507400-77747593-f739-4276-b28d-4a154767cb4e.png)


* In this under sampling model, the accuracy is lower than in the other oversampling models, with a score of 0.54
* The precision scores for the model are the same as the above models.
* The recall for high risk is 0.69, which means that high risk cases are more likely to get flagged as high risk than the other models. 
* The F1 score for high risk is extremely low at 0.01. 
* Even though this model has a higher recall for high risk, it is still not a good model, because there are a high number of false negatives. 




### SMOTEEN
Accuracy Score: 0.6551

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 76 | 25 |
|Actually False | 7,566 | 9,538 | 

![SMOTEEN](https://user-images.githubusercontent.com/80648379/129507410-93dbb259-c4d5-42da-8818-ce37469c53ca.png)


* The accuracy score for the SMOTEEN model around the accuracy score for the oversampling models
* The precision scores are the same as all the previous models, so the model is still not good at predicting positive classifications
* The recall for high risk is 0.75, the best we’ve seen thus far. Recall for low risk cases is okay. 
* The F1 scores for this model are similar to the past models.



### Balanced Random Forest Classifier
Accuracy Score: 0.7885

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 71 | 30 |
|Actually False | 2,153 | 14,951 | 

![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/80648379/129507428-53ec6bc3-717b-418e-8e8a-c8402e70939b.png)


* The accuracy score for this model is 0.79 which means that it correctly predicted classifications almost 80% of the time. 
* The precision score is still relatively low with 0.03. 
* The recall for high risk is 0.7 which is pretty high and the recall for low risk is 0.87. This means that the high risk and low risk cases are likely to get classified correctly. 
* The F1 score for high risk is still pretty low. 
* Overall this model is a decent model for identifying high risk cases. 


### Easy Ensemble Classifier
Accuracy Score: 0.9317

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 93 | 8 |
|Actually False | 983 | 16,121 | 

![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/80648379/129507448-28ebc885-8766-45b9-8e3c-cf48d64d2709.png)


* Looking at overall accuracy, this model is the best with an accuracy score of 0.93
* The precision score is still low, although it is the highest out of all the models. 
* The recall score for high risk is 0.92 and for low risk is 0.94, meaning most cases for both high and low risk are being correctly classified. 
* Although the F1 score is still low for high risk, it is the largest one out of all the other models. 
* Given the accuracy score, as well as the high recall for both high and low risk, we can say this is a good model. 

## Summary
