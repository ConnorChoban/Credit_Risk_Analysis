# Credit_Risk_Analysis

## Overview

The purpose of this analysis is to determine which machine learning algorithm is the most effective to evaluate our credit card credit dataset so that we can better predict credit risk. We'll look at factors such as the accuracy score, precision score, and the recall score to determine which method is the best for predicting high risk loans. 

## Results

### Random Over Sampler

- Accuracy Score: 64.56%
- Precision Score: 1%
- Recall Score: 61%

<img width="912" alt="Screen Shot 2022-06-27 at 11 33 33 PM" src="https://user-images.githubusercontent.com/99847786/176086497-275c49bb-7e95-4707-af64-fe90f04492e3.png">


### SMOTE

- Accuracy Score: 62.34%
- Precision Score: 1%
- Recall Score: 61%

<img width="913" alt="Screen Shot 2022-06-27 at 11 33 48 PM" src="https://user-images.githubusercontent.com/99847786/176086756-79a78f53-681c-4b72-b9fd-6c23b4f0429d.png">

### Cluster Centroids

- Accuracy Score: 51.08%
- Precision Score: 1%
- Recall Score: 57% 

<img width="898" alt="Screen Shot 2022-06-27 at 11 34 02 PM" src="https://user-images.githubusercontent.com/99847786/176086780-de529575-297b-42e5-b499-c3a91e285406.png">


### SMOTEENN

- Accuracy Score: 63.96%
- Precision Score: 1%
- Recall Score: 70%

<img width="926" alt="Screen Shot 2022-06-27 at 11 34 16 PM" src="https://user-images.githubusercontent.com/99847786/176086541-161ec03d-af54-4550-a0b4-08e4be49657f.png">

### Balanced Random Forest Classifier


- Accuracy Score: 78.77%
- Precision Score: 7%
- Recall Score: 91%

<img width="910" alt="Screen Shot 2022-06-27 at 11 17 11 PM" src="https://user-images.githubusercontent.com/99847786/176084591-696ca612-8416-4c81-abcb-ba0c5bb75358.png">


### Easy Ensemble Classifier

- Accuracy Score: 92.54%
- Precision Score: 7%
- Recall Score: 91%

<img width="910" alt="Screen Shot 2022-06-27 at 11 17 28 PM" src="https://user-images.githubusercontent.com/99847786/176084598-8dbbaf5d-9c23-4c3d-9242-4eb0de016b6c.png">



## Summary

The first four methods we used - Random Oversampling, SMOTE, Cluster Centroids and SMOTEENN - had accuracy scores ranging from 51.08% to 64.56%, whereas the last two methods - the Balanced Random Forest Classifier and Easy Ensemble classifier - were much more accurate, with scores of 78.77% and 92.54% respectively. 

In terms of precision, the first four methods all had a score of just 1%, meaning that out of 100 loans deemed to be high risk, only 1 was actually high risk. The precision score was significantly improved using the Balanced Random Forest Classifier at 7%, and by just as much using the Easy Ensemble Classifier, also with a score of 7%. However, at just 7 percent, the precision score is still very low. We could potentially get a higher score by using a larger dataset with more instances of defaulted or high risk loans.

Finally, the recall score (also known as Sensitivity) for the first four methods ranged from to 57% to 70%, whereas the recall score for both the Balanced Random Forest Classifier and the Easy Ensemble Classifier was 91%. This means that out of 100 defaulted loans, anywhere from 57 to 91 were  correctly classified by the machine learning algorithm. 

After examining the csv file used to create the dataset, I noticed one thing. Out of 115,675 records, only 293 loans in the loan_status column were considered late (0.25%). I believe the algorithm is underperforming due to a lack of data regarding high risk loans. As such, I would advise running the various machine learning models on a dataset that has more in-depth information regarding defaulted loans. We need a dataset that has more instances of high risk loans in comparison to low risk loans. And of these models, I would advise using either the Easy Ensemble Classifier or Balanced Random Forest Classifier since in this exercise, they produced the most accurate, precise, and sensitive results. 

