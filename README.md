# Hierarchical clustering 

### Note: Not suitable for larger Dataset - BIRCH(Balanced Iterative Reducing and Clustering Usign Hierarchies) algorithm.

Before kick start with Hierarchical clustering, We should review Similarity and distance calculation (Manhattan/Euclidean/Minkowsk/Jaccard similarityCosine Similarity) & Proximity Matrix.

Point to remember:
  1.Minimum distance
  2.Higher similarity
  
Scipy Implementation of distance:   https://github.com/scipy/scipy/blob/v0.14.1/scipy/spatial/distance.py#L199

Hierarchical clustering begins by treating every data points as a separate cluster. Further below steps followed
  1. Identify the 2 clusters which can be closest together, and
  2. Merge the 2 maximum comparable clusters. We need to continue these steps until all the clusters are merged together.
  
In Hierarchical Clustering, the aim is to produce a hierarchical series of nested clusters. Dendrogram is used for explain Hierarchical clustering, factors are merged (bottom-up view) or cluster are break up (top-down view).
  1. Agglomerative (Bottom-Up) : We have to consider every data point as an individual Cluster and at every step, merge the nearest pairs of the cluster. 
  2. Divisive (Top-Down) : We have to consider all data points as a single cluster and in every iteration.

## Agglomerative

## Divisive

## Sinigle and Complete Linkage



* Hierarchical : MIN
* Hierarchical : MAX
* Hierarchical : Group Average

## Hierarchical : MIN
  ## Advantage 
    * Need not to be Elliptical
  ## Limitation
    * Original Point
    * Sensitive to outlier.
    * Computationaly expensive - Time complexity is high.


## Hierarchical : MAX
  ## Advantage 

  ## Limitation
    * Sensitive to outlier.
    * Spherical cluster are generated - Tends to break larger cluster into smaller cluster.

## Hierarchical : Group Average
  ## Advantage 
    * Better than MIN & MAX - Outlier will be less
  ## Limitation
    * Sensitive to outlier.
    * Spherical cluster are generated - Tends to break larger cluster into smaller cluster.


MST: Divisive Hierarchical Clustering
Build MST(Minimum spanning Tree)
 1. Start with a tree that consists of an point.
 2. In successive steps, look for the closest pair of points(p,q) such that one point(p) is in the current tree but the other (q) is not
 3. As q to the tree and put an edge between p and q

