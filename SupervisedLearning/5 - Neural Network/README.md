# Neural Network (Multilayer Perceptron Learning Algorithm)


The Multilayer Perceptron Learning algorithm, also known as a neural network, is extensively employed for tasks such as image recognition, speech recognition, and natural language processing. The fundamental idea behind neural networks is to identify underlying patterns within a dataset by simulating the operations of the human brain. Neural networks consist of interconnected neurons arranged in layers, with each neuron applying a function to its inputs to compute outputs. These neurons are associated with weights (w) that signify the relative significance of each input compared to others.

<img src="Image/neural-network.png" alt="Drawing" style="width: 500px;"/>

Neural network algorithm has following components:

* Input Nodes (input layer): no computation is done in this layer, Input nodes passes the initial data into the system for further processing by subsequent layers of artificial neurons. A block of nodes is also called a **layer**.
* Hidden nodes, situated within the hidden layer of a neural network, serve as sites for intermediate processing and computation. Following these calculations, these nodes transmit weights—either signals or information—from the input layer to the subsequent layer, which may be another hidden layer or the output layer. Additionally, it's feasible to construct a neural network devoid of a hidden layer.
* Output nodes (output layer): uses an activation function to map information to the desired output format
* Connections and weights: a *network* consists of connects that transfer the output from neuron i to neuron j, assigned weight W_ij
* The Activation Function, also referred to as the transfer function, determines the output of a node based on a given set of inputs. While its operation resembles that of a single perceptron, the capacity to employ nonlinear activation functions enables networks to tackle complex problems with a limited number of nodes.
* Learning rule: algorithm which modifies the parameters of the neural network, in order for a given input to the network to produce a favored output. This *learning* process is often just modifying the weights and thresholds

---


This sub-repository implements a Multilayer Perceptron Learning Algorithm aka neural network on images to predict the labels.

Contents of **Neural Network**

* [Image](https://github.com/sharma7056/renuinde577project/main/SupervisedLearning/5%20-%20Neural%20Network/Image): folder contains images used in README
* [MLP_MNIST.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/5%20-%20Neural%20Network/MLP_MNIST.ipynb): Jupyter notebook file contains
  * a. Building Multilayer Perceptron Learning algorithm from scratch
  * b. Performing multilayer perceptron algorithm using MNIST Dataset to classify the handwritten digits
* [MLP.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/5%20-%20Neural%20Network/MLP.ipynb): Jupyter notebook file contains
  * a. Introduction of the perceptron algorithm
  * b. Building Multilayer Perceptron Learning algorithm from scratch
  * c. Performing the multilayer perceptron algorithm using Fashion MNIST dataset to classify fashion categories
  * d. Increase the number of nodes in the hidden layers and compare
  * e. Add ReLU function as another activation function and compare


### Datasets

* MNIST Dataset

The MNIST Dataset is loaded from [*keras.dataset*](https://keras.io/api/datasets/). It consists of 70000 28 <img src="https://latex.codecogs.com/svg.image?\times" title="\times" /> 28 pixel images of hand written digits, 60000 of which are typically used as labeled training examples, where the other 10000 are used for testing your learning model on.

* Fashion MNIST Dataset

The Fashion MNIST Dataset is also loaded from [*keras.dataset*](https://keras.io/api/datasets/). It consists of 70000 28 <img src="https://latex.codecogs.com/svg.image?\times" title="\times" /> 28 grayscale images of 10 fashion categories, 60000 of which are typically used as labeled training examples, where the other 10000 are used for testing your learning model on.
