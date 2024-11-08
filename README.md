NAME: GOMATHI MP,
COMPANY :CODTECH IT SOLUTION ,
ID:CT6WDS2027,
DOMAIN:DATA ANALYTICS,
DURIATION:SEPTEMBER TO NOVEMBER 2024,
MENTOR:NEELA SANTHOSH KUMAR

overview of the project: CUSTOMER SEGMENTATION AND ANALYSIS

Objective:
The goal is to segment a retail customer base by grouping customers based on their purchase behavior, preferences, and shopping habits.
This segmentation helps in identifying clusters or groups that exhibit similar behaviors, allowing the company to tailor marketing strategies, offers, and services to each group.

Key Activities
Data Preparation:
The sample data is created and preprocessed. A new column, TotalSpent, is calculated by multiplying Quantity and UnitPrice to get the total spending of each customer.
Aggregating Customer Data:
Data is aggregated by CustomerID to derive summary statistics like the number of purchases (NumPurchases), total quantity of items bought (TotalQuantity), and the total amount spent (TotalSpent).
This aggregation helps capture each customer’s purchasing behavior.

Feature Scaling:
Features are scaled using StandardScaler to ensure that each feature contributes equally to the clustering, as clustering algorithms are sensitive to the scale of input features.
Finding Optimal Number of Clusters (Elbow Method):
The code uses the Elbow Method to determine the optimal number of clusters (k) by plotting the inertia (sum of squared distances from each point to its cluster center).
By examining the elbow plot, k=3 is chosen as the optimal number of clusters.

Clustering with K-Means:
A K-Means model is built with k=3, and customers are segmented into three clusters based on their purchasing behavior.
The clusters are assigned back to the customer data for further analysis.

Cluster Visualization:
A scatter plot is created to visualize customer segments based on their spending (TotalSpent) and frequency of purchases (NumPurchases), with each cluster represented by a different color.
Evaluating Clustering (Silhouette Score):
The Silhouette Score is calculated to measure how well-defined each cluster is. A higher score indicates better-defined clusters.

Cluster Summary:
Finally, a summary of each cluster’s average NumPurchases, TotalQuantity, and TotalSpent is generated to understand the characteristics of each segment.

Technologies Used
Pandas:
Used for data manipulation and aggregation to prepare the dataset for clustering.

Numpy:
Used for numerical operations and data handling.

Matplotlib and Seaborn:
Matplotlib is used for plotting the Elbow Method graph to determine the optimal k.
Seaborn is used to create a scatter plot for visualizing the clusters.

Scikit-Learn:
StandardScaler: Used for feature scaling to standardize features before clustering.
KMeans: Implements the K-Means clustering algorithm, where clusters are identified based on centroids.
silhouette_score: A metric from Scikit-Learn that measures the quality of clustering by comparing intra-cluster and inter-cluster distances.
