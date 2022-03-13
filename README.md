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




# **Model used___**

* **RFM model(Heuristic approach)**
* **K-Mean-clustering.**
*  **Hierarchical clustering.**
*  **DBSCAN.**


# **Methods used for Optimal K-Value__**

* **Elbow method.**
* **Silhouette scores.**
*  **Dendrogram.**




# **Exploratory data Analysis Findings___**


**Findings**
* Mean is far from the median shows that we dont have normal distribution of data.
* Since we have other columns in object datatype hence we don't have statistical description for those other columns.
* In quantity we have values in negative and as well as in UnitPrice.


* Positively skewed (or right-skewed) distribution is a type of distribution in which most values are clustered around the left tail of the distribution while the right tail of the distribution is longer.hear mean>median>mode

* Negatively skewed (also known as left-skewed) distribution is a type of distribution in which more values are concentrated on the right side (tail) of the distribution graph while the left tail of the distribution graph is longer.hear mean<median<mode

* For normal distribution graph mean=median=mode.





**Findings**
*  **most of the customers are from United Kingdom ,Germany ,France ,EIRE and Spain.**


## Findings__
* Did groupby Country and aggregated by Customer ID to see the how many unique Customers we have from 28 countries.
 
**Least Country ID's**
*    Israel	4
*	Greece	4
*	EIRE	3
*	Malta	2
*	United Arab Emirates	2
*	Bahrain	2
*	Lithuania	1
*	Czech Republic	1
*	Lebanon	1
*	RSA	1
*	Saudi Arabia	1
*	Singapore	1
*	Iceland	1
*	Brazil	1
*	European Community	1
*	Hong Kong	0


**Maximum uniques ID's**

United Kingdom	3950
* 	Germany	95
* 	France	87
*	Spain	31
*	Belgium	25
*	Switzerland	21


**More than 80% of the customers in the data are from the United Kingdom. There’s some research indicating that customer clusters vary by geography.**

## Findings__

**Till Here I have explored that I have 541909 observations and 8 columns.**
* I have columns with object types int, float, object and datetime64[ns].

*I have explored the null values using different different approaches to ensure the clarity of information*

**I have explored that I am having amount of null value in 2 columns:**
* Description     0.268311 (0.26%).
* CustomerID     24.926694(24%).
      
**Columns with highest unique values are** 
* InvoiceDate    23260*
* InvoiceNo      25900*

**Columns with lowest Unique values are**
* Country           38
* Quantity         722
* UnitPrice       1630

**Country column with unique countries are:**
* 38



## Findings__
* We had negative values in Quantity columns which were removed.
* I also provided next date based on timing for Invoice date.




## Findings__
**for Discription column**
* I started with renaming the descrption column.
* counted the values present in the column.
* checked lowest values =1
* checked highest values = 2028

**Top product  based on maximum selling  are :**
*    1.WHITE HANGING HEART T-LIGHT HOLDER,
*    2.REGENCY CAKESTAND 3 TIER
*    3.JUMBO BAG RED RETROSPOT
*    4.PARTY BUNTING
*    5.LUNCH BAG RED RETROSPOT


**Bottom 5 Product based on the selling are:**
    
*   1.light deorated battry operated	
*    2.Water damaged.
*   3.throw away.	
*   4.re dotcom quick fix.	
*   5.Birthday Banner Tape.


## Findings__
* **Most numbers of customers have purchased in the months of November ,October, December and September.**
* **Months of April ,January and February, we have less number of customer buying.**


## Findings__
* **We can also say that afternoon timings are popular for the purchasing items.**
* **Especially 11-12-13-14-15 gave the more numbers of customer purchasing.**
* **So as it matters alot that what is time of the day we would need to convert data into time zones.**


## Findings__
* **from the discriptive statistics of the recency we can conclude that we have on an average of 50 days of gap for the purchase**


* **2nd observation that it is confering is that we have mean around 92 days but we do have the median 50 days, so that means bascally we do have skewed distribution of data in the recency column.**
* **Distribution in Recency is right skewed.**





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


