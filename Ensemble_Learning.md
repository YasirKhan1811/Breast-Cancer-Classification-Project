# Bagging and Boosting Algorithms (Random Forest and XGBoost)

This project involves building XGBoost, an ensemble learner classification model, to predict whether the breast cancer is malignant "M" or benign "B". This readme file discusses about the ensemble learning methods in great detail.

##Ensemble-Learning

Ensemble Learning Methods:
**Bagging: Deep trees. Independent weak learners (parallel models). Used to decrease the variance of the base model.
Boosting: Shallow trees. Dependent weak learners (sequential models). Used to decrease the biaseness of the base model.**

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

https://www.analyticsvidhya.com/blog/2020/02/what-is-bootstrap-sampling-in-statistics-and-machine-learning/#:~:text=of%20Bootstrap%20Sampling.-,Bootstrap%20Sampling%20in%20Machine%20Learning,stability%20of%20machine%20learning%20algorithms

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

+ Bagging and Boosting get N learners by generating additional data in the training stage.
+ N new training data sets are produced by random sampling with replacement from the original set.
+ By sampling with replacement some observations may be repeated in each new training data set.
+ In the case of Bagging, any element has the same probability to appear in a new data set.
+ However, for Boosting the observations are weighted and therefore some of them will take part in the new sets more often.
+ These multiple sets are used to train the same learner algorithm and therefore different classifiers are produced.

This is represented diagrammatically as follows:
![image](https://user-images.githubusercontent.com/96954071/173543234-203158bd-c016-4ce8-81ad-8b2fddcbf2bb.png)

**Weighted data elements**
While the training stage is parallel for Bagging (i.e., each model is built independently), Boosting builds the new learner in a sequential way as follows:

![image](https://user-images.githubusercontent.com/96954071/173543653-44118298-ddc2-4223-8183-9a0f67f47e37.png)

+ After each training step, the weights are redistributed. Misclassified data increases its weights to emphasise the most difficult cases.
+ In this way, subsequent learners will focus on them during their training.

**Classification stage in action**
+ To predict the class of new data we only need to apply the N learners to the new observations.
+ In Bagging the result is obtained by averaging the responses of the N learners (or majority vote).
+ However, Boosting assigns a second set of weights, this time for the N classifiers, in order to take a weighted average of their estimates.
+ This is shown diagrammatically below:

![image](https://user-images.githubusercontent.com/96954071/173544611-db5567dd-3f92-40c9-b192-3124f6259efc.png)

+ In the Boosting training stage, the algorithm allocates weights to each resulting model.
+ A learner with good a classification result on the training data will be assigned a higher weight than a poor one.
+ So when evaluating a new learner, Boosting needs to keep track of learners’ errors, too.
+ Let’s see the differences in the procedures:

![image](https://user-images.githubusercontent.com/96954071/173545480-d0e09331-b6ef-4673-b1eb-ef7de06d2a77.png)

+ Some of the Boosting techniques include an extra-condition to keep or discard a single learner.
+ For example, in AdaBoost, the most renowned, an error less than 50% is required to maintain the model; otherwise, the iteration is repeated until achieving a learner better than a random guess.
+ The previous image shows the general process of a Boosting method, but several alternatives exist with different ways to determine the weights to use in the next training step and in the classification stage.

Links for references:
1. https://www.kaggle.com/code/prashant111/bagging-vs-boosting/notebook
2. https://towardsdatascience.com/ensemble-methods-bagging-boosting-and-stacking-c9214a10a205
3. https://www.datacamp.com/tutorial/xgboost-in-python#what
4. https://www.analyticsvidhya.com/blog/2018/06/comprehensive-guide-for-ensemble-models/
5. https://towardsdatascience.com/decision-tree-ensembles-bagging-and-boosting-266a8ba60fd9



