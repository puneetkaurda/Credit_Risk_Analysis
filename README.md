# Credit_Risk_Analysis
## Overview
The purpose of this analysis is to evaluate three machine learning models by using resampling to determine which is better at predicting credit risk.
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, it needs to employ different techniques to train and evaluate models with unbalanced classes. This machine learning project used scikit-learn and imbalanced-learn to train and evaluate models to determine credit card risk using a credit card dataset. There were 6 different techniques used to train and evaluate models to determine credit risk: Oversampling with the RandomOverSampler and SMOTE algorithms, Undersampling with the ClusterCentroids algorithm, a combination of over and under sampling with the SMOTEENN algorithm, and two machine learning models that reduce bias - the BalancedRandomForestClassifer and EasyEnsembleClassifier.

## Results

Naive Random Oversampling:

<img width="784" alt="Screen Shot 2022-10-13 at 4 18 26 PM" src="https://user-images.githubusercontent.com/107584891/195721493-e7ec051c-3fb8-4b6a-af05-057f32180afb.png">
-The balanced accuracy score was 0.6533, meaning the model predicted the credit risk accurately 65.96% of the time.
-The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
-The recall scores for this model show that the model is better at identifying positive low-risk loans (0.67) and decent at positively identifying high-risk loans (0.63)

SMOTE Oversampling:


- The balanced accuracy score was 0.6533, meaning the model predicted the credit risk accurately 65.33% of the time.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
- The recall scores for this model show that the model is better at identifying positive low-risk loans (0.67) and decent at positively identifying high-risk loans (0.63)


