# Unsupervised_Customer_segmentation
This project is the part of Almabetter job guarantee program.

#           *Project Title : Extraction/identification of major topics & themes discussed in news articles*
#          **Problem Description**
In this project, your task is to identify major customer segments on a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.
# **Data Description**

# **Attribute Information:**
* ### InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.
* ### StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
* ### Description: Product (item) name. Nominal.
* ### Quantity: The quantities of each product (item) per transaction. Numeric.
* ### InvoiceDate: Invice Date and time. Numeric, the day and time when each transaction was generated.
* ### UnitPrice: Unit price. Numeric, Product price per unit in sterling.
* ### CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
* ### Country: Country name. Nominal, the name of the country where each customer resides.


# **Summary** 
I started with the loading, understanding, and exploring the dataset to see the major trends and insights from data regarding the purchases. I have made a few observations while performing the project on the given dataset. Which are below:
There were (541909, 8) rows and columns out of which I  saw that there were null values in the description and CustomerID columns, which were of float and object data types. I have removed the null values as imputing them with mode would not be meaningful.
After removal of the null values I had (406829, 8) observation and variables respectively.
I did see the overall data distribution and found few points as below:
●    In quantity we have values in negative and as well as in Unit Price.
●    Found positively skewed distribution of the dataset.
●    Once I started exploring further country wise, monthly basis, day basis and hourly basis and as per time zone my findings were below:
●    Countries with top customers are: United Kingdom, Germany, France, EIRE and Spain.
●    Most customers have purchased in the months of November, October, December and September.
●    Most of the customers have purchased the items on Thursday, Wednesday and Tuesday.
●    I have seen that afternoon timings are popular for purchasing items.
●    Especially 11-12-13-14-15 gave more numbers of customer purchasing.
●    Once I have seen the data and for its major minor trends, I then started with modeling techniques which are below:
●    Used RFM model to find out the valuable customers based on Recency, Frequency and Monetary values.
●	While using this model I have seen a few points that there were customers which were having more Recency and more Monetary, more Recency and less monetary.
●	Similarly, for these combinations I have checked for each customer and found the best set of customers after setting the threshold to 5 and 8 respectively given 1263 customers and 2587 customers with threshold of setting to 8.
●	I then started with K-mean clustering to cluster the same set of customers and tried with 2 features and 3 features which were (RFM) Recency, Frequency and Monetary.
●	I checked the cluster formation with the help of Silhouette score and elbow method and DBSCAN.
●	I found DBSCAN performing good to find out the optimal clusters whereas K-mean clustering is not proven that well with elbow method and silhouette scores. After using all methods I have seen that most of the time optimal numbers of clusters were 2.


