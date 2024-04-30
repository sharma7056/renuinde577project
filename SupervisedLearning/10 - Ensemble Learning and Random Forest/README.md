# Ensemble Learning and Random Forest

![image](https://github.com/cissyyang1014/DataScience_and_MachineLearning/blob/main/SupervisedLearning/Ensemble%20Learning%20and%20Random%20Forest/Image/10image001.png)

# Ensemble Learning

Ensemble learning models generate predictions by amalgamating multiple individual models. This fusion of diverse models enhances the algorithm's overall performance, rendering ensemble models more adaptable with reduced bias and decreased sensitivity to data fluctuations. Ensemble algorithms operate under the assumption that all predictions are entirely independent.


![image](https://miro.medium.com/max/2000/1*bUySDOFp1SdzJXWmWJsXRQ.png)

### Hard Voting Classifier

The Hard Voting Classifier represents a straightforward ensemble learning approach. It employs multiple models to generate predictions for each data point, treating the predictions from each model as individual votes. The final prediction is determined by selecting the outcome that receives the majority of votes from the models.

### Bagging (Bootstrap Aggregation)

This technique involves training a collection of individual models either sequentially or in parallel, utilizing random subsets of the data. Each model in this approach learns from the errors of its predecessor. Analogous to the hard voting classifier, the bagging algorithm aggregates the votes and designates the class with the highest number of votes as the ultimate prediction.

# Random Forest

In a single decision tree model typically has high variance and has performance similar to many other models. However, one way to improve performance is to produce many variants of a single decision tree by selecting every time a different subset of the same training set in the context of randomization-based ensemble methods.

![image](https://miro.medium.com/max/2000/1*jXkT3mj1mCqMaX5SqU1wNw.png)

Random forest method is an extension of decision trees, which belongs to the a class of machine learning algorithms called **ensemble methods**. Random forest utilizes multiple subsets drawn from the training data, training a set of decision tree classifiers to generate individual predictions based on these distinct subsets. It accommodates both categorical and numerical variables, exhibiting less sensitivity to scaling and requiring less computational resources compared to SVM. Random forest also performs effectively with missing data and is less prone to overfitting without necessitating hyperparameter tuning. Each tree contributes a vote, and the prediction receiving the highest number of votes is chosen as the final prediction.

![image](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/10%20-%20Ensemble%20Learning%20and%20Random%20Forest/Image/random-forest-classifier.png)


Generalized Algorithm
1. Select n (e.g. 100) random subsets from the training data
2. Train n (e.g. 100) decision trees
   - one random subset is used to train one decisions tree
   - the optimal splits for each decision tree are based on a random subset of features (e.g. 10 features in total, randomly select 5 out of 10 features to split)
 1. Each individual tree predicts the records/candidates in the test set, independently
 2. Make the final prediction
    - For each candidate in the test set, random forest uses the class (e.g. cat or dog) with the majority vote as this candidate's final prediction

The core tenet of ensemble methods revolves around randomness. When building a tree, three key decisions must be made:
- the approach for splitting the leaves
- the predictor type employed in each leaf
- the method for introducing randomness into the tree, such as bagging or bootstrapping

There are a few stopping criteria:
- minimum number of samples in a terminal node to allow it to split
- minimum number of samples in a leaf node when the terminal node is split
- maximum tree depth, i.e. the maximum number of levels a tree can grow
- Tree accuracy (defined by the Gini Index) is less than a fixed threshold

---

This sub-repository demonstrates the implementation of Ensemble Learning algorithms (including Random Forest) to solve classification problems.

Content of **Ensemble Learning and Random Forest**
* [Data](https://github.com/sharma7056/renuinde577project/tree/main/SupervisedLearning/10%20-%20Ensemble%20Learning%20and%20Random%20Forest/Data): contains datasets used in this module
* [Ensemble_Learning_makemoons.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/10%20-%20Ensemble%20Learning%20and%20Random%20Forest/README.md): Jupyter notebook file performing Random Forest and two other different Ensemble Learning algorithms using the make_moons Dataset from sklearn (artificial dataset)
* [Ensemble_Learning_and_Random_Forest.ipynb](https://github.com/sharma7056/renuinde577project/blob/main/SupervisedLearning/10%20-%20Ensemble%20Learning%20and%20Random%20Forest/Ensemble_Learning_and_Random_Forest.ipynb): Jupyter notebook file containing
  * a. Introduction of the Ensemble Learning algorithm and the Random Forest algorithm
  * b. Performing Random Forest algorithm and three other different Ensemble Learning algorithms using penguins dataset to classify penguins species.



### Datasets

There are two datasets used to implement Ensemble Learning algorithms (including Random Forest):

* make_moons Dataset:

The [make_moons](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_moons.html) dataset is an artificial data loaded from [sklearn.dataset](https://scikit-learn.org/stable/modules/classes.html?highlight=dataset#module-sklearn.datasets). It can make two interleaving half circles. Adjusting the parameters (e.g., `noise`) can change the data distribution.

* Penguins Dataset:

The Penguins Dataset contains size measurements for three penguin species observed on three islands in the Palmer Archipelago, Antarctica. These data were collected from 2007 - 2009 by Dr. Kristen Gorman's team. It consists of 344 rows and 7 columns. The three different species of penguins are Chinstrap, Adélie, and Gentoo penguins.
