<h1 align="center"> KMeans </h1>  

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
  K-Means is different from the other algorithms covered in this classification sub-repository - it is a unsupervised algorithm, while all of the others are supervised algorithms. For unsupervised learning, there are no target labels used (usually it is because the target labels are not available). This makes the performance of the K-Means model harder to evaluate, as we cannot predict the predicted labels with the true labels. However, it is very useful when target labels not available/ as an exploratory analysis method.
  
  K-Means algorithm groups n samples to k clusters, making each sample belong to the nearest cluster. k is a hyperparameter that we have to decide before running the algorithm either by using domain knowledge or by parameter tuning during the training process.
  
  <ol> 
    
  <li> Central goal : optimize the similarity (dissimilarity) between the individual objects being clustered. Specifically, we want to:
    
    |- Obtain great similarity of samples within cluster
    
    |- Obtain great dissimilarity of samples between clusters
    
  <li> Cost functions: not related to the outputs, but related to the similarity
    
  <li> Pros:Intuitive, easy to implement; Low computational complexity, O(tnpK), where t is the number of iterations
    
  <li> Cons: Need to specify K first; Strong dependence on the initial guess of cluster center; Easy to stuck at local minimum; Naturally assume ball-shaped data, hard to deal with data which are not ball-shaped; Sensitive to outliers
    
</ol>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Algorithm -->
<h2 id="Algorithm"> Algorithm</h2>

<p align="center">
  <img width="600" height="400" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/kmeans.png">
</p>

<!--General Idea of K-Means Clustering <br>-->

1. Choose the number of clusters(K) and obtain the data points 
2. Place the centroids c_1, c_2, ..... c_k randomly 
3. Repeat steps 4 and 5 until convergence or until the end of a fixed number of iterations
4. for each data point x_i:
       - find the nearest centroid(c_1, c_2 .. c_k) 
       - assign the point to that cluster 
5. for each cluster j = 1..k
       - new centroid = mean of all points assigned to that cluster
6. End 

Note: Usually we need to standardize the data before using them as inputs to the K-Means algorithm. K-means is sensitive to variance in data, and features with larger variance have more influence on result. We need to be careful when the explanatory variables we have are in different measurement units. Even if the variables are in the same measurement unit but have very different value ranges, standardization might be a good idea.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Parameters -->
<h2 id="Parameters"> Parameters</h2>

1. k: this is the most important hyper-parameter for K-Means. We can choose K based on:

    |- The Elbow Method: In this method, you choose a different number of clusters and start plotting the within-cluster distance to the centroid. The 'elbow' is where the within-cluster distance reaches the optimum minimum value.

    |- Other methods to choose k include Minimizing Bayesian Information Criterion (BIC) based on the likelihood function; Based on Minimum Description Length (MDL); or Based on Gaussian distribution assumption (starting from K = 1, increases K until the points in every cluster follow Gaussian distribution).
    
    
2. init ({‘k-means++’, ‘random’}): method for initialization.
    
    |- ‘k-means++’ : selects initial cluster centers for k-mean clustering in a smart way to speed up convergence.
    
    |- ‘random’: choose n_clusters observations (rows) at random from data for the initial centroids.
    
3. algorithm ({“auto”, “full”, “elkan”}, default=”auto”): K-means algorithm to use

    |- “full”: the classical EM-style algorithm 
    
    |- “elkan” variation is more efficient on data with well-defined clusters, by using the triangle inequality. More memory intensive.
    
    |- For now "auto" is “elkan”
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Evaluation -->
<h2 id="Evaluation"> Evaluation</h2>

<p align="center">
</p>

1. Silhouette Analysis
Silhouette analysis can be used to determine the degree of separation between clusters. For each sample:

Compute the average distance from all data points in the same cluster (ai).

Compute the average distance from all data points in the closest cluster (bi).

Compute the coefficient: (bi-ai)/max(bi, ai). [If it is 0: the sample is very close to the neighboring clusters; It it is 1 –> the sample is far away from the neighboring clusters; It it is -1 –> the sample is assigned to the wrong clusters.]

Compute average silhouette score.

2. Visual inspection if the data is in low dimension. If the data has many x variables, it may be useful to do PCA before doing visual inspection of the clustering results.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The 'Facebook Live Sellers in Thailand Data Set' is used.
