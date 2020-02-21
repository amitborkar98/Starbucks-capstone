#  STARBUCKS CAPSTONE PROJECT

## Table of contents:
1)Introduction
2)Installations
3)Project files
4)Problem Statement
5)Results
6)Conclusion

## Introduction
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.
Not all users receive the same offer, and that is the challenge to solve with this data set.

## Installations
You will need the standard data science libraries found in the Anaconda distribution of Python. 
The code should run with no issues using Python versions 3.
Libraries used: Numpy, Pandas , sklearn, matplotlib

## Project Files
data - contains data(Json format) used in the project(profile, portfolio and transcript)
Starbucks_Capstone_notebook - Jupyter notebook used for the project
comined.csv - Comined data used for analysis 
KNeighborsClassifier_df.csv - accuracy score and best parameters of the model.
RandomForestClassifier_df.csv - accuracy score and best parameters of the model.
BaggingClassifier_df.csv -  accuracy score and best parameters of the model.
AdaBoostClassifer_df.csv - accuracy score and best parameters of the model.
RandomForestRegressor_df.csv - accuracy score and best parameters of the model.
GradientBoostingRegressor_df.csv -  accuracy score and best parameters of the model.

## Problem Statement
The data set contains records of multiple offers. The portofolio, profile and transcript data needs to be combined and analysed. The problem which needs to be solved is:-
A) Descriptive Statistics
1) Analyse the best age-range, income range for each offer type
2) Analyse the offer-successfull percentage
3) Analyse the average-amount spent for each offer-type where the offer was successfull
4) Analyse the best offers for each age-range, income-range, customer joined date
5) Analyse the offer completion rate for each age-range and income range
B) Predictive Modeling- Machine Learning
1) Predict the offer successfull rate
2) Predict the amount spent by the customers during offer duartion period.
C) Recommendations
1) Rank-based - For new users
2) User-User based collaborative filtering- for users who have successfully completed atleast 1 offer
Metrics used to measure performance of the model
A) For Classification model:
1) Accuracy score - to measure the accuracy of the model
2) F1 score - to measure the balance between precision and recall
B) For Regression model:
1) Mean-absolute-error - to measure the mean average error in the model
2) Median-absolute-error - to measure the meadian average error

## Results
1)The results of the descriptive analysis are provided above
2)AdaBoostClassifier should be used for predicting the offer completion which yields the accuracy score of 0.95 for training data and 0.91 for testing data
3)GradientBoostingRegressor should be used for predicting amount spent which yields the mean absolute score of 13 for training data and 21 for testing data.
4)Rank based and User-User collaborative filtering recommendations were implemented successfully.

## Conclusion
Results were obtained as expected with good accuracy score and error score respectively. The profile, portofolio data was cleaned in the first part of the project. Later, Transcript data was cleaned and splitted in to offers data and transactions data. The most challenging part of the project was to combine the portfolio, profile, transaction_df and offers_df dataframe to get whether the offer is successfull and to get the amount spent by in customers in the offer duration period. Multiple models were created for predicting the whether the offer is successfull, where the best results were obtained from the AdaBosstClassifier. Later, RandomForestRegressor and GraientBoostingResgressor were used to train the model to predict the amount spent, where using GraientBoostingResgressor obtained a better error. Rank and User-User based collaborative filtering was used to recommend offers to the customer.

Link to the medium article - https://medium.com/@amitborkar98/starbucks-analyzing-offers-aeb27a27bc54