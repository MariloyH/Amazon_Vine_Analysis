# Amazon_Vine_Analysis
Cloud_ETL_Analysis

##Overview
The requiremennt for this project was analyze Amazon reviews written by members of the paid Amazon Vine program which is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. 
First, I selected Pet Supplies dataset from 50 datasets available and used PySpartk to extract the data and transform it DataFrames. Then Iconnected to AWS RDS instance to load the transformed data into SQL tables using PgAdmin.  For the second Deliverable,  I used PySpark through Google Colab to determine if there is any bias toward favorable reviews from Vine members in the PetSupplies  dataset. 


## Results 
### Deliverable 2
From the Amazon Reviews Pet Supplies dataset, I extracted the data and transformed to 4 dataframes for storage as tables in PgAdmin: customer_table, product_table, review_id_table and vine_table. Subsequently, these  Databases were storage in Amazon Cloud Service.

###*Customers Table*
<img width="332" alt="customers_table" src="https://user-images.githubusercontent.com/102195803/180673324-6e295f52-3a30-4260-86f4-5c62efe35e2c.png">

*Products Table*
<img width="749" alt="products_table" src="https://user-images.githubusercontent.com/102195803/180673317-3c7c7556-3590-4570-b8e7-6f8e5d1e0d37.png">

*Review Id Table*
<img width="682" alt="review_id_table" src="https://user-images.githubusercontent.com/102195803/180673312-8b8cd03f-13d9-4c9c-aa84-2a9c5747f0be.png">

*Vine Table*
<img width="587" alt="vine_table" src="https://user-images.githubusercontent.com/102195803/180673329-404df172-ac91-430f-9c0a-86e0ac926919.png">

### Deliverable 2

Subsequently, I repeated the extraction process to perform the Vine Analysis, filtering the total votes equal or greater than 20 and the percent of Helpful Votes to equal or greater than 50%, and then we reduce the dataset from *2,643,619*  reviews to *38,010*

*How many Vine reviews and non-Vine reviews were there?* 

 Vine members made  % (170) of the reviews whereas the remaining 99.1% were Non-Vine members (37,840).
 
 
*How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?*



*What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?*

*1. How many Vine and non-Vine reviews

The Pet Supplies had *39,376* Vine and non-Vine reviews in total. 
From this, 20,797 were Vine and  5 stars. 
How many Vine reviews and non-Vine reviews were there?
How many Vine reviews were 5 stars? *65*  How many non-Vine reviews were 5 stars? *20612*
What percentage of Vine reviews were 5 stars? *0.3%* What percentage of non-Vine reviews were 5 stars? *99.1%*

## Summary
From this results, I don´t see any positive bias for reviews from the Vine program. 99 % of the positive opinions came from non-Vine reviews. 

