# K-means clustering
Idea: 
Place K centroids at random locations and repeat:
- for each point find the nearest centroid (e.g. Euclidean distance) and assign it to a cluster associated with the centroid
- for each cluster, calculate the **mean**, which becomes the new centroid
- stop when none of the cluster assignments change