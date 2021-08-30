# Credit_Risk_Analysis

### The purpose of this analysis:
The purpose of this analysis was to apply machine learning to solve a real-world challenge: credit card risk. Due to its unbalanced problem, such as good loans can easily outnumber risky loans, we need to emply different techniques to train and evaluate models with unbalnced classes. We use inbalanced-learn and scikit-learn libraries ro buils and evaluate models using resampling. We will also used the credit card dataset from LendingClub, as we will oversample the data using the **RandomOverSample** and **SMOTE algorithm**, and undersample the data using the **ClusterCentroids algorithm**. Then we will use a combinatorial approach of over-and undersampling using the **SMOTEEN algorithm**. Next we will compare the two new machine learning models that reduce bias, **BalanceRandomForestClassifier** and **EasyEnsembleClassifer** to predict credit risk. 

### Results:

## Naive Random oversampling:
- Accuracy Score: 65.4%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 72%
- Recall Low Risk: 63%

![Challenge17_NaiveRandomOversampling](https://user-images.githubusercontent.com/83566868/131375258-bba6efdf-8df6-4e1a-8b54-7a91c445bf70.png)

## Smote Oversampling:
- Accuracy Score: 66.2%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 63%
- Recall Low Risk: 69%

![Challenge17_SMOTEOversampling](https://user-images.githubusercontent.com/83566868/131380680-2d496dfb-ba5c-41a8-ae35-02d4c786626a.png)

## Undersampling - Cluster Centroids Resampler Analysis:
- Accuracy Score: 66.7%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 72%
- Recall Low Risk: 62%

![Challenge17_Undersampling](https://user-images.githubusercontent.com/83566868/131381059-4a380987-881d-418c-a700-cbbe5f74eefd.png)

## Combination (over and under) sampling - SMOTEENN:
- Accuracy Score: 68.1%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 74%
- Recall Low Risk: 62%

![Challenge17_Smoteenn](https://user-images.githubusercontent.com/83566868/131381520-4a1be19f-3a73-447b-926f-2b6e7aa2906c.png)

## Balance Random Forest Classifier:
- Accuracy Score: 93%
- Precision High Risk: 6%
- Precision Low Risk: 100%
- Recall High Risk: 92%
- Recall Low Risk: 94%

![Challenge17_BalanceRandom](https://user-images.githubusercontent.com/83566868/131381766-9b3afc1b-925a-460a-88d7-7a245e6a2339.png)

## Easy Ensemble AdaBoost Classifier:
- Accuracy Score: 93%
- Precision High Risk: 6%
- Precision Low Risk: 100%
- Recall High Risk: 92%
- Recall Low Risk: 94%

![Challeneg17_EasyEnsemblerAdaBoost](https://user-images.githubusercontent.com/83566868/131381971-2cc4980e-0062-4f4b-9b2e-c09ecea5b1d2.png)

### Summary: 
Finding a model that allows us to detect if a loan is a high risk or not allows us to be able to analyze and detect less chances of high risk loans. After studying all different models that were used to detect the highest recall rates; the top three that scored the highest for high risk were:

1. Balance Randmon Forest Classifer
2. Easy Ensemble AdaBoost
3. SMOTEENN

While knowing the high risk rates, pulling models that allows us to see recall low risk rate loans are also just as important. Studying all models the top two that scored the  highest for low risk were:

1. Balance Randmon Forest Classifer
2. Easy Ensemble AdaBoost

Both the Easy Ensemble and Balance Random seemed to have calculated similar results, both also caluclated low precision, therefor a lot of low risk credits are not being taken into consideration, therefor the bank may be loosing opportunites. My recommnedation is if it is ultimately necessary to use a model to choose EasyEnsemble , but truly I would not recommend any model.
