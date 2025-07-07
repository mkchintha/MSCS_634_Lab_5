# Lab 5: Clustering Techniques Using DBSCAN and Hierarchical Clustering
**Course**: 2025 Summer - Advanced Big Data and Data Mining (MSCS-634-M40) - Full Term
**Student Name**: Murali Krishna Chintha  

---

## Overview  
This lab focuses on the application and evaluation of two unsupervised clustering algorithms—Hierarchical Clustering and DBSCAN—on the Wine dataset from the `sklearn.datasets` module. The primary objective is to gain practical experience in:

- Preprocessing and standardizing real-world datasets.
- Applying and visualizing clustering algorithms.
- Interpreting clustering structures using dendrograms and scatter plots.
- Evaluating cluster quality using appropriate metrics.

---

## Objectives  
- To explore the structure of the Wine dataset through descriptive statistics and visualization.  
- To implement Agglomerative Hierarchical Clustering and DBSCAN.  
- To analyze the impact of different parameter settings on clustering outcomes.  
- To assess clustering performance using Silhouette Score, Homogeneity Score, and Completeness Score.  
- To compare and contrast the behavior and suitability of the two clustering methods.

---

## Methodology  

### 1. Data Preparation  
The Wine dataset, consisting of 178 samples and 13 numerical features, was standardized using `StandardScaler` to ensure equal feature contribution in distance-based clustering algorithms.

### 2. Hierarchical Clustering  
Agglomerative clustering was applied using various values for `n_clusters`. Cluster quality was assessed visually and through dendrogram analysis to identify natural groupings and separation thresholds.

### 3. DBSCAN Clustering  
DBSCAN was applied using different combinations of `eps` and `min_samples`. The algorithm's ability to detect arbitrary shaped clusters and noise was explored. Evaluation metrics were computed to understand clustering effectiveness.

---

## Key Findings  

### Hierarchical Clustering  
- Optimal cluster formation was observed when `n_clusters=3`, aligning with the known class structure of the dataset.  
- The dendrogram provided a clear visual hierarchy and informed the cluster cut-off decision.  
- Suitable for smaller datasets where interpretability and cluster hierarchy are essential.  

### DBSCAN  
- Demonstrated strong performance in identifying dense regions and handling noise.  
- Effective clustering observed for `eps=1.0` and `min_samples=3`.  
- Sensitive to parameter changes; improper settings led to either over-clustering or excessive noise.  

---

## Comparative Summary  

| Criteria                  | Hierarchical Clustering         | DBSCAN                               |
|---------------------------|----------------------------------|----------------------------------------|
| Parameter Requirement     | Requires `n_clusters`           | Requires `eps` and `min_samples`       |
| Noise Handling            | Limited                         | Excellent                              |
| Cluster Shape Flexibility | Mostly convex clusters          | Arbitrary shapes                       |
| Scalability               | Less suitable for large datasets| Scales better                          |
| Interpretability          | High (via dendrogram)           | Moderate (requires tuning)             |

---

## Evaluation Metrics  
- **Silhouette Score**: Evaluated intra-cluster cohesion and inter-cluster separation.  
- **Homogeneity Score**: Assessed if each cluster contained only members of a single class.  
- **Completeness Score**: Measured if all members of a class were assigned to the same cluster.

---

## Conclusion  
Hierarchical Clustering and DBSCAN both offer valuable insights into the underlying structure of unlabeled data, though their applicability varies with dataset size, noise levels, and desired interpretability. Hierarchical clustering is well-suited for smaller, well-behaved datasets with a need for hierarchical analysis. DBSCAN provides robust performance in detecting arbitrarily shaped clusters and noise, but requires careful parameter selection.

---

## Repository Contents  
- `Lab5_Clustering_Wine.ipynb` – Jupyter Notebook containing full implementation, visualizations, and analysis.  
- `README.md` – Documentation outlining the objective, methodology, and results of the lab.
