

## DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

DBSCAN is a popular clustering algorithm that is part of the unsupervised learning techniques in data mining and machine learning. Unlike centroid-based algorithms like K-means, DBSCAN categorizes data points into clusters based on their density.


### Key Features of DBSCAN

- **Density-based**: Clusters are defined as high-density areas separated by low-density areas. This allows DBSCAN to find clusters of arbitrary shapes, which is a significant advantage over algorithms that define clusters as spherical shapes.

- **Handles noise**: DBSCAN effectively identifies and separates outliers (noise) from core clusters, improving the robustness of the clustering results.

- **Minimal input parameters**: DBSCAN requires two parameters:
  - `eps` (epsilon): The maximum distance between two points for one to be considered as in the neighborhood of another.
  - `min_samples`: The minimum number of points required to form a dense region (a cluster).

### Advantages of DBSCAN

- **No need to specify cluster count**: Unlike K-means, DBSCAN does not require the number of clusters to be specified in advance.
- **Flexibility in shape and size of clusters**: Can discover clusters of varying and non-spherical shapes.
- **Robustness to outliers**: Effectively differentiates outliers from core and border points in a dataset.

### How DBSCAN Works

1. **Classification of Points**: Points are classified into three types:
   - Core Points: A point is a core point if at least `min_samples` points are within `eps` distance from it.
   - Border Points: A point is a border point if it is not a core point itself, but is in the neighborhood of a core point.
   - Noise Points: Points that are neither core nor border points.

2. **Growing Clusters**: Starting from a core point, a cluster is expanded by recursively adding all directly density-reachable points to the cluster. This process continues until no new points can be added.

### Limitations of DBSCAN

- **Parameter sensitivity**: Choosing an appropriate value for `eps` and `min_samples` can be challenging without domain knowledge or heuristic techniques.
- **Performance issues**: Can perform poorly if clusters vary widely in density, as uniform parameter settings might not be suitable across all clusters.


---

This sub-repository implements DBSCAN to solve classification problems.

Contents of **DBSCAN**

- [DBSCAN](https://github.com/sharma7056/renuinde577project/blob/main/UnsupervisedLearning/DBSCAN/DBSCAN.ipynb)