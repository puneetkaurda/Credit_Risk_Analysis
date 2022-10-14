# Credit_Risk_Analysis
## Overview
The purpose of this analysis is to evaluate three machine learning models by using resampling to determine which is better at predicting credit risk.
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, it needs to employ different techniques to train and evaluate models with unbalanced classes. This machine learning project used scikit-learn and imbalanced-learn to train and evaluate models to determine credit card risk using a credit card dataset. There were 6 different techniques used to train and evaluate models to determine credit risk: Oversampling with the RandomOverSampler and SMOTE algorithms, Undersampling with the ClusterCentroids algorithm, a combination of over and under sampling with the SMOTEENN algorithm, and two machine learning models that reduce bias - the BalancedRandomForestClassifer and EasyEnsembleClassifier.

## Results

In examining the results we will look at the Balanced Accuracy Score as well as the Imbalanced Classification Report (ICR) from each model. Here are the results from different models:
Naive Random Oversampling:

<img width="784" alt="Screen Shot 2022-10-13 at 4 18 26 PM" src="https://user-images.githubusercontent.com/107584891/195721493-e7ec051c-3fb8-4b6a-af05-057f32180afb.png">

- The balanced accuracy score was 0.6533, meaning the model predicted the credit risk accurately 65.96% of the time.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
- The recall scores for this model show that the model is better at identifying positive low-risk loans: 0.67 and decent at positively identifying high-risk loans:0.63

SMOTE Oversampling:

<img width="757" alt="Screen Shot 2022-10-13 at 4 27 38 PM" src="https://user-images.githubusercontent.com/107584891/195722443-1d3440ca-8aa5-4288-a0ac-8ed57b2c0a43.png">

- The balanced accuracy score was 0.6512, meaning the model predicted the credit risk accurately 65.12% of the time.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
- The recall scores for this model show that the model is better at identifying positive low-risk loans is 0.66 and decent at positively identifying high-risk loans: 0.64

Undersampling:

<img width="824" alt="Screen Shot 2022-10-13 at 5 03 15 PM" src="https://user-images.githubusercontent.com/107584891/195726207-0d868a50-60d9-4ccf-ad7a-db2a2debaace.png">

- The balanced accuracy score was 0.5103, meaning the model predicted the credit risk accurately 51.03% of the time.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted. This model is not great for identifying high-risk loans.
- The recall scores for the high-risk loans were around 0.59 and the recall scores for low-risk loans were around 0.43. While the high-risk recall is much better, both recall scores are low and show that many of the positives were not accurately predicted.

Combination (Over and Under) Sampling (SMOTEENN):

<img width="813" alt="Screen Shot 2022-10-13 at 5 35 53 PM" src="https://user-images.githubusercontent.com/107584891/195730224-37a706ee-e852-49bf-b34e-026427fa0aed.png">

- The balanced accuracy score for the undersampling technique was around 0.6429, meaning that only 64.29% of the testing data was accurately classified.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted.
- The high-risk recall score for this model is fairly high at 0.69 and the low-risk recall score is average at 0.60. Compared to the previous techniques, this model is much better at identifying true high-risk loans.

Balanced Random Forest Classifier:

<img width="751" alt="Screen Shot 2022-10-13 at 5 37 31 PM" src="https://user-images.githubusercontent.com/107584891/195730405-630d861c-aac7-45c1-bc8b-73774b09fc46.png">

- The balanced accuracy score for this model is comparatively high at 0.7885, meaning that 78.85% of the testing credit data was accurately classified.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted.
- The recall score for low-risk loans is very high at 0.87 and the recall score for high-risk loans is fairly high at 0.70. This shows that the classifier is good at predicting true positives for low-risk loans.

Easy Ensemble AdaBoost Classifier:

<img width="846" alt="Screen Shot 2022-10-13 at 5 38 27 PM" src="https://user-images.githubusercontent.com/107584891/195730495-d32211ee-d024-4a92-aa9f-e6622d511e2a.png">


- The balanced accuracy score for this model was 0.9316, meaning the model was accurate 93.16% of the time.
- The precision scores for this model are very skewed toward the low-risk loans as all of the low-risk loans were correctly predicted, but nearly none of the high-risk loans were accurately predicted.
- The recall score was high for both low and high risk loans: 0.94 for high risk and 0.92 for low risk.

## Summary

All of the machine learning models had low precision scores for the high-risk loans in accurately predicting positives. The balanced accuracy score for the models completed varied with the lowest score for the undersampling method and a high score with Easy Ensemble Classifier. Recall scores also varied between models with the lowest scores for undersampling and highest with the classifying methods. Of the models created, the Easy Ensemble Classifier would be the best model to use to predict credit risk due to the high recall scores for both high and low risk loans, as well as an accuracy score of 93.16%. The precision for this model is still very off, indicating that the positives are not necessarily accurate, and so this model could be much improved before being put into use.
In conclusion, credit-risk is a difficult thing to predict, even for advanced machine learning algorithms with 93 columns of data to process. While the Easy Ensemble AdaBoost Classifier model had the highest overall accuracy, this was largely due to the fact that the dataset was so radically unbalanced.  In the end, I would advise against using any of these algorithms, as it would put creditors as too great of risk being unable to accurately predict who the high-risk clients/debtors would be.


