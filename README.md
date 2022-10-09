# Credit Risk Analysis

## Overview of the Analysis
### Purpose
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. In this project, different techniques to train and evaluate models with unbalanced classes were employed using the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Specifically, using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, the data was oversampled using the RandomOverSampler and SMOTE algorithms, undersampled using the ClusterCentroids algorithm, and over- and undersampled using the SMOTEENN algorithm. Then, two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, were compared to predict credit risk.

The purpose of this analysis was to evaluate the performance of these models and make a written recommendation on whether or not they should be used to predict credit risk.

## Results
The results of the accuracy, precision, and recall scores of all six machine learning models are summarized below. For the first four machine learning models, please refer to the credit_risk_resampling.ipynb file for more details. For the last two machine learning models, please refer to the credit_risk_ensemble.ipynb file for more details.

### [RandomOverSampler](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html)
* **Accuracy Score**: 63.46%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.74

### [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)
* **Accuracy Score**: 65.83%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.63

### [ClusterCentroids](https://imbalanced-learn.org/stable/references/generated/imblearn.under_sampling.ClusterCentroids.html)
* **Accuracy Score**: 54.43%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.74

### [SMOTEENN](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html)
* **Accuracy Score**: 65.77%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.74

### [BalancedRandomForestClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html)
* **Accuracy Score**: 78.77%
* **High-Risk Precision Score**: 0.04
* **High-Risk Recall Score**: 0.67

### [EasyEnsembleClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html)
* **Accuracy Score**: 92.54%
* **High-Risk Precision Score**: 0.07
* **High-Risk Recall Score**: 0.91

## Summary
### Comparison
In summary, the EasyEnsembleClassifier model has the highest accuracy, precision, and recall scores as can be seen in the results section. This makes it the ideal model to use for this credit risk analysis project.

### Recommendation
The EasyEnsembleClassifier model would be the best to use for credit risk analysis; however, since it high-risk precision score is only 0.07, this would not be high enough for real-world use. Moreover, additional research on how to improve upon these models is required.
