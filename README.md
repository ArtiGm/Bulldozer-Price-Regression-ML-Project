# Bulldozer-Price-Regression-ML-Project
How well can I predict the future sale price of a bulldozer, given its characteristics previous examples of how much similar bulldozers have been sold for?

I'm going to go through an example machine learning project to use the characteristics of bulldozers and their past sales prices to predict the sale price of future bulldozers based on their characteristics

Since I'm trying to predict a number, this kind of problem is a regression problem and since I'm going to predicting results with a time component (predicting future sales based on past sales), this is also a time series or forecasting problem.

Looking at the dataset from Kaggle we see that it contains historical sales data of bulldozers. Including things like, model type, size, sale date and more.

Inputs: Bulldozer characteristics such as make year, base model, model series, state of sale (e.g. which US state was it sold in), drive system and more.
Outputs: Bulldozer sale price (in USD).

There are 3 datasets:

Train.csv - Historical bulldozer sales examples up to 2011 (close to 400,000 examples with 50+ different attributes, including SalePrice which is the target variable).
Valid.csv - Historical bulldozer sales examples from January 1 2012 to April 30 2012 (close to 12,000 examples with the same attributes as Train.csv).
Test.csv - Historical bulldozer sales examples from May 1 2012 to November 2012 (close to 12,000 examples but missing the SalePrice attribute, as this is what we'll be trying to predict).

You can download the dataset bluebook-for-bulldozers dataset directly from the Kaggle competition: https://www.kaggle.com/competitions/bluebook-for-bulldozers/data

How I'm going to evaluatee this?

For this problem, Kaggle has set the evaluation metric to being root mean squared log error (RMSLE). As with many regression evaluations, the goal will be to get this value as low as possible (a low error value means our model's predictions are close to what the real values are).

To see how well the model is doing, I'll calculate the RMSLE. 

