<h1 align="center"> Gradient Descent </h1>

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/gd.jpeg">
</p>

<h2 id="Introduction"> Introduction</h2>
Unlike other algorithms we applied in this repository, Gradient Descent itself is not a machine learning method. It is an optimization method that lies behind many
machine learning algorithms. In other words, during the training phase of many machine learning methods, gradient descent is used to minimize the cost function. It requires
the cost function to be differentiable.

<h2 id="Formula"> Formula</h2>
As an example, for regression problem with mean square error as the loss function, the formulas for gradient descent are as follows:
<p align="center">
  <img width="300" height="400" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/gd_form.jpeg">
</p>

Note that the initial learning rate should be carefully chosen as it influences convergence and speed. It is usually set to decrease during the training process to prevent it missing the minimum.

The idea of back propagation for fitting a neural network is also very similar to gradient descent.

