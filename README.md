# Credit_Risk_Analysis
Employ Machine Learning to Solve Credit risk 

## Overview

This analysis involves in the incorporation of Machine Learning statistical algorithms that allows us to make predictions based on data patterns. The purpose of this challenge was to focus on **Supervised Learning** using a dataset from **LendingClub** in order to evaluate and predict credit risk, as these loans have a problem of **unbalanced classification**

Different `Machine Learning` techniques are implemented in order to train and evaluate the data with unbalanced classes. The dataset from the **LendingClub** has an unbalanced classification problem due to the number of good loans outweighing the amount of risky loans. We balanced out the classifications to allow for more meaningful predictions and improved the accuracy score, we essentially employed various `Machine Learning` techniques in order to populate (resample) the data, as the two existing classes (risky and nonrisky) in the datset are not equally represented.  These strategies include `RandomOverSampler`, `SMOTE`, `ClusterCentroids`, `SMOTEENN`, `BalancedRandomForestClassifier`, and `EasyEnsembleClassifier`.


## Libraries and Algorithms
- scikit-learn
- imbalanced-learn 
- RandomOverSampler
- SMOTE algorithms
- ClusterCentroids algorithm
- SMOTEENN algorithm
- BalancedRandomForestClassifier (bias reduction model)
- EasyEnsembleClassifier (bias reduction model)


## Results


# Deliverable 1: Use Resampling Models to Predict Credit Risk

We used the "loan status" to determine whether the application was considered "low" or "high" risk. Applications that had "current" as the "loan status" were classified as "low risk" and the remaining as "high risk". Our data set included 68,817 total applications with 68470 classified as "low risk", and 347 classified as high risk.
![Pic 1](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/1_target%20value%20balance.png)     


Using the 75/25% method to split the data for training vs. testing, 51,366 "low risk" and 246 "high risk" applications were categorized into the training set. While 17,118 "low risk" and 87 "high risk"
![Pic 2](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/2_train_test_split.png)

### Naive Random Oversampling 

![Pic 3](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/naive_random_oversampling.png)
- We used RandomOverSampler Model to randomly select from the minority class and populate it to the training set until both classifications are equal. The results classified 51,366 records each as High Risk and Low Risk.
- Our balanced accuracy score came to 65%
- The "High Risk" precision rate was only 1% with the recall at 59% giving this model an F1 score of 1%.
- "Low Risk" had a precision rate of 100% and recall at 43%.

### SMOTE Oversampling 

![Pic 4](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/SMOTE_oversampling.png)
- We used SMOTE which increases the size of the minority class by creating new values based on the value of the closest neighbors to the minority class instead of random selection
- Our balanced accuracy score came to 51%
- The "High Risk" precision rate was only 1% with the recall at 59% giving this model an F1 score of 1%.
- "Low Risk" had a precision rate of 100% and recall at 43%.

### Cluster Centroids Undersampling
<img width="894" alt="image" src="https://user-images.githubusercontent.com/98793962/175838190-de94fce4-9676-44ed-811d-436f4866ea57.png">
- We used the ClusterCentroids algorithm in order to identify clusters of the majority class that woudl generate synthetic data points that are representative of the clusters. The model classified 246 high risk an low risk loans.
- Balanced accuracy score came out to 65% 
- The "High Risk" precision rate was only 1% with the recall at 63% giving this model an F1 score of 2%.
- "Low Risk" had a precision rate of 100% and recall at 67%.

Deliverable 2: Use the SMOTEENN algorithm to Predict Credit Risk

### Combination (Over and Under) Sampling (SMOTEENN)

![Pic 5](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/SMOTEN.png)
-SMOTEENN (Synthetic Minority Oversampling Technique + Edited NearestNeighbors) Model combines aspects of both oversampling and undersampling. The model classified 68,460 records as High Risk and 62,011 as Low Risk.
- Balanced accuracy score came out to 63% 
- The "High Risk" precision rate was 1% with the recall at 70% giving this model an F1 score of 2%.
-  "Low Risk" had a precision rate of 99% and recall at 57%.

# Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

## RandomForest

![Pic 6](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/random_forest.png)

- We used BalancedRandomForestClassifier Model, where two trees of the same size and equal size to the minority class are constructed to represent one for the majority class and one for the minority class.
- balanced accuaracy score increased to 67%
-  The "High Risk" precision rate was of 73% with the recall at 43% giving this model an F1 score of 47%.
- "Low Risk" had a precision rate of 100% and recall at 100%.

![Pic 7](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/sorted_features.png)
- features sorted by importance 

## EasyEnsembleClassifier Model

![Pic 7](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/easy_ensemble.png)

- Balanced accuracy scores increased to 92%
- The "High Risk" precision rate was of 7% with the recall at 91% giving this model an F1 score of 14%.
- "Low Risk" had a precision rate of 100% and recall at 94%.


# Conclusion

In reviewing all six models, the EasyEnsembleClassifer model yielded the best results with an accuracy rate of 92 and a 7% precision rate when predicting "High Risk candidates. The sensitivity rate was also the highest at 91% compared to the other models. The result for predicting "Low Risk" was also the highest with the sensitivity rate at 100% and an F1 score of 14%. Therefore, if a model needed to be recommended to perform this type of analysis would bt EastEnsembleClassifier






