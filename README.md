# Grocery Store Customer Segmentation
This project is about clustering customers based on their previous shopping behavior. I want to use various clustering methods available in scikit-learn.

The results can be found in this presentation: [link](https://github.com/arashag/Grocery-Store-Customer-Segmentation/blob/master/grocery_store_customer_segmentation_presentation.pdf)

## Prerequisites
All the required packages along with their version are in the `requirements.txt`. They can be easily installed with following command:
```
pip3 install -r requirements.txt
```
## Dataset description
This dataset consists of the transactions data for a franchised grocery store. Initially it has 2.5 million rows and contains the two years sales data. We had to change the level of the dataset by aggregating the transactions for each of the customers because the goal of this project is to cluster the customers. The total number of customers is 5000. After some groupings and aggregations (details in the notebook) we reach to our final dataset required for clustering.

## Clustering results
Two methods have been examined to find the best algorithm that clusters the customers. The judging metric was mostly silhouette score. It turned out that the hierarchical clustering with cosine distance metric and average affinity gave me the best results. The dendrogram relating to this solution is as below:

![dendogram](https://github.com/arashag/Grocery-Store-Customer-Segmentation/raw/master/images/dendogram.png)

Furthermore, the most of the column values change substantially among the two clusters. Two distinct group within the customers have been identified.
  * The products and basket size in the first group are very diverse while are very limited for the second group
  * The time and branch of purchase change very much in the first group while the second group usually purchase things at specific times and locations
