<h1 align="center"> Principal component analysis (PCA) </h1>  

<h2 id="Introduction"> Introduction</h2>

PCA is commonly used in exploratory analysis and dimensionality reduction. 

It tries to reduce data's dimension but preserve as much variability in the data as possible. The first principal component is on a direction that maximizes the variance of the projected data. The i-th principal component is on a direction orthogonal to the previous i-1 principal components and maximizes the variance of the projected data.

The principal components are eigenvectors of the data's covariance matrix. The principal components can be computed by eigendecomposition of the data covariance matrix or singular value decomposition of the data matrix.

Since we do not want the PCA to be dominated by a particular variable just because its value range is much larger compared to other variables, we usually do some form of standardization for the features before performing PCA.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="Dataset"> Dataset</h2>
The 'Facebook Live Sellers in Thailand Data Set' is used.
