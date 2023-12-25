# Customer-Segmentation-Analysis
In marketing, consumer understanding is key. A dataset with details on 2,240 customers, including age, education, marital status, and purchasing behavior, enables effective segmentation. This informs tailored marketing strategies by creating customer clusters.

# Background
The data-set was retrieved from kaggle.com [1]. The data is given to us as a csv file with
headers, containing 2241 records with 37 attributes. These attributes include:
attributes = ['ID', 'Year_Birth', 'Education', 'Marital_Status', 'Income', 'Kidhome',
'Teenhome', 'Dt_Customer', 'Recency',
'MntWines', 'MntFruits', 'MntMeatProducts',
'MntFishProducts', 'MntSweetProducts', 'MntGoldProds', 'NumDealsPurchases',
'NumWebPurchases', 'NumCatalogPurchases', 'NumStorePurchases', 'NumWebVisitsMonth',
'AcceptedCmp3', 'AcceptedCmp4', 'AcceptedCmp5',
'AcceptedCmp1', 'AcceptedCmp2','Response', 'Cluster']
The following attributes were relevant for customer segmentation and used for k-means clustering:
YearBirth, Education, MaritalStatus, Income, Recency, MntWines, MntFruits, Mnt-
MeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds, NumDealsPurchases,
NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumWebVisitsMonth, AcceptedCmp1,
AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5, Response.

# Problem 
In the realm of marketing, understanding the consumer is paramount. The provided dataset
offers a window into the lives of 2,240 customers, cataloging their age, education, marital
status, and a detailed record of their purchasing behavior. This information, is pivotal
for the segmentation of customers into meaningful groups, enabling the delivery of tailored
marketing strategies. We will use the dataset to create clusters of customers.

# Preprocessing 
During preprocessing, I noticed ’Income’ had 24 missing values in total. I filled in the
missing values using the mean income of the column values

# Approach 
Performed an analysis of different customer segments. I did an age calculation
by subtracting ’YearBirth’ from the current year and then categorize these ages into groups
’Child’,’Young’,’Middle-Age’,’Old’. Followed by this, I simplified the maritial status into
2 groups ’Alone’, ’Couple’. A new column ’Children’ is calculated by adding ’KidHome’
and ’Teenhome’. I was able to create an age group bar chart, where most customers fell
into the ’Old’ and ’Middle-aged’ category, suggesting that products or services may appeal
more to older demographics. I also created an education count bar chart that shoes the
distribution of education levels amoung customers where majority have Graduation level
education, indicating most customers are educated. Furthermore, a scaled purchase
methods violin plot was made to show the distribution made through different channels
(discount, web, catalog store). Store purchases were the most common followed by
web, catalog and discount methods. This can help to focus efforts on in-store marketing
campaigns. Used the Gaussian Mixture to create a the summary

## K-Means
Used the Elbow Method to determine the optimal number of clusters. Then created the
distribution of clusters bar chart. This chart shows the distribution of data points across
the clusters formed by K-means. It can be seen that there is a significant variance in the
size of clusters. One cluster is particularly larger than the rest which could imply there is a
dominant segment within the customer base. 

## Hierarchical Clustering
The dendrogram shows the hierarchical clustering of the data. Each vertical line
represents a cluster, and the height of the horizontal lines joining clusters indicates the
distance between them. The shorter the horizontal line, the more similar the clusters.

# Results
• High potential: This cluster has a relatively high average income but less variation
compared to the ’Ideal’. These customers could represent an opportunity for increased
engagement and sales. 

• Risk: With the lowest average income and a small standard deviation, this cluster
might be considered at risk due to lower financial capacity or engagement. 

• Attention Required: Similar to the ’Risk’, but with slightly higher income levels. These
customers might require targeted marketing to increase their engagement. 

• Ideal: The most affluent customer group with the highest average income and the
greatest variability. This group likely includes top spenders and could be the primary
target for premium offerings. 

• Education: most customers have a ’Graduation’ level of education, suggesting a educated
customer base

• Marital Status: Majority of customers are in a relationship, suggesting customer base
is couples or families

• Age: Age distribution is skewed towards middle-aged and older customers, with few
young customers. Suggesting perhaps the products are more appealing to older people.
• Spending Habits: Customers spent the most on wine. This can be a potential focus
for marketing campaigns.

• Income: Range of income is quite large but most customers have a mid range income.
Helps to inform pricing and sale campaigns
