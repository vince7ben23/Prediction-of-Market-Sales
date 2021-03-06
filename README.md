# Prediction-of-Market-Sales

## Problem Statement

Have collected sales data for 1559 products across 10 stores in different cities of 2013 year. The aim is to build a predictive model and find out the sales of each product at a particular store.

With this model, find out the properties of products and stores which play a key role in increasing sales.

 
## Data

Find the data-set from thses files, 

train data: [train.xlsx](train.xlsx)

test data: [test.xlsx](test.xlsx)

train data after data-clean: [train_optimized.xlsx](train_optimized.xlsx)

test data after data-clean: [test_optimized.xlsx](test_optimized.xlsx)

Train (8523) and test (5681) data set, train data set has both input and output variable(s).

| Variable| Description|
|----------------------|-------------------------------|
| Item_Identifier| Unique product ID|
| Item_Weight| Weight of product|
| Item_Fat_Content| Whether the product is low fat or not|
| Item_Visibility| The % of total display area of all products in a store allocated to the particular product|
| Item_Type| The category to which the product belongs|
| Item_MRP| Maximum Retail Price (list price) of the product|
| Outlet_Identifier| Unique store ID|
| Outlet_Establishment_Year| The year in which store was established|
| Outlet_Size| The size of the store in terms of ground area covered|
| Outlet_Location_Type| The type of city in which the store is located|
| Outlet_Type| Whether the outlet is just a grocery store or some sort of supermarket|
| Item_Outlet_Sales| Sales of the product in the particulat store. This is the outcome variable to be predicted.|


## Evaluation Metric

This model performance will be evaluated on the basis of the prediction of the sales for the test data, which contains similar data-points as train except for the sales to be predicted.

This is a practical problem provided by <b>Analytics Vidhya</b>, they have the actual sales for the test dataset, against which my predictions will be evaluated. using the Root Mean Square Error value as the judgment standard.

![title](rmse_1.png)


N: total number of examples.

Predicted: the sales predicted by my algorithm.

Actual: actual values of sales.

## Code Overview

There are two seperated scripts, to deal with data preprocessing and model evaluation respectivly.

Data preprocessing  [data_preprocess.ipynb](data_preprocess.ipynb): 
 - do data exploration first, then deal with missing value and ''not make sense'' value, and find new feature via feature engineering, prepare the clean data for prediction.

Model evaluation  [model_evaluating.ipynb](model_evaluating.ipynb): 
 - in this project, predict product sales with two machine learning algorithms, multi-variable regression and decision-tree, and use cross-validation and learn curve to evaluate the performance of each model. 
 
