# Machine Learning Engineer Nanodegree
## Capstone Proposal
Hongxia(Sophie) Hou 
December 10th, 2021
 
## Proposal
 
### Domain Background

Nowadays, more and more shops, ecommerce are aiming to utilise the data in order to understand how the customers think, feel and decide, so the businesses can determine how best to market their products, services and which sales promotion strategies really work.
 
Starbucks, one of biggest chain of coffee shops, not only go through mounds of coffee beans to satiate it’s raving fans, but they also have mounds of data that they leverage in many ways to improve the customer experience and their business.[source](https://bernardmarr.com/starbucks-using-big-data-analytics-and-artificial-intelligence-to-boost-performance/)
 
This project data is provided by Udacity in collaboration with Starbucks as the capstone project of Machine Learning Engineer Nanodegree. The data is simulated data that mimics customer behavior on the Starbucks rewards mobile app during a month experiment. How can we analyze the data and turn it into meaningful insights to help improve current rewards offer strategy.    
 
### Problem Statement

People often say one thing but do another, and different people respond to the same thing in different ways. Starbucks rewards mobile app sends out an offer to users once every few days. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO(buy one get one free). Some users might not receive any offer during certain weeks.
 
The goal of this project is:

* To carry out data exploratory analysis to discover which demographic groups are there and what the offers are that really excite them? In another word, what the best offer is, not just for the population as a whole but at an individual level. In addition, to identify which demographic group may respond to the offer negatively or do not want to see the offer at all.
* To build a machine learning model to predict which action a customer may take. 
 
### Datasets and Inputs

The project contains three datasets:

1. Portfolio 

   * Containing basic info about each offer, such as `offer_id`, `offer_type`, `duration` for how many days the offer will be valid, `difficulty` for how much amount need to spend in order to get reward or complete the offer, `reward` for how much amount the user will get after an offer complete, `channel` for which channel to carry a certain type of offer.

   * We can use this dataset combined with other dataset by matching the same `offer_id` to analyse how each offer’s performance during this experiment.

2. Profile

   * Containing demographic information about each user, such as `age`, `gender`, `id`, `income` and `became_member_on` for when a user became Starbucks’ member.

   * We can segmentate the user based on different traits, together with other tables, we could discover how each group of users respond to different offers, so that we can determine which offer attracts which group more.

3. Transcript

   * Containing all the events, such as when a user received an offer, when a user opened an offer, when a user completed an offer and got reward, also every single transaction which a user has made. Another important info in this dataset is `time` for which hours happened for each user and each event, it’s from 0hour when the experiment started to the experiment end(at 714 hours)

   * This dataset will let us be able to find out which users did not open/respond to which offer, which users opened which offer but not completed, which users opened and completed which offer, which users completed which offer without seeing it. Together with the previous two dataset, we can segment users into different groups and also we can train a ML model and test how the model predicts the possible action a user could take. 
 
### Solution Statement

I will use EDA(exploratory data analysis) and Exploratory visualization to discover which offer is the best offer and which group like which offer most by:

* Comparing distributions, mean, median for each variable.

* Calculate and compare view_rate and complete_rate with/without influence at each type offer and each group of user level calculate mean, median and machine learning classification algorithm.

* Visualizing with KDE plot and Boxplot.
 
I will also use Support Vector Classification algorithm and Random Forest Tree classification algorithm to build the model, train and test and compare to predict action the customer will take.
 
### Benchmark Model

For the EDA (exploratory data analysis) part, the benchmark is just comparing among the groups percentage of received, viewed and completed at each type of offer level. 

For the predictive model part, we compare performance between two different machine learning models to see which performs better.
 
### Evaluation Metrics
To determine which offer is the winner, I will use:

* View_rate: which is total views divided by total number of receive
* Influence_complete_rate: which is total number of completion with view record in advance divided by total number of receive
* Uninfluence_complete_rate: which is total number of completion without view record before divided by total number of receive
 
To determine which predictive model perform better, I will use:

* Confusion matrix to visualize TP(True Positive), TN(True Negative), FP(False Positive), FN(False Negative).
* Accuracy score: which is (TP+TN)/dataset size
* Precision score: which is how many TP from total predicted positive(TP+FP)
* Recall score: which is how many TP from actual positives(TP+FN)
 
### Project Design
To work on this project, I plan to follow following steps:

1. Get environment setup and data imported
2. Understand each table and each variable by exploring the data, such as check the null value, run the statistical summary, randomly pick some users, check how the event flow looks like in the dataset, etc.
3. EDA and exploratory visualisation. 
4. Manage data, clean the data and do the transformation. I will reshape the table and merge tables, to make each received offer followed by a corresponding view, then corresponding completion. ALso prepare the table for the machine learning classification algorithm.
5. Statistical analysis and understand relationships between variables. I will check the view_rate, complete_rate, check the correlations, etc.
6. Build/train/test the models and compare the models, like mentioned above, two classification models will be built/trained and tested, which are Support Vector Classification and Random Forest Tree classification.
7. Conclusion with insights and recommendations. I will answer the questions which mentioned above and recommend what the next step could be.
