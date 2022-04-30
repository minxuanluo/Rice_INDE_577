<h1 align="center"> Neural Network </h1>  

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/neural network.png">
</p>

<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Introduction"> ➤ Introduction</a></li>
    <li><a href="#Feed Forward Neural Network"> ➤ Feed Forward Neural Network</a></li>
    <li><a href="#Convolutional Neural Network"> ➤ Convolutional Neural Network</a></li>
    <li><a href="#Recurrent Neural Network and Transformer"> ➤ Recurrent Neural Network and Transformer</a></li>
    <li><a href="#Dataset"> ➤ Dataset</a></li>
  </ol>
</details>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Introduction -->
<h2 id="Introduction"> Introduction</h2>

<p align="justify"> 

  Here we refer to multi-layer perceptrons when talking about 'feedforward neural network'. Understanding some aspects about how multi-layer perceptron works lays the foundation for many different neural networks, such as back propagation, optimizers, activation function, and loss function.
  
  Though we can use neural networks for regression or classification problems on tabular data (several explanatory (x) variables and target variable (y)), usually I prefer use random forest or xgboosting for those problems. This is because Neural Network is a very complex model with millions of parameters to estimate. This makes them relatively hard to interpret compared to other machine learning algorithms. This also makes them prune to overfitting - and needs the complement of regularization techniques.
  
  Neural Networks are most famous for its application in computer vision and NLP. In these cases we will have data in the format of images or texts. CNN and Recurrent Neural Network (then Attention Mechanism and Transformer) are suitable for these tasks, respectively.

  
  * **Back Propagation**:

  <p align="center">
  <img width="550" height="500" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/backprop.png">
</p>

(source: http://www.cs.put.poznan.pl/pliskowski/pub/teaching/eio/lab1/eio-supplementary.pdf)

  * **Optimizers**: 
  <p align="center">
  <img width="500" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/optimizer.png">
</p>

(source: https://arxiv.org/pdf/1910.05446.pdf)
  
  * **Activation Function**: 
  
  A few of the most common functions and their uses are included in the chart below:
  
  <p align="center">
  <img width="500" height="400" src="https://www.simplilearn.com/ice9/free_resources_article_thumb/Perceptron/Perceptron_36.jpg">
</p>
  
  * **Loss function**: 
  * Regression Loss Functions
  
    Mean Squared Error Loss
    
    Mean Squared Logarithmic Error Loss
    
    Mean Absolute Error Loss

  * Binary Classification Loss Functions
  
    Binary Cross-Entropy
    
    Hinge Loss
    
    Squared Hinge Loss
    
   * Multi-Class Classification Loss Functions
   
      Multi-Class Cross-Entropy Loss
    
      Sparse Multiclass Cross-Entropy Loss
    
      Kullback Leibler Divergence Loss

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Feed Forward Neural Network -->
<h2 id="Feed Forward Neural Network"> Feed Forward Neural Network</h2>

 <p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/neural network.png">
</p>

Multiple layers of computational units, usually interconnected in a feed-forward way. Each neuron in one layer has directed connections to the neurons of the subesquent layer. Many applications of these apply a sigmoid function as an activation. One particularly useful feature is MLP's ability to learn nonlinear representations because often data is not linearly separable.
 
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- Convolutional Neural Network -->
<h2 id="Convolutional Neural Network"> Convolutional Neural Network</h2>

<p align="center">
  <img width="460" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/cnn.jpeg">
</p>

<p align="center">
</p>

The convolutional layer is the first layer of a convolutional network. While convolutional layers can be followed by additional convolutional layers or pooling layers, the fully-connected layer is the final layer. With each layer, the CNN increases in its complexity, identifying greater portions of the image. Earlier layers focus on simple features, such as colors and edges. As the image data progresses through the layers of the CNN, it starts to recognize larger elements or shapes of the object until it finally identifies the intended object.

The convolutional layer is the core building block of a CNN, and it is where the majority of computation occurs. It requires a few components, which are input data, a filter, and a feature map. Let’s assume that the input will be a color image, which is made up of a matrix of pixels in 3D. This means that the input will have three dimensions—a height, width, and depth—which correspond to RGB in an image. We also have a feature detector, also known as a kernel or a filter, which will move across the receptive fields of the image, checking if the feature is present. This process is known as a convolution.

The feature detector is a two-dimensional (2-D) array of weights, which represents part of the image. While they can vary in size, the filter size is typically a 3x3 matrix; this also determines the size of the receptive field. The filter is then applied to an area of the image, and a dot product is calculated between the input pixels and the filter. This dot product is then fed into an output array. Afterwards, the filter shifts by a stride, repeating the process until the kernel has swept across the entire image. The final output from the series of dot products from the input and the filter is known as a feature map, activation map, or a convolved feature.

<p align="center">
  <img width="400" height="200" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/filter.png">
</p>

(source: https://www.ibm.com/cloud/learn/convolutional-neural-networks)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- Recurrent Neural Network and Transformer -->
<h2 id="Recurrent Neural Network and Transformer"> Recurrent Neural Network and Transformer</h2>

<p align="center">
  <img width="450" height="300" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/recurrent.png">
</p>

A recurrent neural network (RNN) is a type of artificial neural network which uses sequential data or time series data. These deep learning algorithms are commonly used for ordinal or temporal problems, such as language translation, natural language processing (nlp), speech recognition, and image captioning; they are incorporated into popular applications such as Siri, voice search, and Google Translate. Like feedforward and convolutional neural networks (CNNs), recurrent neural networks utilize training data to learn. They are distinguished by their “memory” as they take information from prior inputs to influence the current input and output. While traditional deep neural networks assume that inputs and outputs are independent of each other, the output of recurrent neural networks depend on the prior elements within the sequence. 

(source: https://www.ibm.com/cloud/learn/recurrent-neural-networks)

<p align="center">
  <img width="600" height="400" src="https://github.com/minxuanluo/INDE577/blob/main/Classification/images/transformer.svg">
</p>

Like recurrent neural networks (RNNs), transformers are designed to handle sequential input data, such as natural language, for tasks such as translation and text summarization. However, unlike RNNs, transformers do not necessarily process the data in order. Rather, the attention mechanism provides context for any position in the input sequence. For example, if the input data is a natural language sentence, the transformer does not need to process the beginning of the sentence before the end. Rather it identifies the context that confers meaning to each word in the sentence. This feature allows for more parallelization than RNNs and therefore reduces training times.

(source: https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)#:~:text=A%20transformer%20is%20a%20deep,and%20computer%20vision%20(CV))

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<!-- Dataset -->
 I used a build-in image dataset in sklearn, 'The Labeled Faces in the Wild face recognition dataset'. The targets(classes) are ['Ariel Sharon' 'Colin Powell' 'Donald Rumsfeld' 'George W Bush'
 'Gerhard Schroeder' 'Hugo Chavez' 'Junichiro Koizumi' 'Tony Blair'], and the images have shape (1348, 62, 47), where the first dim is num_samples. For this image recognition task, I compare the performances of MLP (without/with dropout layer) and a convolutional network.
