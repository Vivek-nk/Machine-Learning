# Robust Path Based Spectral Clustering 

## Implementation of Unsupervised Algorithm 

## Implementation of K-Means Clustering Algorithm and Hierarchical Clustering Algorithm

The spiral dataset represents three intertwined spirals, each with approximately 100 two dimensional data points.

The spiral dataset is available in the spiral-dataset.csv file. The file contains three columns, corresponding to the X and Y coordinates in the Cartesian plane, as well as the cluster
number in the third column of the csv file are to denote only the membership of each data point to one of the three clusters. Please note that the cluster numbers are irrelevant in
clustering as it is an unsupervised learning algorithm.

- First lets Generate a figure from the given dataset.

- Now lets implement the k-means clustering algorithm.

- Run your k-means algorithm on the given dataset setting the value k=3 because there are 3 clusters. Initially the 3 centroids are randomly initialized.

- Once the  k-means algorithm has converged, stop the clustering and from your clustering result compute the intrinsic performance metric: Sum of Squared Error, SSE (smaller the better)

- Implement the Hierarchical clustering algorithm.

- Using the “single linkage” method, the hierarchical clustering algorithm is ran on the dataset, and the 3-cluster is obtained (by cutting the dendrogram at a certain height)

- Using the “complete linkage” method, the hierarchical clustering algorithm is ran on the dataset, and the 3-cluster is obtained (by cutting the dendrogram at a certain height)

- Using the “average linkage” method, the hierarchical clustering algorithm is ran on the dataset, and the 3-cluster is obtained (by cutting the dendrogram at a certain height)

- Using the “centroid linkage” method, the hierarchical clustering algorithm is ran on the dataset, and the 3-cluster is obtained (by cutting the dendrogram at a certain height)


Intrinsic Measure of Evaluation
• Sum of Squared Error, SSE
- It is actually the sum of the squared distances between the given data samples with their corresponding centroids.


- Project is implemented on Python, and requires Jupyter Notebook (Anaconda) to run.. 

- K- Means Clustering and Hierarchical Clustering is implemented for performing the clustering of the given spiral data set.

- Both algorithms are written from scratch.




