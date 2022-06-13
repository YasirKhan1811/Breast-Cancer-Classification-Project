# Ensemble-Learning
Ensemble Learning Methods

Links for references:
1. https://www.kaggle.com/code/prashant111/bagging-vs-boosting/notebook
2. https://towardsdatascience.com/ensemble-methods-bagging-boosting-and-stacking-c9214a10a205
3. https://www.datacamp.com/tutorial/xgboost-in-python#what
4. https://www.analyticsvidhya.com/blog/2018/06/comprehensive-guide-for-ensemble-models/

In ensemble learning, a set of weak learners are combined to create a strong learner that obtains better performance than a single one. It combines several models to increase the performance of ML model compared to a single model. Bagging and Boosting are two types of ensemble learning techniques. These two decrease the variance of single estimate as they combine several estimates from different models.

What are ensemble methods?
Ensemble learning is a machine learning paradigm where multiple models (often called “weak learners”) are trained to solve the same problem and combined to get better results. The main hypothesis is that when weak models are correctly combined we can obtain more accurate and/or robust models.

The main causes of error are due to noise, bias, and variance. Ensemble helps to minimize these factors.

+ Bagging helps to decrease the model’s variance.
+ Boosting helps to decrease the model’s bias.

Combinations of multiple classifiers decrease variance, especially in the case of unstable classifiers, and may produce a more reliable classification than a single classifier.

To use Bagging or Boosting you must select a base learner algorithm. For example, if we choose a classification tree, Bagging and Boosting would consist of a pool of trees as big as we want. The description of bagging and boosting can be seen in the following diagram:

![image](https://user-images.githubusercontent.com/96954071/173231121-4aaf0a75-5e3c-4e7e-a0bd-63efdab82a0d.png)

**Bootstrap Sampling (Bootstrapping)**
Bootstrapping is random sampling from original dataset with replacement. The size of the subsets is the same as the size of the original set.

**Bagging**
+ Also known as Bootstrap Aggregation. It is a powerful ensemble method. Bagging is the application of the Bootstrap procedure to a high-variance machine learning algorithm, typically decision trees.

+ The idea behind bagging is combining the results of multiple models (for instance, all decision trees) to get a generalized result. Now, bootstrapping comes into picture.

+ Bagging (or Bootstrap Aggregating) technique uses these subsets (bags) to get a fair idea of the distribution (complete set). The size of subsets created for bagging may be less than the original set.

+ The pictorial representation is as follows:

![image](https://user-images.githubusercontent.com/96954071/173240546-7ea9d5f3-aa22-4bbe-aa4c-ed9afe879189.png)

How Bagging works:

+ Multiple subsets are created from the original dataset, selecting observations with replacement.

+ A base model (weak model) is created on each of these subsets.

+ The models run in parallel and are independent of each other.

+ The final predictions are determined by combining the predictions from all the models.

Now, bagging can be represented diagrammatically as follows:

![image](https://user-images.githubusercontent.com/96954071/173240617-1a9d2e9a-9cb7-46fe-9112-3f489adcc5ac.png)

**Boosting**

* Boosting is a sequential process, where each subsequent model attempts to correct the errors of the previous model. The succeeding models are dependent on the previous model.
* In this technique, learners are learned sequentially with early learners fitting simple models to the data and then analyzing data for errors. In other words, we fit consecutive trees (random sample) and at every step, the goal is to solve for net error from the prior tree.
* When an input is misclassified by a hypothesis, its weight is increased so that next hypothesis is more likely to classify it correctly. By combining the whole set at the end converts weak learners into better performing model.
 
Let’s understand the way boosting works in the below steps.

1. A subset is created from the original dataset.

2. Initially, all data points are given equal weights.

3. A base model is created on this subset.

4. This model is used to make predictions on the whole dataset.

Let's understand Boosting with the following illustration:
![image](https://user-images.githubusercontent.com/96954071/173283063-f549805b-3fdc-467c-a997-179be2905d51.png)

**Getting N learners for Bagging and Boosting**


