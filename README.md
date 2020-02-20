# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Predicting Affluence in Manhattan using Yelp Pricing Data


<img src="../images/yelp pic.png" width="300px">
<img src="../images/census pic.png" width="300px">

### Authors:
- [Alex Lau](https://www.linkedin.com/in/alex-lau-data-science/)
- [Despina Matos](https://www.linkedin.com/in/despina-matos/)
- [Julie Vovchenko](https://www.linkedin.com/in/julievovchenko/)
- [Kelly Wu](https://www.linkedin.com/in/kelly-wu-nj/)

<img src="../images/Manhattan Skyline.jpg" width="800px"> 

(Manhattan's Skyline)

### Table of Contents:

- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Conclusions](#Conclusions)
- [Limitations](#Limitations)
- [Recommendations](#Recommendations)
- [Sources](#Sources)

---
### Problem Statement

According to [FEMA](https://www.fema.gov/blog/2015-04-29/everyone-must-be-prepared-emergencies), the importance of preparing ourselves for disasters is universal. Thus, when these situations occur, it is a difficult task for organizations or nations to decide where to send initial resources. Our client, [New Light Technologies](https://newlighttechnologies.com/), is interested in utilizing community data as a practical solution to help organizations or nations with this pressing matter. Specificically, **can Yelp's cost estimates ($, $$, $$$) determine neighborhood affluence?** 

Given the neighborhood affluence, it is great source for determining disaster-resistance. Therefore, scraping Yelp's data by using [Yelp's API](https://www.yelp.com/fusion) and connecting zipcodes from business locations to [United State Census](https://2020census.gov/?cid=20002:%2Bus%20%2Bcensus:sem.ga:p:dm:en:&utm_source=sem.ga&utm_medium=p&utm_campaign=dm:en&utm_content=20002&utm_term=%2Bus%20%2Bcensus) data, we can determine if Yelp's data correlates with affluence. We also decided our location for our research will be the borough of Manhattan because there were number of natural disasters in this location and this location is extremly diverse.  We will use various supervised machine learning models and we will use our models' accuracy scores as the way to determine the best model.  


---

### Executive Summary

We began by determing how big of a scope our Yelp data should be and what supplement data source we should include with our Yelp dataset. We decided on using Yelp's Manhattan data because we were able to satisfy the requirements for answering the problem statment. In addition, we decided on using the Census data because it was easily accessible to acquire income data with Manhattan's zipcodes. In other words, we used the Census data because it was able to influence our definition of "affluence". We determined our "affluence rate" after exploring our final dataset.  

Next, we pulled our Yelp data by using Yelp's API and collected our Census income data by filtering with Manhattan's zipcodes on their website. The Yelp data was imported was in JSON format. Therefore, we need to create a dataframe in Pandas to have easier access to clean and multiplate through the data. For the Census data, it was already in a dataframe that we could multiplate through. 

Once, we looked through the dataframes, we looked for particular features. In the Yelp data, we created two datsets. One called restaurants, where we focused on `name`, `review_count`, `rating`, `zipcode` and `type` features. The second one, called yelp_data, we focused on `zipcode`, `price_$`, `price_$$`, `price_$$$`, and `price_$$$$` features. We chose two datasets because we wanted to see if we should include types of businesses in our model. In the Census data, we created two datasets as well. One called census_income, where we focused only on `zipcode` and `medium_income` features. The second one, called census_breakdown, we focused on `zipcode` and the breakdown of ranges for household income. We chose two datasets because one was for modeling and the other was for exploratory analysis. 

With creating these four datasets, we did some data cleaning in each. We checked for duplicate posts, missing values, dropped data not related, and extracted the correct details for our problem statement.

Then, we did some exploratory data analysis. (Got to look at what Juile did).

Next, we were able to preprocess. We merged our datasets, yelp_data and census_income, into one. Then, we created our X feature and determed our "affluence rate" which was our target variable. We also did a train-test split. Lastly, we determined a basline score to compare to our models' results.

Finally, we were able to model. We modeled regression models and classification models. (Got to look at Alex and Kelly's models)

In the end, we focused on accuracy score and the bias-variance tradeoff from each classification model to determined which model was the best to answer our problem statement.

---

### Conclusions 

---

### Limitations

---

### Recommendations

---

### Sources

# Predicting-Affluence-in-Manhattan-using-Yelp-Pricing-Data
