### Support Vector Machines (SVMs)

The Support Vector Machine (SVM) algorithm is a supervised machine learning technique applicable to both regression and classification assignments. SVM identifies a hyperplane within an N-dimensional space (where N denotes the number of features) to segregate diverse data types. To establish boundaries, it determines the maximum distance between the nearest points of two classes, defining the optimal decision boundary known as support vectors. The area between the decision boundary and the support vectors is termed the margin. Therefore, SVM is primarily employed for binary classification tasks and exhibits robust performance when handling linearly separable data. We use **Kernalized SVM** for non-linearly separable data. SVM is more often used for classification, but it can also be used for regression. The advantage of SVM is its significant accuracy with less computational power.

The working flow of a simple SVM algorithm can be simply summarized in two steps:

* Find boundaries (or hyperplane) that correctly separate the classes for the training data
* Picks the one that has the maximum distance from the closest data points

## Kernel Trick

The kernel trick is a critical enhancement for SVMs, allowing them to perform well in non-linear scenarios. Kernels transform the original input data into a higher-dimensional space where a linear separator might be found. Common kernels include:

Linear Kernel: No transformation is needed, suitable for linearly separable data.
Polynomial Kernel: Transforms data by considering polynomial combinations of features.
Radial Basis Function (RBF): Can handle complex, nonlinear relationships by measuring the distance between points in a transformed feature space.
Sigmoid Kernel: Similar to the activation function used in neural networks.

- Multiclass Classification
While inherently designed for binary classification, SVM can be extended to handle multiple classes using strategies such as:
One-vs-All (OvA): Trains a single classifier per class, with the samples of that class as positive samples and all other samples as negatives.
One-vs-One (OvO): Trains a classifier for every pair of classes. A voting scheme is then used to decide the most voted class


---

This sub-repository demonstrates the implementation of Support Vector Machines algorithms.

Contents of **Support Vector Machines (SVMs)**

* [Image](https://github.com/sharma7056/renuinde577project/tree/main/SupervisedLearning/9%20-%20Support%20Vector%20Machines%20(SVMs)/Image): contains images used in README
* [SVM](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/9%20-%20Support%20Vector%20Machines%20(SVMs)/SVM.ipynb): Jupyter notebook file performs the SVM algorithm to train a classifier to automatically annotate single-cell RNA-seq data.

![iamge](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/9%20-%20Support%20Vector%20Machines%20(SVMs)/Image/SVM.png)


### Dataset

* Processed 3k PBMCs Dataset:

The [Processed 3k PBMCs](https://scanpy.readthedocs.io/en/stable/generated/scanpy.datasets.pbmc3k_processed.html) Dataset is loaded from [scanpy.datasets](https://scanpy.readthedocs.io/en/stable/api.html#module-scanpy.datasets). The Processed 3k Peripheral Blood Mononuclear Cells (PBMCs) Dataset consists of 3k PBMCs from a Healthy Donor and are freely available from [10x Genomics](https://support.10xgenomics.com/single-cell-gene-expression/datasets/1.1.0/pbmc3k). There are 2,700 single cells that were sequenced on the Illumina NextSeq 500.
