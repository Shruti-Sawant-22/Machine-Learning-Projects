# ML--Customer-Segmentation

## Objective : To increase marketing efficiency by exploring the Retail Store Data and coming up with insights to build a data driven business strategies

## Project Summary

### 1 - Data Exploration
### 2 - Data Analysis
### 3 - Building Features
### 4 - Visualizing the data
### 5 - Building the RFM Metrics to visualize to categorise the customer
### 6 - Preprocessing the Data for Machine Learning
### 7 - Building the Machine Learning Model to obtain the clusters
### 8 - Profiling the clusters

## Business Impact

### 1. Helping Business Development Team to create product differentiation based on the characteristic for each customer.
### 2. Know how to treat customer with specific criteria.
### 3. Recommendation based on customer segmentation.

## Data Exploration

### 25% of the rows do not have Customer ID
### 90% of the data is from United Kingdom
### We have total around 1 years of data

## Data Analysis

### Total return orders = 5172
### Total return orders where CustomerID is null= 1518

!["Month wise Revenue"](https://github.com/Shruti-Sawant-22/Machine-Learning-Projects/blob/main/Customer%20Segmentation/Month%20wise%20Revenue.png)

### Sales in the 1st half of the year was not so great

!["Month wise Order"](https://github.com/Shruti-Sawant-22/Machine-Learning-Projects/blob/main/Customer%20Segmentation/Month%20wise%20orders.png)
## Highest number of orders are placed in November and th lowest being December (Maybe business was not expecting such a drastic sales and ran out of stock the following month)

### Do a value counts on country you will see that 90% data is from UK

### 1.Restrict the data where country = United Kingdom.
### 2.Restrict the data further where Quantity > 0
### 3.Convert the date into DateTime object. Print the max and min date.
### 4.Drop record where CustomerID is null
### 5.Drop record where Unitprice is less than 0
### 6.Create a revenue field (Revenue = Quantity * Unit Price)
### 7.Aggregating the Orders by Month
### 8.Create Month wise Quatity plot (line plot)
### 9.Create Month wise Revenue plot (line plot)
### 10.Study about RFM Metric(Recency Frequent, Monetary) used in Businesses

# Using RFM Metric(Recency Frequent, Monetary)

## Understanding Recency, Frequency, Monetary Value
### The RFM model is based on three quantitative factors:
### 1. Recency: How recently a customer has made a purchase
### 2. Frequency: How often a customer makes a purchase
### 3. Monetary Value: How much money a customer spends on purchases


### Modeling Data : RFM Quantiles
### Now we split the metric into segments using Quantiles.We will asign scores from 1-4 to each recency frequency and monetary respectively.
### 1 is the highest value and 4 is the lowest value.
### Our final RFM score is calculated simply by combining indivisual RFM scores

## Model Building (K-Means Clustering model) findling the best value for k using "Elbow-Method"

!["Elbow Plot"](https://github.com/Shruti-Sawant-22/Machine-Learning-Projects/blob/main/Customer%20Segmentation/Elbow_plot.png)
## Final Interpretation / Cluster Interpretation

### Cluster 0 : Represents the best customers who visit the store frequently and are big spenders

### Cluster 1 : Represents customers who were good customers and used to visit the store frequently but have not visited recently
   
### Cluster 2 : Represents lost customers who visited the store long back and only a selective times
   
### Cluster 3 : Represents new customers who recently started visiting our store.
   
## Business Action

### 1. Take feedback from customers from cluster 1 understand why they stopped visiting as they account for nearly 25% of the entire customer base

### 2. Study the purchase pattern from customers falling in cluster 0 and try to implement the same startegy to cluster 3 for customer retention
