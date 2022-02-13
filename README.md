# Amazon_Vine_Analysis by David Aduaka

## Overview of Amazon Vine Analysis

For this Challenge, I was tasked with analyzing Amazon reviews written by members of the Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. From the 50 datasets, I selected the Watch dataset to analyze. Using PySpark and AWS RDS, I performed the ETL process to extract the dataset, transform it, and load it into pgAdmin. Then, using PySpark again to recreate the vine table, filtering it by certain conditions, ultimately to determine if there is any bias toward favorable reviews from Vine members.

## Results 
The vine_df was created, and then filtered for more than 20 total votes, and more than 50% helpful. This became the vine_helpful_df, and all calculations were performed on this dataframe. The Vine and Non-Vine dataframes were created by filtering the vine column for Y and N respectively.

### Vine 
![image](https://user-images.githubusercontent.com/70069730/153780848-61be13cd-44bf-4fa5-a9d9-589d383d7e27.png)

### Non-Vine
![image](https://user-images.githubusercontent.com/70069730/153780883-4b6e45d0-6146-47bb-ab03-65b8afe93aef.png)

### How many Vine reviews and non-Vine reviews were there?
![image](https://user-images.githubusercontent.com/70069730/153780914-d73d0af2-1401-48af-a217-7f09ef80eb0d.png)

For the Watch dataset, there were 47 Vine reviews and 8,362 Non-Vine reviews.
