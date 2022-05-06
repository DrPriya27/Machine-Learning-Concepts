**Case 1: When ground truth grouping is unknown**
________________________________________________


1) **Silhouette score**-  The Silhouette Coefficient is defined for each sample and is composed of two scores:\
   a: The mean distance between a sample and all other points in the same cluster\
   b: The mean distance beteween a sample and all other points in the next nearest cluster\

   The Silhouette Coefficient s for a single sample is then given as:
   
   ![image](https://user-images.githubusercontent.com/54790008/166201819-faa9ff3f-8741-4e24-a412-02bdbf3947ce.png)


   The Silhouette Coefficient for a set of samples is given as the mean of the Silhouette Coefficient for each sample. It ranges from [-1,1]. The higher the Silhouette    Coefficients (the closer to +1), the more is the separation between clusters. If the value is 0 it indicates that the sample is on or very close to decision   boundary between two neighboring clusters whereas a negative value indicates that thos samples might have been assigned to the wrong cluster.\
Python command 'sklearn.metrics import silhouette_score'
    
2) **Calinski Harabaz index**- also known as the Variance Ratio Criterion and is based on the principle of variance ratio. The index is the ratio of the sum of between-clusters dispersion and of within-cluster dispersion for all clusters (where dispersion is defined as the sum of distances squared). The higher the index the better is clustering. 

Python command 'sklearn.metrics import calinski_harabasz_score'

3) **Davies-Bouldin Index**- This index signifies the average ‘similarity’ between clusters, where the similarity is a measure that compares the distance between clusters with the size of the clusters themselves. a lower Davies-Bouldin index relates to a model with better separation between the clusters. Zero is the lowest possible score. Values closer to zero indicate a better partition

    The Davies–Bouldin index can be calculated by the following formula:

![image](https://user-images.githubusercontent.com/54790008/166203196-0e2fd897-9dc1-4ad5-b0ea-fe2198295876.png)

    where n is the number of clusters, c i {\displaystyle c_{i}} c_{i} is the centroid of cluster i {\displaystyle i} i, σ i {\displaystyle \sigma _{i}} \sigma _{i} is the average distance of all elements in cluster i {\displaystyle i} i to centroid c i {\displaystyle c_{i}} c_{i}, and d ( c i , c j ) {\displaystyle d(c_{i},c_{j})} d(c_{i},c_{j}) is the distance between centroids c i {\displaystyle c_{i}} c_{i} and c j {\displaystyle c_{j}} c_{j}. Since algorithms that produce clusters with low intra-cluster distances (high intra-cluster similarity) and high inter-cluster distances (low inter-cluster similarity) will have a low Davies–Bouldin index, the clustering algorithm that produces a collection of clusters with the smallest Davies–Bouldin index is considered the best algorithm based on this criterion.
    Python command 'sklearn.metrics import davies_bouldin_score'
    
4) **Dunn index**:- The Dunn index aims to identify dense and well-separated clusters. It is defined as the ratio between the minimal inter-cluster distance to maximal intra-cluster distance. For each cluster partition, the Dunn index can be calculated by the following formula
 ![image](https://user-images.githubusercontent.com/54790008/166203111-b1296632-6279-4334-8903-e1c50b56d605.png)
 
 where d(i,j) represents the distance between clusters i and j, and d '(k) measures the intra-cluster distance of cluster k. The inter-cluster distance d(i,j) between two clusters may be any number of distance measures, such as the distance between the centroids of the clusters. Similarly, the intra-cluster distance d '(k) may be measured in a variety ways, such as the maximal distance between any pair of elements in cluster k. Since internal criterion seek clusters with high intra-cluster similarity and low inter-cluster similarity, algorithms that produce clusters with high Dunn index are more desirable.


Case 2: When ground truth grouping is known

1) Homogeneity
2) Completeness
3) Adjusted Rand Index
4) Adjusted Mutual Information
5) V-Measure
