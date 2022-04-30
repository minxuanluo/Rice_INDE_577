<h1 align="center"> Decision Tree </h1>  

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/dt.png">
</p>

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

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) <br>

<!--This project is written in Python programming language. <br>-->

<p align="justify"> 
  Basic Algorithm for Decision Tree:
  <ol> 
  <li> Start with the whole training data
  <li> Select attribute and the splitting value based on impurity measures:
    <br />
   |- Gini Index
    <br />
   |- Information Gain
    <br />
   |- Misclassification Error
  <li> Create child nodes based on split
  <li> Recurse on each child node utiling a stopping criterion below is reached:
    <br />
   |- All samples in the node have the same class
    <br />
   |- Number of samples in the node smaller than or equal to the specified minimum number of samples required to split the node
    <br />
   |- The tree has reached maximum depth
   
</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>
<p align="center">
</p>

<p> 
  The most important parameters for a decision are those specifying optimization crterion, tree complexity/depth and imbalanced data. Below are based on scikit learn.
  <ul>
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
Common evaluation methods for classification problems can be used for decision trees.
<br />
Additional approaches to investigate how the decision tree is making decisions include: plot feature importances (based on impurity reductions for nodes splitting on this feature); plot tree structure (see on each level which threshold of which variable is used for splitting).
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The HeartDisease dataset is used. It is the same dataset we used in the Logistic Regression Notebook. Note that the SMOTE_training_x.csv, SMOTE_training_y.csv, x_test.csv, y_test.csv files are saved in the Logistic Regression Notebook.
This makes sure that we are using the exactly same train_test split as in the Logistic Regression Notebook, and the results can be compared with each other.

