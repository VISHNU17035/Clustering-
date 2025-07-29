# Customer Segmentation using Clustering Algorithms

This repository contains code and analysis for performing customer segmentation using multiple clustering techniques on a shopping mall dataset. The objective is to group customers based on features like age, annual income, and spending score to derive insights for business targeting and strategy.

---

## Dataset

- **Source**: `Customer data_clustering.csv`
- **Attributes**:
  - `CustomerID`
  - `Gender`
  - `Age`
  - `Annual Income (k$)`
  - `Spending Score (1-100)`

---

## Clustering Algorithms Applied

### 1. **K-Means Clustering**
- Selected features: `Gender`, `Age`, `Annual Income`, `Spending Score`
- Optimal clusters: `k=5`
- Evaluation: **Silhouette Score = 0.44**
- Visualization: 2D scatter plot (Income vs. Spending Score)

---

### 2. **K-Medoids Clustering**
- Selected features: `Age`, `Annual Income`, `Spending Score`
- Distance metric: **Manhattan**
- Initialization: 3 randomly chosen medoids
- Evaluation: **Silhouette Score = 0.309**
- Visualization: 2D scatter plot

---

### 3. **DBSCAN (Density-Based Clustering)**
- Distance metric: **Cosine Distance**
- Parameters: `eps=0.3`, `min_samples=5`
- Evaluation: Clustering attempted but **no valid clusters formed**
- Notes: High-dimensional data + parameter sensitivity affected performance.

---

### 4. **Agglomerative (Hierarchical) Clustering**
- Linkage: `Ward`
- Distance metric: `Euclidean`
- Evaluation: **Silhouette Score = 0.39**
- Visualization: 2D cluster scatter plot and dendrogram

---

## Evaluation Metric

- **Silhouette Score** was used to assess the quality of each clustering algorithm, with higher scores indicating better-defined clusters.

---

##  Tools & Libraries

- Python 3.x
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `sklearn` (KMeans, DBSCAN, silhouette_score)
- `pyclustering` (K-Medoids)
- `scipy` (Dendrogram)

---

## Key Insights

- K-Means performed best for this dataset based on silhouette score.
- DBSCAN struggled with the chosen parameters and did not form valid clusters.
- Agglomerative and K-Medoids provided reasonable but less optimal cluster separation.

