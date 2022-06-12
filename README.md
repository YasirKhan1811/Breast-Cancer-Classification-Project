# Ensemble-Learning
Ensemble Learning Methods

Links for references:
1. https://www.kaggle.com/code/prashant111/bagging-vs-boosting/notebook
2. https://towardsdatascience.com/ensemble-methods-bagging-boosting-and-stacking-c9214a10a205
3. https://www.datacamp.com/tutorial/xgboost-in-python#what

In ensemble learning, a set of weak learners are combined to create a strong learner that obtains better performance than a single one. It combines several models to increase the performance of ML model compared to a single model. Bagging and Boosting are two types of ensemble learning techniques. These two decrease the variance of single estimate as they combine several estimates from different models.

The main causes of error are due to noise, bias, and variance. Ensemble helps to minimize these factors.

+ Bagging helps to decrease the model’s variance.
+ Boosting helps to decrease the model’s bias.

Combinations of multiple classifiers decrease variance, especially in the case of unstable classifiers, and may produce a more reliable classification than a single classifier.

To use Bagging or Boosting you must select a base learner algorithm. For example, if we choose a classification tree, Bagging and Boosting would consist of a pool of trees as big as we want.

![image](https://user-images.githubusercontent.com/96954071/173231121-4aaf0a75-5e3c-4e7e-a0bd-63efdab82a0d.png)

