# Amazon_Vine_Analysis


# Overview of the Project


Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.


# Analysis of the Project


I extracted the dataset from AWS S3 related to products under baby category


![Spark Data Frame](https://user-images.githubusercontent.com/101373142/177060448-02a7c421-e9b4-4293-8917-85da910daf99.png)


I separated the datasets into 4 tables: customers, products, reviews and vine. I connected to an AWS RDS instance and loaded the transformed data into pgAdmin


![Connect to AWS RDS](https://user-images.githubusercontent.com/101373142/177060469-e0a1ef58-4ef4-4370-bc9e-b70e05b74756.png)


I then used Pandas to complete additional analysis.  I created a vine table with the following columns: review id, start rating, votes for the review and its helpfulness, vine/non-vine participant. Analysis was based on reviews that have 20 votes of more and at least half of them are marked as helpful


# Results


I filtered data to meet analysis requirements and created summary data frame:


![Vine 5 star reviews](https://user-images.githubusercontent.com/101373142/177060508-423b71bb-c6c8-47a5-a92e-73a492eef94e.png)


There are only 222 reviews within Vine program and 6704 reviews from non-Vine customers

111 Vine program reviews have five stars rating. It is equal to 50% of all reviews written by Vine program participants

There are also 3,339 five star ratings; approximately 49.81% of all non-Vine reviews


# Summary


Based on the results in the summary table, it appears there isn’t any positivity bias for reviews in the Vine program. Results show that non-vine customers tend to leave many more reviews with higher ratings



![Vine Star Ratings](https://user-images.githubusercontent.com/101373142/177060551-eb405d09-18ab-4fa8-bad3-88564ef8473d.png)




