# Predicting Housing Prices: Project Overview 
* Created a tool that estimates housing price (MAE ~ $20K) to help predicting housing prices based on house's features
* Optimized Linear to reach the best model. 
* Deployed one-hot encoding to turn 60+ categorical columns of data into numerical types

## Code and Resources Used 
**Python Version:** 3.10
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn
**Dataset:** https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data  

## Data Cleaning
After scraping the data, I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

*	Created a frame of train data and test data so that they both can be processed simultaneously 
*	Filled out Null values when the columns have enough values
*	Created an object_list to store columns that has object dtype 
*	Created a dummies dictionary to contain sub-dataframes which has been converted to dummies
*	Concatenated all sub-dataframes in dummies
*	Dropped columns that have had converted by dummies

## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![alt text](https://github.com/ahnngo/house-prices-advanced-regression-techniques/blob/master/Charts/Null%20Values%20Count.png)

## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 30%.   

I tried three different test size and evaluated them using Mean Absolute Error. I chose 30% because it gave the the lowest MAE of $20k.   

## Model performance
* MAE: 20885.35859244997
* MSE: 1513293840.693288
* RMSE: 38901.07762894606

![alt text](https://github.com/ahnngo/house-prices-advanced-regression-techniques/blob/master/Charts/y_test%20vs.%20prediction.png)
![alt text](https://github.com/ahnngo/house-prices-advanced-regression-techniques/blob/master/Charts/Error%20Distribution.png)


