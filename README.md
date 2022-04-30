<h1 align="center"> INDE577-Project </h1>
<h3 align="center"> This is a repository for INDE 577 - Data Science and Machine Learning </h3>  

</br>


<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project"> ➤ About The Project</a></li>
    <li><a href="#prerequisites"> ➤ Prerequisites</a></li>
    <li><a href="#folder-structure"> ➤ Folder Structure</a></li>
    <li><a href="#dataset"> ➤ Dataset</a></li>
   <!--<li><a href="#experiments">Experiments</a></li>-->
    <li><a href="#contributors"> ➤ Contributors</a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- ABOUT THE PROJECT -->
<h2 id="about-the-project"> About The Project</h2>

<p align="justify"> 
  This repository aims to review of all the machine learning algorithms covered in the course INDE577 (Spring 2022), with the specific goals to:
  <ol> 
  <li> Clearly explaining the algorithm being implemented
  <li> Use exploratory analysis to understand the data being used
  <li> Identify types of problems and suitable algorithms
  <li> Conducting performance and error analysis
</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- PREREQUISITES -->
<h2 id="prerequisites"> Prerequisites</h2>

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) <br>

<!--This project is written in Python programming language. <br>-->
The following open source packages are used in this project:
* Numpy
* Pandas
* Matplotlib
* scikit learn
* tensorflow

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="folder-structure"> Folder Structure</h2>

    ├── Supervised Learning
    ├────── README.md
    ├────── Logistic Regression
    ├────── Decision Tree
    ├────── Neural Network
    ├────── Support Vector Machine
    ├────── K-Nearest Neighbors
    ├────── Ensemble Learning
    ├────── Linear Regression
    ├────── Regression Tree

    ├── Unsupervised Learning
    ├────── README.md
    ├────── K-Means Clustering
    ├────── Principal Component Analysis
    
    ├── Optimization
    ├────── README.md
    ├────── Gradient Descent 
 
    ├── README.md
    
  

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- DATASET -->
<h2 id="dataset"> Dataset</h2>

<p align="center">
</p>

<p> 
  There are two types of tasks that this course mainly cover: classification and regression. In classfication problems, the target variable is a categorical variable. The target can have two or more levels. Models' performances are usually measured by metrics such as accuracy, precision, recall, area under the curve (AUC). In regression, the target variable is a continuous variable. Models' performances are usually measured by measures such as Mean Squared Error. 
  
  Two different datasets are used in this project, one is a classification problem, and another one is a regression problem.
  <ul>
    <li><b>Heart Disease Prediction</b>: Binary Classification Problem</li> 
    <br />
Heart disease is one of the leading causes of death for people of most races in the US. Common risk factors for heart diseass include high blood pressure, high cholesterol, and smoking. Other key indicator include diabetic status, obesity (high BMI), not getting enough physical activity or drinking too much alcohol. Identifying these key risk factors is very important in healthcare. Machine learning methods are used to identify important factors to predict a patient's condition.This dataset contains 18 variables (9 booleans, 5 strings and 4 decimals). <br />
    <br />
The 'HeartDisease' variable has value of 'Yes' for respondents that have ever reported having coronary heart disease (CHD) or myocardial infarction (MI). 
    <br />
This dataset is used in notebooks for Logistic Regression, Decision Tree, Ensemble Learning.
    <br />
    <br />
    <li><b>Face Recognition Dataset (from sklearn)</b>: Multi-class Classification Problem </li> 
    <br />
This data contains black and white images of previous US presidents' faces. The target variable for this dataset name. 
    <br />
This dataset is used in notebooks for Neural Network, SVM.
    <br />
    <br />
    <li><b>Academic Performance Prediction</b>: Regression Problem</li> 
    <br />
This data approach student achievement in secondary education of two Portuguese schools. The data attributes include student grades, demographic, social and school related features) and it was collected by using school reports and questionnaires. The dataset regarding the performance in Mathematics (mat) is used in this project. In the dataset, the target attribute G3 has a strong correlation with attributes G2 and G1. G3 is the final year grade (issued at the 3rd period), while G1 and G2 correspond to the 1st and 2nd period grades. The regression task here is to predict variable G2. Variable G3 is dropped, and G1 is included as an explanatory variable.
    <br />
    <br />
    <li><b>Fruit dataset</b>:  Multi-class Classification Problem</li> 
    <br />
This data contains fruit types as labels and records for instances with features such as mass, weight, height.
    <br />
This dataset is used in notebooks for KNN.
    <br />
    <br />
    <li><b>Facebook Live Sellers in Thailand Data Set</b>: Has label, but not used for Training. Used for Unsupervised Learning</li> 
    <br />
This data contains engagment metrics for posts such as num_reactions, num_comments, num_shares, num_likes, num_loves, num_wows, num_hahas, num_sads, num_angrys. Each record also has a status_type variable, which is the type of the post, being 'video', 'photo', 'link' or 'status'.
    <br />
This dataset is used in notebooks for K-Means, PCA.
    <br />
    <br />
    
  </ul>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- CONTRIBUTOR -->
<h2 id="contributors"> Contributors</h2>

<p>

  <b>Minxuan Luo</b> <br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Email: ml122@rice.edu<a></a> <br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; GitHub: <a href="https://github.com/minxuanluo">@minxuanluo</a> <br>
