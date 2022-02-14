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

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

In each instance, a five_star dataframe had to be created by filtering the star_rating == 5.

![image](https://user-images.githubusercontent.com/70069730/153781094-62e3aac2-3897-430b-ab17-b173ccb02231.png)

There were only 15 five-star Vine reviews, while there were 4,332 five-star Non-Vine reviews.

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

Finally, 2 calculations needed to be performed using variables I already created. The image below depicts this.

![image](https://user-images.githubusercontent.com/70069730/153781185-7b863806-59f3-41d6-8490-bdaadc83d09c.png)

31.9% of Vine reviews were 5 stars. 51.8% of Non-Vine reviews were 5 stars.

## Summary 
- There were a total of 8,409 reviews for watches in this dataset. There were 47 Vine reviews and 8,362 Non-Vine reviews.
- There were only 15 five-star Vine reviews, while there were 4,332 five-star Non-Vine reviews.
- 31.9% of Vine reviews were 5 stars. 51.8% of Non-Vine reviews were 5 stars.
- Because Vine reviews did not result in a greater percentage of 5-star reviews than Non-Vine reviews, I can conclude that there is no positivity bias related to Vine reviews.

I performed an additional analysis that looked at the average star rating for Vine and Non-Vine reviews.

![image](https://user-images.githubusercontent.com/70069730/153781236-fdf460b4-505f-4483-b874-ed4180fac437.png)

The average for Vine reviews is 3.9, and the average for Non-Vine reviews is 3.8. These are relatively close, and supports my previous conclusion. To further support it, I also looked at the percent of Vine and Non-Vine reviews to the total.

![image](https://user-images.githubusercontent.com/70069730/153781253-dd0d2ff1-54f6-47de-a364-67a3a5711173.png)

Over 99% of watch reviews were Non-Vine. This further indicates no positivity bias towards Vine reviews, as consumers saw significantly more Non-Vine reviews to help make their purchase determination.


