# Big Mart Sales Prediction

## Objective
This project aim to predict food sales based on various factors. In the ever-evolving world of retail and food service, understanding sales patterns is crucial for business planning and growth. The project focuses on leveraging analytical and modeling techniques to forecast food sales. The goal is to build a model that can accurately predict future sales, helping businesses to manage inventory, optimize supply chain processes, and ultimately increase profitability.

## Data Description

### Overview
The dataset includes informations for 2013 sales data for 1559 products across 10 stores in different cities, such as the type of food, price, location of sale, promotional details and historical sales.
This dataset contains 8523 rows and 12 columns.

### Data Source
The dataset for comes from Aalytics Vidhya platform which is originally collected by a big mart employees.
Link to dataset: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/#ProblemStatement

### Data Dictionary

<p align = "center"> 
  <img src = https://github.com/Mahdi-Kriaa/food_sales_prediction/blob/main/Images/data_dictionary.PNG>
</p>

## Methodology
We will employ various data preprocessing techniques to handle missing values and categorical variables. We will explore different machine learning models, including random forests and gradient boosting, to predict the sales for each store. Model performance will be evaluated based on different metrics such as r2 and RMSE.

## Exploratory Data Analysis

To explore the dataset the following plots were used:

    - a boxplot and histogram was visualized for each numeric datatype column. 
    - a boxplot was visualized for each categorical column.
    - a contingincy matrix for some categorical column
    

<p align = "center"> 
  <img src = "https://github.com/Mahdi-Kriaa/food_sales_prediction/blob/main/Images/sales_hist_box.png">
</p>

This histogram shows that the majority of the sales are less than $6,200.
 
To visualize the data for explantory purposes, a barplot and regplot were chosen.

    - the barplot was chosen to show how the types affect sales. 
    - the regplot was chosen to show the trend of sales over the item MRP depending on the outlet type.

<p align = "center"> 
  <img src = "https://github.com/Mahdi-Kriaa/food_sales_prediction/blob/main/Images/outlet_size_vs_sales.png">
</p>


We see that sales increase in medium stotes and decrease in small ones.


<p align = "center"> 
  <img src = "https://github.com/Mahdi-Kriaa/food_sales_prediction/blob/main/Images/item_mrp_vs_sales_trend.png">
</p>


We see that sales trend increase linearly with the item price for each type of store

## Machine Learning 

### Machine Learning Models

Models used in this project are the following :

    - Linear Regressor
    - KNN
    - Decision Tree
    - Random Forest
    - AdaBoost
    - XGBoost
    - Stacking Regressor
    
We note that neural networks models were not preferred as we are dealing with structred data.

### Models Evaluation & Results

The following are the Mean Absolute Error scores for each model with default tuning, for the testing set:

    - Linear Regressor: 826.40
    - KNN: 857.50
    - Decision Tree: 1073.82
    - Random Forest: 790.23
    - AdaBoost: 970.10
    - XGBoost: 825.61
    - Stacking Regressor: 786.732

The Final Model Chosen was a tuned stacking regressor . For the testing set the model, `57.81%` of the variance in sales was explained by features and the Mean Absolute 
Error score had a calculation of `$1102.73`.

## Recommendations
- The use of this model to predict the sales of an item in a store is reliable for an error tolerance of 812$.
- To boost sales, we must mainly choose the optimal items prices and outlet type.

## Limitations & Next Steps

The model is not reliable for an error tolerance less than 812$, so, other features can be added like historical sales and economic indicators, also the
data samples number is not very high and providing more samples could improve the model performance.



 
