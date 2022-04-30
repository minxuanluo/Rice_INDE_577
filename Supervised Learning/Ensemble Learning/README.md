<h1 align="center"> Ensemble Methods </h1>  
<h4 align="center"> Bagging and Boosting are similar in that they are both ensemble techniques, where a set of weak learners are combined to create a strong learner that obtains better performance than a single one. The training set for bagging usually is based on random sampling with replacement from the original set. In the training set for boosting, misclassified data increases its weights. If the difficulty of the single model is over-fitting, then Bagging is the best option to reduce variance; if the base learners are very weak learners like stumps, boosting is good at reducing bias. </h4>
</br>

<h1 align="center"> General Ensemble Learning </h1>  
You can use majority voting to give prediction outputs based on the predictions of multiple classifiers. The classifiers can be from the same class (with different params/randomization) or different algorithms.

The code shuld be similar as follows:

```
voting_clf = VotingClassifier([('lr', clf_1),
                               ('mlp', clf_2),
                               ('dt', clf_3)], voting='hard'
                               )
voting_clf.fit(X_train, y_train)
test_pred = voting_clf.predict(X_test)
print(f'{voting_clf.__class__.__name__}, accuracy score = {accuracy_score(y_test, y_pred)}')
```


<h1 align="center"> Random Forest </h1>  

</br>


<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Introduction"> ➤ Introduction</a></li>
    <li><a href="#Algorithm"> ➤ Algorithm</a></li>
    <li><a href="#Parameters"> ➤ Parameters</a></li>
    <li><a href="#Evaluation"> ➤ Evaluation</a></li>
    <li><a href="#Dataset"> ➤ Dataset</a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Introduction -->
<h2 id="Introduction"> Introduction</h2>

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/rf.jpeg">
</p>

<p align="justify"> 
  Random Forests grows many classification trees. To classify a new object from an input vector, put the input vector down each of the trees in the forest. Each tree gives a classification, and we say the tree "votes" for that class. The forest chooses the classification having the most votes (over all the trees in the forest).
  <ol> 
  <li> The performance of random forest depends on: m: Reducing m reduces both the correlation and the strength. Needs parameter tuning to find a good m.
    <br /> 
    |- the correlation between any two trees in the forest. Increasing the correlation increases the forest error rate.
    <br /> 
    |- The strength of each individual tree in the forest. Decreasing the error rate of the individual trees decreases the forest error rate.
  <li> Start from root, choose a suitable feature xi and its split point ci at each internal node, split the node to two child nodes depending on whether xi <= ci , until the child nodes are pure
  <li>  It is unexcelled in accuracy among current algorithms.
  <li> It runs efficiently on large data bases.
  <li> It can handle thousands of input variables without variable deletion.
  <li> It gives estimates of what variables are important in the classification.
  <li> It generates an internal unbiased estimate of the generalization error (OOB) as the forest building progresses.

</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Algorithm -->
<h2 id="Algorithm"> Algorithm</h2>

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) <br>

<!--This project is written in Python programming language. <br>-->

<p align="justify"> 
  Basic Algorithm for Random Forest:
  <ol> 
  <li> If the number of cases in the training set is N, sample N cases at random - but with replacement, from the original data. This sample will be the training set for growing the tree.
  <li> If there are M input variables, a number m << M is specified such that at each node, m variables are selected at random out of the M and the best split on these m is used to split the node. The value of m is held constant during the forest growing.
  <li> Each tree is grown to the largest extent possible. There is no pruning.
  <li> Majority vote for prediction
   
</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>
<p align="center">
</p>

<p> 
  The most important parameters for a decision are those specifying ensemble configuration and single tree properties. Below are based on scikit learn.
  <ul>
<br />    
<b>Ensemble configuration</b>
    <br /> 
    <li><b>max_samples</b></li>: (If bootstrap is True, the number of samples to draw from X to train each base estimator)
    <br /> 
    <li><b>warm_start</b></li>: (When set to True, reuse the solution of the previous call to fit and add more estimators to the ensemble, otherwise, just fit a whole new forest) 
    <li><b>bootstrap</b></li>: (If False, the whole dataset is used to build each tree) 
    <li><b>n_estimators</b></li>: (default 100, number of trees in the dataset)

<br />   
<br /> 
<b>Single Tree Properties</b>
    <br /> 
    <li><b>optimization crterion</b></li> 
