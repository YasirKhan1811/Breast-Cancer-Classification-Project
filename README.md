# Ensemble-Learning
Ensemble Learning Methods

Links for references:
1. https://www.kaggle.com/code/prashant111/bagging-vs-boosting/notebook
2. https://towardsdatascience.com/ensemble-methods-bagging-boosting-and-stacking-c9214a10a205
3. https://www.datacamp.com/tutorial/xgboost-in-python#what
4. https://www.analyticsvidhya.com/blog/2018/06/comprehensive-guide-for-ensemble-models/

In ensemble learning, a set of weak learners are combined to create a strong learner that obtains better performance than a single one. It combines several models to increase the performance of ML model compared to a single model. Bagging and Boosting are two types of ensemble learning techniques. These two decrease the variance of single estimate as they combine several estimates from different models.

The main causes of error are due to noise, bias, and variance. Ensemble helps to minimize these factors.

+ Bagging helps to decrease the model’s variance.
+ Boosting helps to decrease the model’s bias.

Combinations of multiple classifiers decrease variance, especially in the case of unstable classifiers, and may produce a more reliable classification than a single classifier.

To use Bagging or Boosting you must select a base learner algorithm. For example, if we choose a classification tree, Bagging and Boosting would consist of a pool of trees as big as we want. The description of bagging and boosting can be seen in the following diagram:

![image](https://user-images.githubusercontent.com/96954071/173231121-4aaf0a75-5e3c-4e7e-a0bd-63efdab82a0d.png)

Bootstrap Sampling (Bootstrapping)
Links for reference:
https://www.analyticsvidhya.com/blog/2020/02/what-is-bootstrap-sampling-in-statistics-and-machine-learning/#:~:text=of%20Bootstrap%20Sampling.-,Bootstrap%20Sampling%20in%20Machine%20Learning,stability%20of%20machine%20learning%20algorithms.

https://towardsdatascience.com/what-is-bootstrap-sampling-in-machine-learning-and-why-is-it-important-a5bb90cbd89a

