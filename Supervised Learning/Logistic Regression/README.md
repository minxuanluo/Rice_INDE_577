<h1 align="center"> Logistic Regression </h1>  

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
  <img width="460" height="250" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/logistic_regression.jpeg">
</p>

<p align="justify"> 
  Logistic Regression, also known as the Logit Model, is usually used as the baseline model in classification problems. The dependent variable is a categorical variable, if it has two levels it is binary regression; if it has more than 2 levels it is multinomial regression. This type of analysis can help you predict the likelihood of an event happening or a choice being made. 

</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Algorithm -->
<h2 id="Algorithm"> Algorithm</h2>

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) <br>

<!--This project is written in Python programming language. <br>-->

<p align="justify"> 
  The logistic model:
  
  log(p(X)/(1-p(X))) = b^TX = b1X1 + b2X2 + ... + bpXp
  
  The coefficient estimates are obtained from maximum likelihood estimation. In practice, we can maximize the log likelihood function by running repeated weighted least squares regressions. We refer to it as iteratively reweighted least squares or IRLS. Statistical softwares usually do the optimization iteratively.
  
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>
<p align="center">
</p>

Maximum Iteration: Note that in Python's statsmodel package, by default, the maximum number of iterations performed for Logistic regression is 35, after which the optimization fails. This is because logistic regression usually converges really fast.

If the training procedure stops at the maximum iteration, it is likely because that there is complete separation, or quasi-complete separation. In this case some parameters might go off to infinity and the optimization stops at some convergence or stopping criterion. There is a small chance that this is just a very complex optimization problem. In this case, just increase the maximum iteration parameter.

Before running the Logistic Regression, make sure use dummy encodings for all categorical variables, choose a base value for each variable, and drop the dummy variable for that base value.


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

<p> 
Common evaluation methods for classification problems, such as confusion matirx, precision, recall, accuracy, ROC-AUC can be used.
<br />
  
  A lot of times we are also interested in the coefficient estimates - they can be better interpretated after calculating the odds ratios. Odds is defined as p(event)/(1-p(event)). Odds ratio is defined as the ratio of two odds. For example, if the gender in our sample has two values: male and female, then the odds ratio for gender is [p(event, male)/(1-p(event, male))]/[p(event, female)/(1-p(event, female))]. And this can be caluclated by taking the exponential of the coefficient estimate of the male variable (e^beta(male)).
<br />
  
  We can also examine each explanatory variables' contributions by looking at the absolute magnitude and the sign of the estimated coefficients, look at their statistical significance, and calculate confidence intervals for coefficient estimates or for odds ratios.
  
  In this notebook I used a imbalanced dataset, so model performances with/without oversampling (on training set) are compared based on an (imbalanced) test set.
  
  
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The HeartDisease dataset is used.
