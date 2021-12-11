**DBSCAN and Clustering Examples**

Exploring and understanding Density-based spatial clustering of applications with noise (DBSCAN) and comparing it with Kmeans clustering.

## DBSCAN

Density-based spatial clustering of applications with noise (DBSCAN) is a well-known data clustering algorithm that is commonly used in data mining and machine learning.
Based on a set of points (let’s think in a bidimensional space as exemplified in the figure), DBSCAN groups together points that are close to each other based on a distance measurement (usually Euclidean distance) and a minimum number of points. It also marks as outliers the points that are in low-density regions.

Parameters:
The DBSCAN algorithm basically requires 2 parameters:
*eps: specifies how close points should be to each other to be considered a part of a cluster. It means that if the distance between two points is lower or equal to this value (eps), these points are considered neighbors.*

*minPoints: the minimum number of points to form a dense region. For example, if we set the minPoints parameter as 5, then we need at least 5 points to form a dense region.*

## Why should we use DBSCAN?

The DBSCAN algorithm should be used to find associations and structures in data that are hard to find manually but that can be relevant and useful to find patterns and predict trends.

Clustering methods are usually used in biology, medicine, social sciences, archaeology, marketing, characters recognition, management systems and so on.
Let’s think in a practical use of DBSCAN. Suppose we have an e-commerce and we want to improve our sales by recommending relevant products to our customers. We don’t know exactly what our customers are looking for but based on a data set we can predict and recommend a relevant product to a specific customer. We can apply the DBSCAN to our data set (based on the e-commerce database) and find clusters based on the products that the users have bought. Using this clusters we can find similarities between customers, for example, the customer A have bought 1 pen, 1 book and 1 scissors and the customer B have bought 1 book and 1 scissors, then we can recommend 1 pen to the customer B. This is just a little example of use of DBSCAN, but it can be used in a lot of applications in several are

![16](https://user-images.githubusercontent.com/86251750/145678517-580dfac4-d838-4d65-8680-a01fbd0b7962.PNG)

    from sklearn.cluster import DBSCAN

## KMeans Clustering

K-Means Clustering, also known as Lloyd’s Algorithm, is an iterative, data-partitioning, Unsupervised Learning Algorithm used to assign n observations to exactly one of K clusters defined by their centroids, where K is chosen before the algorithm starts.

**Clustering**

The most basic definition of clustering is the technique of grouping data points together. It is an assumption that data points of the same group posses similar properties or features, whereas data points from different groups will have high dissimilarity.
Clustering is an Unsupervised Learning Method and is commonly used for statistical data analysis in many fields. With clustering, we only try to investigate the structure of the data by grouping them.

**steps for Kmeans**

•Step 1: Choose the number of clusters k. ...

•Step 2: Select k random points from the data as centroids. ...

•Step 3: Assign all the points to the closest cluster centroid. ...

•Step 4: Recompute the centroids of newly formed clusters. ...

•Step 5: Repeat steps 3 and 4.

**Stopping Criteria for K-Means Clustering**

There are essentially three stopping criteria that can be adopted to stop the K-means algorithm:

•Centroids of newly formed clusters do not change

•Points remain in the same cluster

•Maximum number of iterations are reached

We can stop the algorithm if the centroids of newly formed clusters are not changing. Even after multiple iterations, if we are getting the same centroids for all the clusters, we can say that the algorithm is not learning any new pattern and it is a sign to stop the training.

Another clear sign that we should stop the training process if the points remain in the same cluster even after training the algorithm for multiple iterations.

Finally, we can stop the training if the maximum number of iterations is reached. Suppose if we have set the number of iterations as 100. The process will repeat for 100 iterations before stopping.

![17](https://user-images.githubusercontent.com/86251750/145678993-10d17e0e-df87-401a-abb7-f3ddebf57660.PNG)

    from sklearn.cluster import KMeans
    
    
