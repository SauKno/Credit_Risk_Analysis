# Credit_Risk_Analysis
## Overview of the Analysis
In this project, Python was used to build and evaluate several machine learning lodesl to predict credit risk. The following procedures were used:
1. Oversample the data using the **RandomOverSampler** and **SMOTE** algorithms.
2. Undersample the data using the **ClusterCentroids** algorithm.
3. Use the **SMOTEENN** algorithm, an approach that uses over and undersampling
4. Reduce bias by comparing two machine learning models: **BalancedRandomForestClassifier** and **EasyEnsembleClassifier**.

Through the evaluation of the performance of these models, the results will determine if these models should be used to predict credit risk. 

## Results
**RandomOverSampler Model**
<img width="1089" alt="Screen Shot 2022-04-17 at 2 08 07 PM" src="https://user-images.githubusercontent.com/94129215/163726993-ae7398c6-9547-47e5-80ac-fd6cdf397f1d.png">

Balanced Accuracy Score: 64.6%
High_Risk Precision: 1%
High_Risk Sensitivity: 68%
High_Risk F1: 2%

Low_Risk Precision: 100% (Due to the high number of low_risk population)
Low_Risk Sensitivity: 62%

**SMOTE Model**
<img width="1087" alt="Screen Shot 2022-04-17 at 2 10 43 PM" src="https://user-images.githubusercontent.com/94129215/163727066-2e77e3d5-ace7-40b3-95bb-d30783a99d0f.png">

These results are similar to the RandomOverSampler Model. 
Balanced Accuracy Score: 62.3%
High_Risk Precision: 1%
High_Risk Sensitivity: 64%
High_Risk F1: 2%

Low_Risk Precision: 100% (Due to the high number of low_risk population)
Low_Risk Sensitivity: 61%

**ClusterCentroids Model**
<img width="1066" alt="Screen Shot 2022-04-17 at 2 12 35 PM" src="https://user-images.githubusercontent.com/94129215/163727127-39b63adb-f7cd-4d68-8dad-0c66f4823140.png">

In this model, the balanced accuracy score drops, high risk sensitivity drops, and Low-Risk sensitivity increases. 
Balanced Accuracy Score: 51.3%
High_Risk Precision: 1%
High_Risk Sensitivity: 40% (Due to the high number of false positives)
High_Risk F1: 1%

Low_Risk Precision: 100% (Due to the high number of low_risk population)
Low_Risk Sensitivity: 59%

**SMOTEENN Model**
<img width="1121" alt="Screen Shot 2022-04-17 at 2 13 36 PM" src="https://user-images.githubusercontent.com/94129215/163727159-c4e17eac-2883-414d-8ef0-48fd644e74b6.png">

Balanced Accuracy Score: 61.6%
High_Risk Precision: 1%
High_Risk Sensitivity: 54% (Due to the high number of false positives)
High_Risk F1: 2%

Low_Risk Precision: 100% (Due to the high number of low_risk population)
Low_Risk Sensitivity: 69%

**BalancedRandomForestClassifier Model**
<img width="1081" alt="Screen Shot 2022-04-17 at 2 15 16 PM" src="https://user-images.githubusercontent.com/94129215/163727205-7afd5d50-217a-43ec-a896-9e154daa2cfd.png">

Balanced Accuracy Score: 78.8%
High_Risk Precision: 4%
High_Risk Sensitivity: 91% (Due to the lower number of false positivies)
High_Risk F1: 7%

Low_Risk Precision: 100% 
Low_Risk Sensitivity: 67%


**EasyEnsembleClassifier Model**
<img width="1120" alt="Screen Shot 2022-04-17 at 2 16 27 PM" src="https://user-images.githubusercontent.com/94129215/163727241-31b6dfc2-c12b-4ea3-8fec-93efaac5aeec.png">

Balanced Accuracy Score: 92.5%
High_Risk Precision: 7%
High_Risk Sensitivity: 94% (Due to the number of false positives)
High_Risk F1: 14%

Low_Risk Precision: 100% (Due to the high number of low_risk population)
Low_Risk Sensitivity: 91%


## Summary
All the models used demonstrate a weakness in their precision on if a credit risk is high.

The Ensemble models showed a lot more improvement on the sensitivity of high risk credits. 

The EasyEnsembleClassifier model shows a recall of 92.5%, which means it detects a little more than 9 out of 10 high risk credit. The low precision of this model means it will falsely detect low risk credits as high risk credits which penalizes the bank's credit strategy and causes them to miss potentially lucrative business opportunities. 

Due to the overall weakenesses in precision, I would not recommend any of these models for the bank. Further investigation is needed to find a more reliable model to determine credit risk of potential clients.
