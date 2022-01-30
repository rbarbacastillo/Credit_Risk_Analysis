# Credit_Risk_Analysis

# Analysis Overview

In this project, we use Python to build and evaluate supervised machine learning models to predict credit risk evaluation.

We adopted the following procedure:

* oversample the data using the RandomOverSampler and SMOTE algorithms.
* Undersample the data using the ClusterCentroids algorithm.
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

According to the results of the different models we will evaluate which is the most useful model for this purpose

# Resources

Data Source: LoanStats_2019Q1.csv
Software: Python 3.7.9, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3
Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)
RandomOverSampler model

* The balanced accuracy score is 65%.
* The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
* Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

# SMOTE model

* The balanced accuracy score is 64%.
* The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
* Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.

# ClusterCentroids model

The balanced accuracy score is down 52%.
The high_risk precision is 1% with 63% sensitivity and a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is 40%.

# SMOTEENN model

The balanced accuracy score is about 62%.
The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.
Due to the high number of false positives, the low_risk sensitivity is 57%.

# BalancedRandomForestClassifier model

The balanced accuracy score improved to 79%.
The high_risk precision is at 4% with 67% sensitivity with a F1 of 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

# EasyEnsembleClassifier model

The accuracy score increases 93%.
The high_risk precision is still at 7% with 91% sensitivity which makes a F1 of 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

# Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models has a better sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% which is useful to detect high risk credits, but with a low precision, however there is a flaw to detect low risk credits, cosidering them as high risk credits.

Depending on the institution strategy, the model could be useful or adjusted.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.
