# Credit Risk Analysis

## Overview

This repo uses supervised machine learning to predict credit risk for loans. It evaluates six different models. 

## Results 

### Random Oversampling 
Accuracy Score: 0.6403

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 67 | 34 |
|Actually False | 6,546 | 10,558 | 

![Random Oversampling](https://user-images.githubusercontent.com/80648379/129507384-c1fb82ff-e124-4010-9b4f-08cb57b2324f.png)




### SMOTE
Accuracy Score: 0.6515

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 62 | 39 |
|Actually False | 5,317 | 11,787 | 

![SMOTE Oversampling](https://user-images.githubusercontent.com/80648379/129507368-df8aa965-49fa-4f8f-81e0-ffc7e042b53a.png)



### Cluster Centroid Undersampling 
Accuracy Score: 0.5447

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 70 | 31 |
|Actually False | 10,325 | 6,779 | 

![Undersampling](https://user-images.githubusercontent.com/80648379/129507400-77747593-f739-4276-b28d-4a154767cb4e.png)



### SMOTEEN
Accuracy Score: 0.6551

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 76 | 25 |
|Actually False | 7,566 | 9,538 | 

![SMOTEEN](https://user-images.githubusercontent.com/80648379/129507410-93dbb259-c4d5-42da-8818-ce37469c53ca.png)



### Balanced Random Forest Classifier
Accuracy Score: 0.7885

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 71 | 30 |
|Actually False | 2,153 | 14,951 | 

![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/80648379/129507428-53ec6bc3-717b-418e-8e8a-c8402e70939b.png)



### Easy Ensemble Classifier
Accuracy Score: 0.9317

|.  | Predicted True | Predicted False
|---|---|---|
|Actually True | 93 | 8 |
|Actually False | 983 | 16,121 | 

![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/80648379/129507448-28ebc885-8766-45b9-8e3c-cf48d64d2709.png)




## Summary
