# Amazon_Vine_Analysis

## Analysis Summary

This project was proposed to analyze the Amazon Vine program to assess if it creates a bias in review data.  Various tools were used for this analysis from Pyspark, ETL, AWS RDS instance, and PGadmin for queries.  The data we analyzed was Digital Video games.

## Results

Unfortunately, the dataset we choose was not the best one for this analysis.  The Digital video game dataset had 0 vine reviews so the analysis only shows what is created from the non-paid reviewers.

In the snip below you can see that first the data was filtered for only those reviews which had more than 20 total votes.

![image](https://user-images.githubusercontent.com/107594247/194798963-44d0b6ca-3635-4cc4-a29a-af121f579a2f.png)

Then the data was split into two frames, one with Y for vine and one with N for vine (shown below)

![image](https://user-images.githubusercontent.com/107594247/194799016-22e3e570-ca70-414d-aa4b-0cf8bdc2d163.png)

This is where the issue became clear.  The Dataframe for the Y's was empty as there were no vine reviews to split out.  The N's was a more full data frame

Analyzing the N's however, we can see that the average score given was 3.17 stars and there were 631 5's out of 1685 total reviews.

![image](https://user-images.githubusercontent.com/107594247/194799098-6490858a-2fc1-4955-8327-0011911a206f.png)


I suggest if this effort were done again, a different data set should be used for better analysis. 
