Contents:-

https://analyticsindiamag.com/a-tutorial-on-various-clustering-evaluation-metrics/

There are some metrics, like Homogeneity, Completeness, Adjusted Rand Index, Adjusted Mutual Information, and V-Measure. To compute these metrics, one needs to know the true labels of data-set, so we may test algorithms with classification data-sets to have true labels and then evaluate results.

https://stats.stackexchange.com/questions/95782/what-are-the-most-common-metrics-for-comparing-two-clustering-algorithms-especi

1) Silhouette score- The Silhouette Coefficient is calculated by using the mean of the distance of the intra-cluster and nearest cluster for all the samples. The Silhouette Coefficient ranges from [-1,1]. The higher the Silhouette Coefficients (the closer to +1), the more is the separation between clusters. If the value is 0 it indicates that the sample is on or very close to the decision boundary between two neighboring clusters whereas a negative value indicates that those samples might have been assigned to the wrong cluster.
2) Calinski Harabaz index
3) Davies-Bouldin Index