criterion: {“gini”, “entropy”}; splitter: {“best”, “random”}; max_features: int, float or {“auto”, “sqrt”, “log2”}
    <li><b>tree complexity/depth</b></li> 
    max_depth (default=None); min_samples_split (default=2); min_samples_leaf (default = 1); max_leaf_nodes (default=None); min_impurity_decrease (default=None)
    <li><b>Imbalanced data</b></li> 
class_weightdict (list of dict or “balanced”) (default=None). Note that for multioutput (including multilabel) weights should be defined for each class of every column in its own dict. For example, for four-class multilabel classification weights should be [{0: 1, 1: 1}, {0: 1, 1: 5}, {0: 1, 1: 1}, {0: 1, 1: 1}] instead of [{1:1}, {2:5}, {3:1}, {4:1}].
    <br />



  </ul>
</p>



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

<p> 
Common evaluation methods for classification problems such as confusion matrix, accuracy, precision, recall can be used for random forests.
<br />
Additional approaches to investigate how the random forest is making decisions include: plot feature importances (based on impurity reductions for nodes splitting on this feature).
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The HeartDisease dataset is used.


<h1 align="center"> Boosting (XGboost) </h1>  

</br>

<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Introduction"> ➤ Introduction</a></li>
    <li><a href="#Algorithm"> ➤ Algorithm</a></li>
    <li><a href="#Parameters"> ➤ Parameters</a></li>
    <li><a href="#Evaluation"> ➤ Evaluation</a></li>
    <li><a href="#Dataset"> ➤ Dataset</a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Introduction -->
<h2 id="Introduction"> Introduction</h2>

<p align="justify"> 
  When used for classification, Decision Tree starts with a root node of a tree then compares the value of different attributes and follows the next branch until it reaches the end leaf node. It uses different algorithms to check about the split and variable that allow the best homogeneous sets of population. When making predictions about new samples, the samples are routed down the tree and reach a final end leaf node. The predicted class for a test sample is the majority vote of all training samples in that leaf node.
  <ol> 
  <li> Tree structure : internal nodes indicate features, while leaf nodes represent classes
  <li> Start from root, choose a suitable feature xi and its split point ci at each internal node, split the node to two child nodes depending on whether xi <= ci , until the child nodes are pure
  <li>  Equivalent to rectangular partition of the region

</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Algorithm -->
<h2 id="Algorithm"> Algorithm</h2>

* **AdaBoost**

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/ada.png">
</p>

It fits a sequence of weak learners on different weighted training data. It starts by predicting original data set and gives equal weight to each observation. If prediction is incorrect using the first learner, then it gives higher weight to observation which have been predicted incorrectly. Being an iterative process, it continues to add learner(s) until a limit is reached in the number of models or accuracy.

Mostly, we use decision stamps with AdaBoost. But, we can use any machine learning algorithms as base learner if it accepts weight on training data set. We can use AdaBoost algorithms for both classification and regression problem.

* **Gradient Boosting**

In gradient boosting, it trains many model sequentially. Each new model gradually minimizes the loss function (y = ax + b + e, e needs special attention as it is an error term) of the whole system using Gradient Descent method. The learning procedure consecutively fit new models to provide a more accurate estimate of the response variable.

The principle idea behind this algorithm is to construct new base learners which can be maximally correlated with negative gradient of the loss function, associated with the whole ensemble.

* **XGBoost**

"The name xgboost, though, actually refers to the engineering goal to push the limit of computations resources for boosted tree algorithms. Which is the reason why many people use xgboost."

The implementation of XGBoost supports parallelization and regularization.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>
<p align="center">
</p>

There are generally three types of parameters for **XGBoost**: general parameters, booster parameters and task parameters.

* General parameters: relate to which booster we are using to do boosting, commonly tree or linear model

* Booster parameters: depend on which booster you have chosen

* Learning task parameters: decide on the learning scenario. For example, regression tasks may use different parameters with ranking tasks.

* Command line parameters: relate to behavior of CLI version of XGBoost.


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

<p> 
Common evaluation methods for classification problems can be used for XGBoost.
  
<br />
<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/shap.png">
</p>
As an ensemble method, XGBoost is harder to interpret than decision trees. However, we can use SHAP (SHapley Additive exPlanations), which is "a game theoretic approach to explain the output of any machine learning model". It "connects optimal credit allocation with local explanations using the classic Shapley values from game theory and their related extensions (see papers for details and citations)." It gives us an idea of how each feature is contributing the final prediction that the model makes.
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The HeartDisease dataset is used.
