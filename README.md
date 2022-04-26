# Credit Risk Analysis
Module 17 Challenge

## Overview of the Credit Risk Analysis Project
The Credit Risk Analysis was intended to utilize machine learning to address credit card risk. Specifically, the goal was to utilize a variety of machine learning techniques such as oversampling, undersampling, SMOTEENN, BalancedRandomForestClassifier and EasyEnsembleClassifier to find the model that best predicts credit risk. In predicting credit rusk, the data includes a variety of factors such as home ownership status, annual income, prior recorded bankruptcies (to name a few). 


## Results

### RandomOverSampler
- Balanced accuracy score = .49
- Precision is high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision is low for high-risk
- Recall is low for low-risk and high for high-risk applications

![](/Images/RandomOverSampling.png)

### RandomOverSampler on Scaled Data
- Balanced accuracy score = .83. The scaled data led to a much higher balanced accuracy score with this model.
- Precision and recall are high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision remains low for high-risk
- Recall is high for both high-risk and low-risk applications

![](/Images/ScaledRandomOverSampler.png)

### SMOTE
- Balanced accuracy score = .66. 
- Precision is high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision remains low for high-risk
- Recall is average for both high-risk and low-risk applications

![](/Images/SMOTE.png)

### ClusterCentroids
- Balanced accuracy score = .66. 
- Precision is high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision remains low for high-risk
- Recall is average for both high-risk and low-risk applications

![](/Images/ClusterCentroids.png)

### SMOTEENN
- Balanced accuracy score = .54. 
- Precision is high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision remains low for high-risk
- Recall is high for high-risk applications and mediocre for low-risk applications

![](/Images/SMOTEENN.png)

### BalancedRandomForestClassifier
- Balanced accuracy score = .82. 
- Precision is high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision remains low for high-risk
- Recall is high for both high-risk and low-risk applications

![](/Images/RandomForest.png)

### EasyEnsembleClassifier
- Balanced accuracy score = .92. 
- Precision is high for the low-risk populuation, meaning that almost all low-risk credit applications were predicted correctly
- Precision remains low for high-risk
- Recall is high for both high-risk and low-risk applications

![](/Images/EasyEnsemble.png)

## Summary 
- Recall is highest for the EasyEnsembleClassifier model and followed closely by the RandomForestClassifier model. Recall is important in this model because we want to ensure to capture all of the high-risk applications so that the credit card company can detech fraudulent transactions in realtime. 
- Precision is high for all models which means the model is effective in identifying low-risk applications but also tags many of the high-risk applications as low-risk. High precision is helpful in situations where there is value in ensuring that no applications be mistakenly marked as high-risk. We can be confident that those applications identified as high-risk in these models are high-risk, but we also must understand that some of the 1,000s of applications marked as low-risk are also high-risk but not identified as such. 
- Ultimate preference in which model to use depends on the credit card company goals and objectives. Assuming that the credit card company wants to detect as many high-risk transactions as possible, even if some aren't high-risk and can be further vetted/researched to ultimately be dismissed, would suggest use of a high recall model such as the EasyEnsembleClassifier or RandomForestClassifier models.


