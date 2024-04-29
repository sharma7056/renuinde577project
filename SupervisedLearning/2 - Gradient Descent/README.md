# Gradient Descent

This sub-repository demonstrates the implementation of Gradient Descent to solve regression problems.

Contents in **Gradient Descent**
* [Data](https://github.com/sharma7056/renuinde577project/tree/main/SupervisedLearning/2%20-%20Gradient%20Descent/Data): folder containing datasets
* [Gradient_Descent.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/2%20-%20Gradient%20Descent/Gradient_Descent.ipynb): Jupyter notebook containing 
  - 1) Introduction of Gradient Descent algorithm
  - 2) Implement:
    * Part 1: 
      * Build the Gradient Descent algorithm from scratch
      * Find a best linear model for a data with 4 data points using the algorithm.
    * Part 2: 
      * Build the Gradient Descent algorithm from scratch
      * Perform the Gradient Descent to find a linear regression model to predict the body mass of penguin by the flipper length
      * Compare the built algorithm with the *LinearRegression* tool from sklearn

![image](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/2%20-%20Gradient%20Descent/Image/GD_2.png)

### A Short Summary

# Gradient Descent

Gradient descent serves as an optimization technique aimed at locating a local minimum of a differentiable function. Its primary application lies in determining parameter values that minimize a given cost function. The basic concept involves iteratively adjusting parameters to progressively approach the local minimum of the function, <img src="https://latex.codecogs.com/svg.image?min_{x&space;\in&space;{R^{n}}}&space;f(x)" title="min_{x \in {R^{n}}} f(x)" />.

Gradient Descent find the local minimum of a function by calculating proportional needed in the opposite of the gradient of the function at the current point. The iterative method updates <img src="https://latex.codecogs.com/svg.image?x" title="x" /> as 

<img src="https://latex.codecogs.com/svg.image?x_{n&plus;1}&space;=&space;x_{n}-\alpha&space;\triangledown&space;f(x_{n})" title="x_{n+1} = x_{n}-\alpha \triangledown f(x_{n})" />, where <img src="https://latex.codecogs.com/svg.image?\alpha" title="\alpha" /> is the step length and <img src="https://latex.codecogs.com/svg.image?\triangledown&space;f(x_n)" title="\triangledown f(x_n)" /> is the gradient of <img src="https://latex.codecogs.com/svg.image?f(x_n)" title="f(x_n)" />.

### Algorithm

When using the Loss function <img src="https://latex.codecogs.com/svg.image?L(w,b)=&space;\frac&space;{1}{2M}&space;\sum_{i=1}^{M}{(wx^i&space;&plus;b&space;-y^i)^2}" title="L(w,b)= \frac {1}{2M} \sum_{i=1}^{M}{(wx^i +b -y^i)^2}" />:

* Step 1: Randomly choose intial <img src="https://latex.codecogs.com/svg.image?w" title="w" /> and <img src="https://latex.codecogs.com/svg.image?b" title="b" /> (<img src="https://latex.codecogs.com/svg.image?w" title="w" />, <img src="https://latex.codecogs.com/svg.image?b" title="b" /> = np.random.rand(2))

* Step 2: Set the MAX_ITER and COUNT

* Step 3: While COUNT < MAX_ITER do 

    - <img src="https://latex.codecogs.com/svg.image?w&space;=&space;w&space;-&space;\alpha&space;\times&space;\frac{\partial&space;L(w,&space;b)}{\partial&space;w}" title="w = w - \alpha \times \frac{\partial L(w, b)}{\partial w}" />
    - <img src="https://latex.codecogs.com/svg.image?b&space;=&space;b&space;-&space;\alpha&space;\times&space;\frac{\partial&space;L(w,&space;b)}{\partial&space;w}" title="b = b - \alpha \times \frac{\partial L(w, b)}{\partial w}" />
    - COUNT += 1


In practice there are two types of gradient descent methods:
- **Batch Gradient Descent** (aka vanilla gradient descent)
  - The algorithm computes the error for each instance in the training dataset but updates the model only after processing all examples.
  - the whole process is called a "training epoch"
  - Advantages: include computational efficiency, a stable error gradient, and consistent convergence.
  - Disadvantages: include the possibility of suboptimal convergence due to the stable error gradient and the necessity for the entire training set to be accessible in memory during the process.

- **Stochastic Gradient Descent**
  - Parameter updates occur individually for each training example.
  - This method can potentially accelerate convergence compared to batch gradient descent, depending on the problem.
  - Advantage: ability to track detailed improvement rates due to frequent updates.
  - Disadvantage: frequent updates increase computational costs and may introduce noisy gradients. 

When there are one or more inputs you can use a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on your training data.

Mean squared error is a common measure of performance:

![image](https://miro.medium.com/max/1013/1*GQ6vjZ9j0K5V7BReHywWAA.png)

Check out [this video](https://youtu.be/IHZwWFHWa-w?t=416) for more information.
