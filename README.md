# Amazon_Vine_Analysis

## Overview 

"Amazon Vine is a customer review program that enables Amazon selling partners to put their products in the hands of Amazon reviewers that Amazon invited to participate in Vine. These reviewers, also known as Vine Voices, were selected for their ability to post insightful reviews on their Amazon purchases."(Amazon Seller Center)

In this project, we used PySpark and Jupyter Notebook to perform the ETL process to extract one of the Amazon review datasets, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. After we successfully transferred the data, we used PySpark and Pandas to determine if there was any bias toward favorable reviews from Vine members in my dataset. 


### The Data Resources
https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt

### The Dataset Chosen for This Project: Reviews on US Lawn and Garden
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Lawn_and_Garden_v1_00.tsv.gz


## Determine Bias of Vine Reviews

![deterimin bias](Image/vine_paid_vs_unpaid.png)

- How many Vine reviews and non-Vine reviews were there?
    - From the screenshot above, we can see that there were 373 vine reviews and 45692 non-vine reviews in this dataset.
- How many Vine reviews were five stars? How many non-Vine reviews were five stars?
    - There were 171 5-star vine reviews and 22536 non-paid/non-vine reviews.
- What percentage of Vine reviews were five stars? What percentage of non-Vine reviews were five stars?
    - 45.8% of vine reviews were five starts, versus 49.3% of non-vine 5-star reviews.

## Summary: 

From the 5-star review rate, we can see no positivity bias for reviews in the Vine program. On the contrary, the vine program had 7.6% fewer 5-star reviews than non-vine ones. Based on this result, we can assume that vine viewers were more strict in product rating than non-vine reviewers. To prove this differently, we can check the 1-star review rate between the paid and unpaid reviews to see if the difference is similar.


