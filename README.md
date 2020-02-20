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

According to [FEMA](https://www.fema.gov/blog/2015-04-29/everyone-must-be-prepared-emergencies), the importance of preparing ourselves for disasters is universal. Thus, when these situations occur, it is a difficult task for organizations or nations to decide where to send initial resources. Our client, [New Light Technologies](https://newlighttechnologies.com/), is interested in utilizing public and easily accessible data as a practical solution to help organizations or nations with this pressing matter. Specificically, **can Yelp cost estimates ($, $$, $$$) determine neighborhood affluence?** 

Given the neighborhood affluence, it is a great source for determining disaster-resistance. Therefore, scraping Yelp's data by using [Yelp's API](https://www.yelp.com/fusion) and connecting zipcodes from business locations to [United State Census](https://2020census.gov/?cid=20002:%2Bus%20%2Bcensus:sem.ga:p:dm:en:&utm_source=sem.ga&utm_medium=p&utm_campaign=dm:en&utm_content=20002&utm_term=%2Bus%20%2Bcensus) data, we can determine if Yelp's data correlates with affluence. We also decided our location for our research will be the borough of Manhattan because there were a number of natural disasters in this location and this location is extremely diverse. We will use various supervised machine learning models and we will use our models' accuracy scores as the way to determine the best model.  


---

### Executive Summary

We began by determing how large of a scope our Yelp data should be location wise and what supplemental data source we should include with our Yelp dataset. We decided on using Yelp's Manhattan data because we were able to satisfy the requirements for answering the problem statment. In addition, we decided on using the Census data because it was easily accessible to acquire income data with Manhattan's zipcodes. In other words, we used the Census data because it was able to influence our definition of "affluence". We determined our "affluence rate" after exploring our final dataset.  

Next, we pulled the Yelp data by using Yelp's API and collected the Census income data by filtering with Manhattan's zipcodes on the Census' website. The Yelp data was imported was in JSON format. Therefore, we need to create a dataframe in Pandas to have easier access to clean and manipulate through the data. For the Census data, it was already in a dataframe that we could manipulate through. 

Once, we looked through the two dataframes, we looked for particular features. In the Yelp data, we primarily focused on cost estimates. In the census data, we primarily focused on household income. With creating these datasets, we did data cleaning in each. We checked for duplicate posts and missing values. We also dropped data that was not related and isolated data from columns that benefited to answering our problem statement. 

Once our datasets were cleaned, we did some exploratory data analysis. We analyzed trends and correlations between median income and restaurants’ cost estimates through bar graphs and geomapping.

Next, we were able to preprocess. We merged four datasets together into one to get a master dataset. With some trial and error, we decided to do feature engineering. We create an average cost estimate for each zipcode because we wanted to determine if there was a relationship between the average and the median income. Then, we created our X feature and determined our "affluence rate" which was our target variable. We also did a train-test split. Then, we determined a baseline score to compare to our models' results.

Lastly, we were able to model. We modeled various classification models with various hyperparameters. 

In the end, we focused on accuracy score and the bias-variance tradeoff from each classification model to determine which model was the best to answer our problem statement. 

---

### Conclusions 

Yelp cost estimates can determine a neighborhood’s affluence. It isn’t perfect as there may be other underlying factors that can affect affluence more than the Yelp cost estimates of restaurants. Since our best model, Voting Classifier, quite accurately predicts affluence of neighborhoods based on public and easily accessible data, we can allocate resources based on affluency during emergencies; primarily focusing on less affluent neighborhoods.

---

### Limitations

---

### Recommendations

---

### Sources

