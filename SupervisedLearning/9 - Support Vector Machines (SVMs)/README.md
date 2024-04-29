# Support Vector Machines (SVMs)

Contents of **Support Vector Machines (SVMs)**

* [Image](https://github.com/sharma7056/renuinde577project/tree/main/SupervisedLearning/9%20-%20Support%20Vector%20Machines%20(SVMs)/Image): contains images used in README
* [SVM.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/9%20-%20Support%20Vector%20Machines%20(SVMs)/SVM.ipynb): Jupyter notebook file performs the SVM algorithm to train a classifier to automatically annotate single-cell RNA-seq data.

![iamge](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/9%20-%20Support%20Vector%20Machines%20(SVMs)/Image/SVM.png)

### A Short Summary

# Support Vector Machines (SVMs)

The Support Vector Machine (SVM) algorithm is a supervised machine learning technique applicable to both regression and classification assignments. SVM identifies a hyperplane within an N-dimensional space (where N denotes the number of features) to segregate diverse data types. To establish boundaries, it determines the maximum distance between the nearest points of two classes, defining the optimal decision boundary known as support vectors. The area between the decision boundary and the support vectors is termed the margin. Therefore, SVM is primarily employed for binary classification tasks and exhibits robust performance when handling linearly separable data. We use **Kernalized SVM** for non-linearly separable data. SVM is more often used for classification, but it can also be used for regression. The advantage of SVM is its significant accuracy with less computational power.

The working flow of a simple SVM algorithm can be simply summarized in two steps:

* Find boundaries (or hyperplane) that correctly separate the classes for the training data
* Picks the one that has the maximum distance from the closest data points

---

### Dataset

* Processed 3k PBMCs Dataset:

The [Processed 3k PBMCs](https://scanpy.readthedocs.io/en/stable/generated/scanpy.datasets.pbmc3k_processed.html) Dataset is loaded from [scanpy.datasets](https://scanpy.readthedocs.io/en/stable/api.html#module-scanpy.datasets). The Processed 3k Peripheral Blood Mononuclear Cells (PBMCs) Dataset consists of 3k PBMCs from a Healthy Donor and are freely available from [10x Genomics](https://support.10xgenomics.com/single-cell-gene-expression/datasets/1.1.0/pbmc3k). There are 2,700 single cells that were sequenced on the Illumina NextSeq 500.
