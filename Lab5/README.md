# Clustering Analysis on Wine Dataset

## Purpose
The purpose of this lab was to apply and compare clustering techniques—specifically Hierarchical Clustering and DBSCAN—on the Wine dataset from `sklearn.datasets`. This hands-on exploration aimed to build an intuitive and analytical understanding of how unsupervised learning algorithms can group data without labels. By experimenting with parameters, visualizing cluster formations, and evaluating results with internal and external metrics, the lab highlights each algorithm’s strengths, limitations, and ideal use cases.

## Key Insights
- **Data Standardization:** Standardizing features was essential prior to clustering, ensuring fair distance calculations among variables with different scales.

- **Hierarchical Clustering:**
  - Successfully grouped wine samples into distinguishable clusters based on chemical properties.
  - The dendrogram revealed the nested structure of clusters, which is helpful in deciding the optimal number of clusters.
  - Agglomerative clustering worked best when the number of clusters was known or could be inferred visually.

- **DBSCAN Clustering:**
  - Showed the ability to detect noise and clusters of arbitrary shapes without specifying the number of clusters.
  - Very sensitive to the `eps` and `min_samples` parameters. Slight changes drastically affected results.
  - Performed well when clusters had varying densities but struggled in uniformly distributed high-dimensional data like Wine.

- **Evaluation Metrics:**
  - **Silhouette Score** provided insight into how well points fit within their assigned clusters.
  - **Homogeneity Score** and **Completeness Score** (when comparing with true labels) helped evaluate the quality of label-to-cluster mapping.
  - DBSCAN showed lower silhouette scores due to many noise points, while Hierarchical clustering scored higher with optimal `n_clusters`.

## Challenges and Decisions
- **Choosing Optimal Parameters:**
  - For Hierarchical Clustering, selecting `n_clusters` required visual inspection of the dendrogram.
  - For DBSCAN, tuning `eps` and `min_samples` was non-trivial and required iterative testing to balance cluster tightness and noise detection.

- **Noise Handling in DBSCAN:**
  - Identifying an appropriate `eps` value was challenging due to DBSCAN’s sensitivity. Too small led to excessive noise; too large merged distinct clusters.

- **Cluster Evaluation Without Labels:**
  - Internal metrics like the silhouette score were helpful, but external metrics (homogeneity/completeness) relied on the presence of ground truth, which real-world clustering often lacks.

- **Visualization:**
  - Using only two principal components for visualization simplified interpretation but may have hidden clustering structures in higher dimensions.
