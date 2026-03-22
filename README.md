# Retail Demand Forecasting and Stock Optimisation

## Overview
This project explores retail demand forecasting and stock optimisation using a synthetic retail dataset. The goal was to predict units sold, understand the main drivers of demand, and identify understock and overstock situations to support better inventory decisions.

## Objectives
- Analyse retail sales and inventory data
- Identify key drivers of demand
- Build and compare predictive models for units sold
- Use predicted demand to support stock optimisation
- Translate model outputs into business recommendations

## Dataset
The project began with a synthetic retail inventory dataset containing variables such as:
- Units Sold
- Inventory Level
- Price
- Discount
- Holiday/Promotion
- Competitor Pricing
- Seasonality

During exploratory analysis, I found that some key business variables showed little or no realistic relationship with demand. To improve the usefulness of the dataset for modelling, I introduced more realistic demand behaviour such as:
- negative price elasticity
- positive discount effects
- promotional uplift
- inventory constraints

## Workflow
1. Exploratory Data Analysis  
   - correlation analysis
   - scatter plots
   - grouped comparisons
   - identification of unrealistic relationships and data leakage risks

2. Data Improvement  
   - adjusted synthetic demand relationships to reflect more realistic retail behaviour
   - created a revised target with interpretable business drivers

3. Modelling  
   - Linear Regression
   - Random Forest Regressor
   - XGBoost
   - model comparison using RMSE and cross-validation

4. Stock Optimisation  
   - compared predicted demand with inventory level
   - classified stock as understock, overstock, or optimal
   - generated business recommendations

## Key Results
- Linear Regression achieved the best performance with RMSE of approximately 10 units
- Price showed a strong negative relationship with demand
- Discount and promotions had positive effects on units sold
- Stock analysis showed:
  - Overstock: 39,532
  - Understock: 27,030
  - Optimal: 6,538

These results suggest substantial inefficiencies in inventory allocation, with overstocking representing the largest issue.

## Business Insight
The project shows how predictive modelling can support retail decision-making by improving stock allocation. The findings suggest that demand-driven inventory planning could reduce excess stock, lower holding costs, and reduce missed sales opportunities.

## Tools and Technologies
- Python
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn
- XGBoost
- Jupyter Notebook


## Future Improvements
- Add product-level seasonal effects
- Build an interactive Power BI or Tableau dashboard
- Incorporate returns and category-level demand behaviour
- Extend optimisation logic to recommend reorder quantities


