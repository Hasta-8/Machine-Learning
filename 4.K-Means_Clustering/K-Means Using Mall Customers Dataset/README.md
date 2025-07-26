Introduction
This notebook explores different clustering techniques using the Mall Customers Dataset to identify distinct customer segments.

Dataset: The analysis utilizes the Mall Customers Dataset, containing information about customers including their CustomerID, Gender, Age, Annual Income (k$), and Spending Score (1-100).

Data Preprocessing:

The Gender column was one-hot encoded to convert it into a numerical format suitable for clustering algorithms.
The CustomerID column was dropped as it is not relevant for clustering.
Clustering Techniques Used and Process:

K-Means Clustering:

The elbow method was employed by calculating the Within-Cluster Sum of Squares (WCSS) for different numbers of clusters (1 to 10). The elbow plot suggested an optimal k of 5.
The silhouette score was also calculated for different numbers of clusters (2 to 10) to evaluate the quality of the clustering. While the silhouette score suggested k=7, the difference from k=5 was not significant, reinforcing the choice of k=5 based on the elbow method and visual inspection.
The K-Means model was built with 5 clusters, and the cluster centers were examined.
A scatter plot of 'Annual_Income_(k$)' versus 'Spending_Score' was generated, colored by the assigned clusters, to visualize the resulting segments.
Hierarchical Clustering:

The Euclidean distance between data points was calculated.
A dendrogram was generated using the Ward linkage method to visualize the hierarchical clustering process and help determine the number of clusters.
An Agglomerative Clustering model was fitted with 4 clusters (chosen based on visual inspection of the dendrogram and comparison with K-Means results).
A scatter plot of 'Annual_Income_(k$)' versus 'Spending_Score' was generated, colored by the assigned hierarchical clusters.
Density-Based Spatial Clustering of Applications with Noise (DBSCAN):

The Nearest Neighbors algorithm was used to calculate the distances to the nearest neighbor for each data point.
A k-distance plot was generated to help determine the optimal epsilon parameter, identifying a point where the distance plot shows a significant bend (around 13-15).
The min_samples parameter was chosen as twice the number of dimensions (2 * 4 = 8).
The DBSCAN model was fitted with epsilon=15 and min_samples=8.
A scatter plot of 'Annual_Income_(k$)' versus 'Spending_Score' was generated, colored by the assigned DBSCAN clusters, including noise points.
Challenges Faced:

Determining the optimal number of clusters can be subjective and requires considering multiple evaluation metrics (Elbow method, Silhouette score) and visual inspection, as seen with the slight discrepancy between the elbow method and silhouette score for K-Means.
Visualizing clusters in datasets with more than two features is challenging when relying solely on 2D scatter plots. Principal Component Analysis (PCA) or other dimensionality reduction techniques could be used for better visualization in higher dimensions.
Learnings and Conclusion:

This notebook demonstrates the application of three different clustering algorithms (K-Means, Hierarchical, and DBSCAN) for customer segmentation.
Each algorithm has its strengths and weaknesses and can produce different clustering results.
The choice of parameters (e.g., k for K-Means, linkage and number of clusters for Hierarchical, epsilon and min_samples for DBSCAN) is crucial and impacts the clustering outcome.
Visualizations are essential for understanding the characteristics of the clusters, although their interpretability decreases with increasing data dimensionality.
Based on the analysis, the mall customers can be effectively segmented into distinct groups based on their income and spending habits. This segmentation can provide valuable insights for developing targeted marketing strategies, personalized promotions, and optimizing store layouts to cater to the specific needs and preferences of each customer segment.
