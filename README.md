# Amazon_Vine_Analysis by David Aduaka

## Overview of Amazon Vine Analysis

For this Challenge, I was tasked with analyzing Amazon reviews written by members of the Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. From the 50 datasets, I selected the Watch dataset to analyze. Using PySpark and AWS RDS, I performed the ETL process to extract the dataset, transform it, and load it into pgAdmin. Then, using PySpark again to recreate the vine table, filtering it by certain conditions, ultimately to determine if there is any bias toward favorable reviews from Vine members.

## Results 
The vine_df was created, and then filtered for more than 20 total votes, and more than 50% helpful. This became the vine_helpful_df, and all calculations were performed on this dataframe. The Vine and Non-Vine dataframes were created by filtering the vine column for Y and N respectively.

### Vine 
