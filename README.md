# coffee_sales
# Coffee Sales Analysis

This project analyzes coffee sales data from a vending machine to understand purchasing patterns, sales trends, and product performance. It also uses machine learning models to predict sales based on features like time, coffee type, and payment method.

## Project Overview

**Dataset:** Daily coffee transactions (March 2024 – July 2024)
**Tools Used:** Python, Pandas, Matplotlib, Seaborn, Scikit-learn
**Models:** Linear Regression, Random Forest Regressor
**Objective:** 
  - Analyze sales trends by time, product, and customer behavior
  - Forecast future sales
  - Identify key factors impacting revenue

## Data Cleaning & Preparation

- Converted `date` and `datetime` columns to `datetime64`
- Handled missing values in:
  - `card`: replaced with `'cash'`
  - `coffee_name`, `cash_type`: filled with mode
- Created new features:
  - `hour`, `dayofweek`, `month` from timestamp

## Exploratory Data Analysis

Visual insights revealed:

**Most Popular Products:** Americano with Milk, Latte
**Peak Hours:** 10 AM and 7 PM
**Peak Day:** Tuesday
**Revenue Leaders:** Latte and Americano with Milk
**Low Performers:** Cocoa, Espresso

> EDA techniques: heatmaps, bar charts, time series plots, product-hour analysis

## Machine Learning Models

### 1. Linear Regression

- Used one-hot encoded features: `coffee_name`, `cash_type`, `dayofweek`
- Model performance:
  - **R² Score:** 0.82
  - **MSE:** 3.39

### 2. Random Forest Regressor

- Better performance on nonlinear relationships
- Model performance:
  - **R² Score:** *higher than LR*
  - **MSE:** *lower than LR*

### Feature Importances
- Top features influencing sales:
  - `hour`, `coffee_name_Latte`, `dayofweek_Tuesday`, `cash_type_card`

## Export

- Saved predicted vs actual sales to `coffee_sales_predictions.csv`

## Future Enhancements

- Add time-series forecasting (e.g., Prophet or ARIMA)
- Create a Streamlit dashboard for interactive analysis
- Add clustering for customer segmentation



## File Structure

