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

We used the "loan status" to determine whether the application was considered "low" or "high" risk. Applications that had "current" as the "loan status" were classified as "low risk" and the remaining as "high risk". Our data set included 68,817 total applications with 68470 classified as "low risk", and 347 classified as high risk.
![Pic 1](https://github.com/schoolboycamel/Credis__risk_analysis/blob/main/Resources/1_target%20value%20balance.png)     


Using the 75/25% method to split the data for training vs. testing, 51,366 "low risk" and 246 "high risk" applications were categorized into the training set. While 17,118 "low risk" and 87 "high risk"

### Naive Random Oversampling 
