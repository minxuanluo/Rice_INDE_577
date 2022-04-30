<h1 align="center"> Support Vector Machine </h1>  

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


  Support Vector Machine (SVM) is a supervised machine learning algorithm that is mostly used for classification task (it can also be used for regression). In SVM, the data points are in n-dimensional space (with n: number of features). Classification is performed by finding the hyper-plane that differentiates the classes well.
  
  There are two types of SVMs:
  
  * Linear SVM: Linear SVM is used for linearly separable data, which means if a dataset can be classified into two classes by using a single straight line, then such data is termed as linearly separable data, and classifier is used called as Linear SVM classifier.
  
<p align="center">
  <img width="450" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/svm.png">
</p>
  
  * Non-linear SVM: Non-Linear SVM is used for non-linearly separated data, which means if a dataset cannot be classified by using a straight line, then such data is termed as non-linear data and classifier used is called as Non-linear SVM classifier.

<p align="center">
  <img width="450" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/svm-kernel.png">
</p>

  <p align="justify"> 
  <ol> 
    
  <li> Pros:
    
    It works really well with a clear margin of separation
    
    It is effective in high dimensional spaces.
    
    It is effective in cases where the number of dimensions is greater than the number of samples.
    
    It uses a subset of training points in the decision function (called support vectors), so it is also memory efficient.
    
  <li> Cons: 
    
    Training time is long when we have a large dataset

    It doesn't cope well with dataset that has classes that have large overlapping regions. 

    SVM doesn’t directly provide probability estimates, these are calculated using an expensive five-fold cross-validation. It is included in the related SVC method of Python scikit-learn library.
    
</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Algorithm -->
<h2 id="Algorithm"> Algorithm</h2>

<p align="center">
  <img width="450" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/svm-optim.png">
</p>

<p align="center">
  <img width="450" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/soft margin.png">
</p>

<!--General Idea of SVM <br>-->

SVM can be considered as a constrained optimization problem. Here we assume linear SVM - we can solve it by using method of Lagrange Multipliers.




![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>

1. kernel: the function to transform data

    choosing the right kernel is crucial, because if the transformation is incorrect, then the model can have very poor results. 
    
    As a rule of thumb, always check if you have linear data and in that case always use linear SVM (linear kernel). Linear SVM is a parametric model, but an RBF kernel SVM isn’t, so the complexity of the latter grows with the size of the training set. 
    
    It is more computationally expensive to train an SVM with a kernel, the model becomes more complex and more prune to overfitting. 
    
2. Regularization Praramter (C in python): soft margin, how much you can tolerate misclassification.
    
    The Regularization Parameter (in python it’s called C) tells the SVM optimization how much you want to avoid miss classifying each training example.
    
    If the C is higher, the optimization will choose smaller margin hyperplane, so training data miss classification rate will be lower.
    
    If the C is low, then the margin will be big, even if there will be miss classified training data examples. Reducing C can help alleviate the problem of overfitting.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

Usual evaluation methods for classification problems: confusion matrix, precision, recall, accuracy, ROC-AUC.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
A built-in dataset (face recognition) in sklearn is used. It is the same dataset as the one we use in the Neural Network notebook. PCA is first used to get features from the images.
