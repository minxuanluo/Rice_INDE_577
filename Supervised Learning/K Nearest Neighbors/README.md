<h1 align="center"> K Nearest neighbors </h1>  

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
  <img width="300" height="150" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/knn.png">
</p>

<p align="justify"> 
  k-nearest neighbor (kNN) is the simplest supervised learning method, especially useful when prior knowledge on the data is very limited

  * Do training and test simultaneously: When classifying a test sample x, scan the training set and find the closest k samples Dk = {x1,...,xk} to the test sample. Then make vote based on the labels of the samples in Dk. The majority vote is the label of the test sample

  * Low bias, high variance
    
  * Pros: Not sensitive to outliers; easy to implement and parallelize
    
  * Cons: Need to tune k, take large storage, computationally intensive
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Algorithm -->
<h2 id="Algorithm"> Algorithm</h2>

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) <br>

<!--This project is written in Python programming language. <br>-->

<p align="justify"> 
  Basic Algorithm for K Nearest Neighbors:

  Input : training set Dtrain = {(x1,y1),...,(xN,yN)}, a test sample x without label y, k and distance metric d(x,y)
    
  Output : predicted label ypred for x
  
  1. Compute d(x,xj) for each (xj,yj) ∈ Dtrain 
  
  2. Sort the distances in an ascending order, choose the first k samples (x(1), y(1)), . . . , (x(k), y(k))
  
  3. Make majority vote ypred = Mode(y(1), . . . , y(k))

</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>
<p align="center">
</p>

<p> 
  The most important parameter for K Nearest Neighbors is k.
  
  To tune k: Use Cross-validation (CV): partition the dataset into M parts (M = 5 or 10), let κ : {1,...,N} → {1,...,M} be randomized partition index map, the CV estimate of prediction error is CV(fˆ,k) = sum(L(yi,fˆ−κ(i)(xi,k)))/N.

</p>



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

<p> 
Common evaluation methods for classification problems such as confusion matrix, precision, recall, ROC-AUC can be used for K Nearest Neighbors.

</p>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
I use a fruit dataset for this task. KNN is based on distance calculation and is relatively slow on large dataset compared to other methods such as random forest. Specifically, we are using a fruit's mass, width, height to predict what kind of fruit it is.

Besides directly using sklearn, I also include code to implement KNN from scratch.
