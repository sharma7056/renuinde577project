# Linear Regression

![image](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/Linear%20Regression/Image/linear-regression.png)

[Linear regression](https://en.wikipedia.org/wiki/Linear_regression) a traditional supervised model with a history spanning over two centuries, combines a designated set of input values (x) to predict an output (y). Both input and output variables are numerical. The linear equation assigns a unique scale factor (often represented as "m") to each input value, along with a constant term (often represented as "b"). This constant provides the line with an additional degree of freedom, allowing it to vertically shift on a two-dimensional plane. Thus, we have the familiar equation from algebra: **y = mx + b** (below). In the image above, the red line is referred to as the **line of best fit** described by this equation.

![image](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/Linear%20Regression/Image/regression-equation.jpeg)

In higher dimensions, the line is called a plane or "hyperplane", and simply adds additional terms to the equation, as written below:

$$y = \beta_0 + \beta_1X_1 + \beta_2X_2 + ... + \beta_nX_n$$


When the coefficient of one of these terms becomes zero, it effectively removes the influence of the input variable on the model.

Some of the commonly used linear regression based methods::
- **Simple linear regression:** The model has a single input variable and employs statistical methods to estimate coefficients. This entails calculating statistical metrics such as means, standard deviations, correlations, and variances. 
- **Ordinary least squares** ("or ordinary least squares linear regression" or "least squares regression"): This is the widely used. When there is more than one input, OSLR can estimate the values of the coefficients. The [Gauss-Markove theorem](https://en.wikipedia.org/wiki/Gauss%E2%80%93Markov_theorem) ensures this method minimizes the "sum of the squared residuals." Essentially a regression line through the data, calculate the distance from each data point to the regression point, square it, and sum all the squared errors together. This method uses the matrix and linear algebra to estimate the optimal values for the coefficients. It requires memory to fit the data and perform matrix operations but is very fast to calculate.
- **Gradient Descent:** This approach is further discussed [elsewhere](https://github.com/sharma7056/renuinde577project/blob/main/supervised%20learning/1%20-%20gradient%20descent/README.md) in this repository, but in short this method starts with random values for the coefficients, then iteratively works to minimize the error of the model.
- **Regularization:** These models aim to minimize the sum of squared errors on training data using ordinary least squares, while simultaneously diminishing model complexity. They prove advantageous when input variables exhibit collinearity, a scenario where ordinary least squares would lead to overfitting the training data.
  - [LASSO Regression](https://en.wikipedia.org/wiki/Lasso_(statistics)) (aka Least Absolute Shrinkage and Selection Operator, or L1 regularization): modifies ordinary least squares to also minimize the absolute sum of the coefficients by pulling data values towards the mean. This algorithm is useful in feature selection and applies a "penalty" to features that do not benefit the prediction
  - [Ridge Regression](https://en.wikipedia.org/wiki/Tikhonov_regularization) (aka L2 Regularization): modifies ordinary least squares to minimize the squared absolute sum of the coefficients and compensate for large variation in input data. It includes a penalty term (often denoted lambda) that shrinks the weight of probability theta
  - [Elastic Net](https://en.wikipedia.org/wiki/Elastic_net_regularization): is a combination of LASSO and Ridge Regression that adjusts both the weight of the features and probability


Please read [Linear_Reression.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/Linear%20Regression/Linear_Regression.ipynb) to learn more details.

---

This sub-repository demonstrates the implementation of Linear Regression algorithm on the time series financial data.

Contents of **Linear Regression**

* [Image](https://cdn.analyticsvidhya.com/wp-content/uploads/2021/05/2.3.png): contains images used in the sub-repository
* [Data](https://github.com/sharma7056/renuinde577project/tree/main/SupervisedLearning/3%20-%20Linear%20Regression/Datasets) contains dataset used in the regression.
* [Linear_Reression](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/3%20-%20Linear%20Regression/Linear_Regression.ipynb): Jupyter notebook file contains
  * a. Introduction of Linear Regression
  * b. Building Linear Regression algorithm from scratch and implement Linear Regression to predict the car price, and predict the future prices
  * c.  Feature Engineering