# K Nearest Neighbors (KNN)

This sub-repository demonstrates the implementation of K Nearest Neighbors to solve classification problems.

Contents of **K Nearest Neighbors (KNN)**

* [Image](https://github.com/ppunia74/INDE-577_Fall2022/tree/main/SupervisedLearning/6%20-%20K%20Nearest%20Neighbors%20(KNN)/Image): contains images. 
* [Data](https://github.com/ppunia74/INDE-577_Fall2022/tree/main/SupervisedLearning/6%20-%20K%20Nearest%20Neighbors%20(KNN)/Data): contains dataset used in this module. 
* [KNN.ipynb](https://github.com/ppunia74/INDE-577_Fall2022/blob/main/SupervisedLearning/6%20-%20K%20Nearest%20Neighbors%20(KNN)/KNN.ipynb): Jupyter notebook implementations of
  * 1) Building KNN algorithm from scratch and performing KNN using Hawks Dataset to classify the hawks species
  * 2) Compare the built algorithm with the *KNeighborsClassifier* from sklearn


### A Short Summary

<img src="Image/KNN-regression.gif" alt="Drawing" style="width: 500px;"/>

# K Nearest Neighbors (KNN)

K Nearest Neighbors (KNN) represents a straightforward classification algorithm that retains all available cases and categorizes new data based on their similarity to existing cases. Its primary utilization lies in classifying data by assessing their resemblance to neighboring instances. The application spectrum spans from recommendation systems and anomaly detection to image and text classification. Although less prevalent, KNN can also serve for regression tasks.

### Idea

In short, KNN essentially entails aggregating a majority vote from the K most akin (i.e., nearest) instances to a given "unseen" observation. Put differently, data sharing similar features are expected to cluster closely together in space.
<img src="Image/KNN-voting.png" alt="Drawing" style="width: 500px;"/>

### Generalized Algorithm:

1. Load training and testing datasets
2. Specify/choose the value of k (K should be odd for classification)
  influence on the result, while larger values of K will have smoother decision boundaries (meaning lower variance but increased bias... and are computationally expensive). 
   - Alternatively, you have the option of employing cross-validation: segment a portion of the training dataset for cross-validation. Extract a small subset from the training data, referred to as the "validation" dataset. Then, utilize this dataset to assess various potential values of K. This involves predicting labels for each instance in the validation set using different values of K, such as K = 1, K = 2, K = 3, and so forth. Subsequently, determine which value of K yields the optimal performance on the validation set and adopt that value as the final setting.
   - In general, choosing the value of k is k = sqrt(N), where N is the number of samples in the training dataset
3. For each point in the test data:
   a. Calculate the distance between the point and each point in the dataset 
   Two-Dimension formula:
   <img src="http://chart.googleapis.com/chart?cht=tx&chl= d(p, q) = \sqrt {(p_1-q_1)^2+(p_2-q_2)^2}" style="border:none;">
   n-Dimention formular:
   <img src="http://chart.googleapis.com/chart?cht=tx&chl=d(p, q) = \sqrt {(p_1-q_1)^2+(p_2-q_2)^2+...+(p_n-q_n)^2}=\sqrt {\sum \limits_{i=1}^{n}(p_i-q_i)^2}" style="border:none;">
   
   b. Sort the values in ascending order based on distances
   c. Find the top k values from the sorted list
   d. Find the frequency (statistical [mode](https://en.wikipedia.org/wiki/Mode_(statistics)) of the labels of the top k values
   e. Assign the mode to the test data point
   f. The assigned value is the classified (classification) or predicted (regression) value for that particular datapoint.

### How should we measure error?

<img src="http://chart.googleapis.com/chart?cht=tx&chl=E = \frac {1}{M} \sum \limits_{i=1}^{M} \left(y_i \ne \hat {y_i} \right)" style="border:none;">

---

### Datasets

I use Hawks data to implement K Nearest Neighbors (KNN) algorithm:
  
* Hawks Dataset:

The Hawks dataset has 908 cases and 19 columns. The data were collected by the students and faculty from Cornell College at Lake MacBride near Iowa City, Iowa. There are three different species of hawks: Red-tailed, Sharp-shinned, and Cooper's hawks.