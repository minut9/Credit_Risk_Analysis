# Credit_Risk_Analysis
## Purpose
The purpose of this analysis is to use Machine Learning to determine risks of applicates from a data set from LendingClub. This project is classified as “Supervied Learning” because the data includes labeled outcomes. To complete the analysis, adjustments to balance the unbalanced classifications from the given data set were made for more accurate predictions for higher accuracy scores. 

### Tools/Machine Learning Algorithms 
* RandomOverSampler
*	SMOTE
*	ClusterCentroids
*	SMOTEENN
*	BalancedRandomForestClassifier
* EasyEnsembleClassifier

## Results
Originally, the dataset had over 100,000 loan applicants in Q1 2019. After using the loan status to determine if the application was considered "high" or "low" risk, the applicants who were classified as "current" or "loan status" were classified as "low risk", meaning the rest of the data was "high risk". By cleaning the data, this reduced the dataset to 68470 with nearly all applicants classified to "low risk"(99%).

<img width="378" alt="init balance of target values" src="https://user-images.githubusercontent.com/86068655/156027559-46083f97-864d-418e-99c7-614875270551.png">

### <u>OverSampling
#### RandomeOverSampler Model
RandomeOverSampler Model found a balanced accuracy score of 64%

<img width="484" alt="Naive Random Oversampling" src="https://user-images.githubusercontent.com/86068655/156044506-f9448b0d-5b1f-4a71-aa4c-1526a118d95c.png">

<img width="393" alt="Naive Risk" src="https://user-images.githubusercontent.com/86068655/156044647-8b4dc849-90a9-4452-90a0-bdbfae50997e.png">

  * The high risk precision rate was 1% with a recall of 66%, which gave this result of an F1 score of 2%. 
  * The low risk had a precision of 100% and the recall was at 62%.

<img width="718" alt="Naive Oversampling report" src="https://user-images.githubusercontent.com/86068655/156044660-5f85483c-9010-4ba1-b8e1-7a0ba9f9d958.png">

#### SMOTE (Synthetic Minority Oversampling Technique)
The SMOTE algorithm had a balanced accuracy score of 65.8% which is somewhat better than the previous model.

<img width="395" alt="Smote" src="https://user-images.githubusercontent.com/86068655/156045267-b7a7a5bd-4a7a-453d-9b40-9e6c3eb9a00a.png">

  * The high risk precision, again, was only 1% but the recall dropped slightly to 62%
  * The low risk still had a precision of 100% but improved the recall score to 69%.
  * 
<img width="381" alt="Smote risk" src="https://user-images.githubusercontent.com/86068655/156045516-abfc7d1c-96df-4460-a987-c6c34da95baa.png">

<img width="710" alt="Smote report" src="https://user-images.githubusercontent.com/86068655/156045552-2de1a520-a0a6-48f4-84e7-6c5c0052d5b9.png">

### UnderSampling
#### Cluster Centroids algorithm
This algorithms balanced score was lower than the oversamplings scores at 54.4%

<img width="398" alt="CC Balanced" src="https://user-images.githubusercontent.com/86068655/156046271-3a6443ec-d7da-4437-92a8-8eb775259362.png">

  * The high risk precision rate was at 1% and the recall at 69%. The F1 score was 1%.
  * The low risk model had a precision rate of 100% with a low recall rate of 40% compared to the oversampling models.

<img width="391" alt="CC risk" src="https://user-images.githubusercontent.com/86068655/156046476-560c01de-bffe-4304-b70f-8d3996dda0b9.png">

<img width="716" alt="CC report" src="https://user-images.githubusercontent.com/86068655/156046494-6490d365-9b82-4b60-b67a-162f76d4b39c.png">

### Combination Sampling
#### SMOTEENN
(Synthetic Minority Oversampling Technique + Edited Nearest Neighbors) or SMOTEENN had a balanced accuracy score with was 64.8%

<img width="398" alt="SMOTEENN balance" src="https://user-images.githubusercontent.com/86068655/156047354-2fd84abc-6396-4407-8869-d79a4ba32f90.png">

  * The high risk precision rate was 1% and the precision rate was a 72%, which brought the F1 score to 2%.
  * The low risk was still 100%, but with a recall at 57%.

<img width="378" alt="SMOTEENN risk" src="https://user-images.githubusercontent.com/86068655/156047610-79ff755b-73d8-48f5-a57c-5ab0e52af369.png">

<img width="722" alt="SMOTEENN report" src="https://user-images.githubusercontent.com/86068655/156047627-46793261-c25f-4fa7-9514-64f951342bb9.png">


### Ensemble Classifiers to Predict Credit Risk
#### BalancedRandomForestClassifier 
This algorithm brought the balanced accuracy score to 78.8%.

<img width="566" alt="Balanced Random Forrest Classifiier" src="https://user-images.githubusercontent.com/86068655/156047905-2ca89e3b-f3a9-446c-9b94-3313d4b374e4.png">

  * The high risk precision rate increased to 3% with the recall at 70% to give the F1 score of 6%.
  * The low risk still had a precision score of 100% but a high recall of 87%.

<img width="371" alt="Forrest Classifier risk" src="https://user-images.githubusercontent.com/86068655/156048240-3a4e634e-7bc6-44f7-8383-d2dc834813d8.png">

<img width="720" alt="Forrest classifier report" src="https://user-images.githubusercontent.com/86068655/156048254-835d419f-0ce9-4269-8296-ee25c450c826.png">


#### EasyEnsembleClassifier Model
This algorithm had the best algorithm score of 93.1%.

<img width="390" alt="Easy Ensemble AdaBoost Classifier" src="https://user-images.githubusercontent.com/86068655/156048486-45cbc42b-3bd5-4d52-b739-a2b46cf47d69.png">

  * The high risk precision rate increased to 9% and the recall increased to 92% wiht the highest F1 score of 16%.
  * The low risk precision rate was still 100% but the recall jumped to 94%.

<img width="388" alt="Easy Esemble risk" src="https://user-images.githubusercontent.com/86068655/156048700-93b8cbca-a130-4db0-9587-d122103add46.png">

<img width="716" alt="Easy Ensemble report" src="https://user-images.githubusercontent.com/86068655/156048715-37ba9023-1432-4b6b-8418-3f2c59969836.png">


## Summary
After reviewing the results, it was clear that the EasyEnsembleClassifier Model had the best results with an accuracy score of 93.1 and a precision rate of 9% when predicitng high risk applicants. The recall rate was also the highest at 92% for high risk applicants as well as low risk applicants, 94%. This model is clearly the best model to choose because it has the best algorithm to assess credit risks when lending to applicants. 


