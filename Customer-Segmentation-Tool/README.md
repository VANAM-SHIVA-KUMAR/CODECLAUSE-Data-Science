# Customer-Segmentation


## Business Value

Customer segmentation is the process of grouping customers together based on some common characteristics, based on their interactions with the business. In most cases this interaction is in terms of their purchase behavior and patterns. These groups are beneficial for marketing campaigns, in identifying potential profitable customers and in developing customer loyalty.

## Problem Statement

To identify clusters of customer based on their purchase behaviour by taking into account the recency, frequency and monetary value of their transactions.

## Data

![](Images/Data%20Sample.PNG)

Each row of data represents a transaction and each column contains a transaction's attributes.

__InvoiceNo__ : A unique identifier for the invoice. An invoice number shared across
rows means that those transactions were performed in a single invoice (multiple
purchases). 

__StockCode__ : Identifier for items contained in an invoice.

__Description__ : Textual description of each of the stock item.

__Quantity__ : The quantity of the item purchased.

__InvoiceDate__ : Date of purchase.

__UnitPrice__ : Value of each item.

__CustomerID__ : Identifier for customer making the purchase.

__Country__ : Country of customer.

## Approach

+ Loading Dependencies

+ Loading Data

+ Data Exploration

+ Data Processing

+ Focussing on One Market (UK in this case)

+ Building Recency Feature
    
+ Calculating Frequency and Monetary Values

+ Customer Segmentation
Kmeans Algorithm
Silhouette Score Metric 

+ Visualize Customer Segments

We use the silhouette score for finding out the optimal number of clusters during our clustering process.

## Data Exploration

__Sales By Counntry__

![](Images/Sales%20by%20Country.PNG)

__Top 15 customers contributing to 10.5% of total sales__

![](Images/Top%2015%20customers.PNG)

__Sales Recency__

![](Images/Sales%20Recency.PNG)

## Processed Data

__Data with Recency, Frequency and Monetary feature__

![](Images/RFM%20Data.PNG)


## Model Building and Clustering

Developed and tested 3,4 and 5 number of clusters for their silhouette score. The results are as follows:

__Clusters 3__

![](Images/clusters%203.PNG)

+ There is a stark difference in Monetary vallue of customer

+ Cluster 2 is the cluster with high value customers who shop frequently and is certainly an important segement for each business.

+ Cluster 0 and 1 has customer groups with low spend and medium spends 

__Clusters 4__

![](Images/Clusters%204.PNG)

+ The high value customers are subdivided into two groups, one with lower spends and lower frequency (represented by cluster 0) and another with high amount and higher frquency but lower recency represented by cluster 1.

__Clusters 5__

![](Images/Clusters%205.PNG)

+ With 5 clusters too we have two subgroup for higher spend customers and 3 subgroup for customers with lower spend but varying frequency and recency.

## __Visualizing Clusters__

Amount vs Frequency

![](Images/Amount%20vs%20Freq.PNG)

Recency vs Amount

![](Images/Recency%20vs%20Amount.PNG)

Recency vs Frequency

![](Images/Recency%20vs%20Freq.PNG)


## __Conclusion__
Going by mathematical metrics we see the silhouette score for 3 clusters is max suggesting that 3 clusters is the optimal number of clusters for this dataset. However we need to include business metrics and domain insights in our modelling process to obtain the best suited data-focussed solution for the bsuiness problem at hand :-)

