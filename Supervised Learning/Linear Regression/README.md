<h1 align="center"> Linear Regression </h1>  

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Regression/images/linear.png">
</p>

<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Introduction"> ➤ Introduction</a></li>
    <li><a href="#Assumptions"> ➤ Assumptions</a></li>
    <li><a href="#Evaluation"> ➤ Evaluation</a></li>
    <li><a href="#Dataset"> ➤ Dataset</a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Introduction -->
<h2 id="Introduction"> Introduction</h2>

* **Exploratory Analysis**

Exploratory analysis can be used to make sure the explanatory variables have a linear relationship with the dependent variable. If a apparent non-linear pattern is found, then we may need to transform the feature before including it in the model (e.g., polynomial transformation, log transformation).

* **Ordinary Least Squares**

Coefficient Estimates: Beta = (X^TX)^(-1)X^TY

* **Regularization**

To avoid overfitting, we sometimes add a penalty term to the cost function, which regularizes or shrinks the coefficient estimates towards zero. In other words, this technique discourages learning a more complex or flexible model. Depend on we using L1 norm or L2 norm for the penalty term, it will be Lasso Regression or Ridge Regression.

Ridge regression tends to shrink the coefficients for least important predictors, very close to zero. But it will never make them exactly zero. Lasso regression shrinks unimportant features' coefficient to exactly zero, which is similar to performing variable selection.


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Assumptions -->
<h2 id="Assumptions"> Assumptions</h2>

* **Linearity**: 

The relationship between X and the mean of Y is linear.
 
* **Homoscedasticity**: 

The variance of residual is the same for any value of X.

* **Independence**: 

Observations are independent of each other.

* **Normality**: 

For any fixed value of X, Y is normally distributed.

* **No Perfect Multicollinearity**: 

No independent variable can be calculated by a linear combination of other independent variables. Variance Inflation Factor (VIF) can be checked. The general rule of thumb is that VIFs exceeding 4 warrant further investigation, while VIFs exceeding 10 are signs of serious multicollinearity requiring correction.


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

<p> 
The most commonly used metric for evaluating regression models is Mean Squared Error. 
  
  R2 is measures the goodness of fit of a model. This statistic indicates the percentage of the variance in the dependent variable that the independent variables explain collectively.
  
  The residuals should exhibit random patterns. If a notable pattern is found in residuals, this may indicate violation of linear regression's assumptions. Transformation may be needed before rerunning the model.
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The Academic Performance dataset is used.
