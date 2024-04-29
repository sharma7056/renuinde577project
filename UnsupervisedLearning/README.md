# Unsupervised Learning

There are two unsupervised learning algorithm performed in this sub-repository. The K Means Clustering algorithm is coded from scratch. 

Contents of **Unsupervised Learning**:
* [K Means Clustering](https://github.com/ppunia74/INDE-577_Fall2022/tree/main/UnsupervisedLearning/K%20Means%20Clustering)

---

**Unsupervised Learning**

Unsupervised learning is used to find underlying patterns in data, and involves finding structures and relationships from inputs. This is helpful when we have unlabeled data or aren't sure which outputs are meaningful. There is a set of data that is **unlabeled** to learn from, with the goal of identifying patterns in that data. In contrast to supervised learning, which focuses on labels, unsupervised learning focuses on **features** of the data. 

![image](https://github.com/ppunia74/INDE-577_Fall2022/blob/main/UnsupervisedLearning/Image/unsup_header.png)


The outcome of an unsupervised learning model involves grouping observations into distinct clusters (clustering) or establishing rules to discern associations among variables (association). With extensive datasets, maintaining training datasets as compact and effective as possible is crucial. Unsupervised learning algorithms can also employ "dimensionality reduction" to represent dataset information with only a fraction of its original content, often integrated as part of preprocessing steps.

Unsupervised learning offers data scientists the capability to undertake more intricate processing tasks in contrast to supervised learning. It possesses greater potency as it can uncover patterns within a dataset that may elude human observation. However, unsupervised learning can also exhibit greater unpredictability when compared to other methods such as deep learning and reinforcement learning. 

Variables:
- features

Types of Algorithms:
- **Dimensionality Reduction**
  - goal: combine parts of data in unique ways to convey meaning in less space
  - e.g. analyzing high-resolution images by appropriately reducing their resolution.
  - common algorithms: principal component analysis (PCA), singular-value decomposition (SVD)
- **Clustering**
  - goal: Identify similarities or patterns within observed data and organize them into clusters or subgroups that exhibit maximum similarity within the group and distinctiveness from data in other clusters.
  - e.g. detecting groups of similar visitors to a blog (40% male comic book lovers who read in the evening vs 20% young sci-fi lovers who visit on weekends)
  - common algorithms: K-means clustering, hierarchical clustering, probabilistic clustering
- **Association**
  - goal: Detect sequences and novel insights among different objects within a set. In this scenario, the identified pattern manifests as a rule (e.g., if this, then that).
  - e.g. analyzing supermarket data and finding that people who buy bbq sauce and potato chips tend to also buy steak
  - common algorithms: A priori algorithm, frequent pattern (FP) growth algorithm, rapid association rule mining (RARM), ECLAT algorithm


![image](https://github.com/ppunia74/INDE-577_Fall2022/blob/main/UnsupervisedLearning/Image/unsup_cat.png)