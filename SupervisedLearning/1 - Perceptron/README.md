# Perceptron

![image](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/1%20-%20Perceptron/Image/perceptron.jpeg)


The perceptron, a supervised binary classifier, operates as a single-layer neural network. Within the perceptron algorithm, each neuron receives inputs, assigns weights to them individually, computes their sum, and then applies a nonlinear function (activation function) to generate an output. Essentially, it functions as a mathematical model that delineates a boundary to distinguish between two groups in a given space.

The perceptron comprises four essential components: input values, weights and bias, the weighted sum (net sum), and the activation function.

### Weighted Sum

The weighted sum represents the combined input to the neuron from all previous layers, adjusted by the respective weights and added to a bias value. This sum is then fed into the activation function to produce the neuron's output. The weighted sum, `z`, is calculated by multiplying each input feature in `X` by its corresponding weight from `w` and then summing all these products together, adding the bias `b` at the end:

z = w^T X^i + b = w_1 X^i_1 + w_2 X^i_2 + ... + w_n X^i_n + b


### Activation Function

The activation function in a perceptron decides the output based on the weighted sum. It introduces non-linearity to the model, enabling it to learn more complex patterns. The sign function is typically used in perceptrons, which outputs one of two classes based on the sign of the input.

The output of the perceptron, `y_hat^i`, is determined by the sign of the weighted sum:

y_hat^i = sign(z) = {
  1  if z > 0
 -1  if z <= 0
}

### Loss function

The loss function quantifies the error between the predicted outputs and the actual labels during training. It guides the training process by indicating how well the model is performing, with the goal being to minimize this error through adjustments in the model's weights. The perceptron loss for an individual example is given by the squared error loss:

L(w, X^i) = 0.5 * (y_hat^i - y^i)^2


To train the perceptron, we need to update its weights based on the errors made by the model. This is done using stochastic gradient descent. The gradient of the loss function with respect to the weights is computed, and then the weights are updated in the direction that minimally reduces the loss. The approximate gradient of the loss with respect to the weights is calculated as:

∇L(w, X^i) = (y_hat^i - y^i) * X^i

The weight update rule is then defined as:

w_(n+1) = w_n - α * ∇L(w, X^i)


---


This sub-repository illustrate the use of Perceptron algorithm to solve classification problems.

Contents of **Perceptron**

* [Data](https://github.com/sharma7056/renuinde577project/tree/main/SupervisedLearning/1%20-%20Perceptron/Data): contains all data files used in this module
* [Perceptron.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/1%20-%20Perceptron/Perceptron.ipynb): Jupyter notebook file contains
  * a. Introduction of the perceptron algorithm
  * b. Building Perceptron algorithm from scratch
  * c. Implement the perceptron algorithm using banknote authentication dataset to classify forged and genuine currency


### Dataset

Following datasets is used to implement Perceptron algorithm:

* Banknote Authentication Dataset:

The banknote authentication dataset contains data extracted from images that were taken from genuine and forged banknote-like specimens. The final images have 400x 400 pixels. Due to the object lens and distance to the investigated object gray-scale pictures with a resolution of about 660 dpi were gained. Wavelet Transform tool were used to extract features from images.
