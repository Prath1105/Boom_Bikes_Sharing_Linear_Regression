# Boom_Bikes_Sharing_Linear_Regression
# Bike Demand Prediction using Multiple Linear Regression

## Introduction
BoomBikes, a US-based bike-sharing provider, has seen a significant decline in revenue due to the COVID-19 pandemic. As the economy recovers, BoomBikes wants to understand the **demand for shared bikes** after the lockdown ends. To achieve this, the company has gathered data on daily bike rentals and various influencing factors.

This project aims to develop a **multiple linear regression model** to predict the demand for shared bikes, helping BoomBikes optimize their business strategy and maximize revenue.

## Business Objective
BoomBikes seeks to:
- Identify **key factors affecting bike demand**.
- Understand **how variables influence rental rates**.
- Develop a data-driven model to **forecast future demand**.
- Improve **strategic planning and profitability**.

## Dataset
The dataset contains daily bike demand data across the American market, including:
- **Seasonal & Weather Factors:** Temperature, humidity, wind speed, weather conditions.
- **Temporal Factors:** Year (`yr`), month, day type (weekday/weekend).
- **User Information:** Casual vs. registered users (`casual`, `registered`).
- **Target Variable:** `cnt` (total number of bike rentals).

## Data Preparation
Certain variables in the dataset need preprocessing:
- Convert **categorical numeric variables** like `season` and `weathersit` into string categories.
- Retain the `yr` column, as demand trends may change over years.
- Use `cnt` (total rentals) as the target variable.

## Modeling Approach
1. **Exploratory Data Analysis (EDA)** - Understanding trends and correlations.
2. **Feature Engineering** - Selecting significant predictors.
3. **Multiple Linear Regression Model** - Building the predictive model.
4. **Residual Analysis** - Checking model assumptions.
5. **Model Evaluation** - Using the **R-squared score** to measure accuracy.

## Model Evaluation
To assess the model performance on the test set:
```python
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
