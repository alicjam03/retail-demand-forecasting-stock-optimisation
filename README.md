# Retail Demand Forecasting and Stock Optimisation

## Project Overview
This project explores how data science can be used to support retail decision-making through demand forecasting and stock optimisation.

Using a synthetic retail dataset containing pricing, discount, promotion, inventory, and competitor pricing information, I carried out exploratory data analysis, improved the realism of the dataset, built predictive models, and translated the outputs into business recommendations for stock management.

## Objectives
- Identify key drivers of product demand
- Build predictive models to forecast units sold
- Compare model performance across different machine learning approaches
- Use predicted demand to identify understock and overstock scenarios
- Generate business-focused recommendations for inventory optimisation

## Dataset
The original dataset contained retail variables such as:
- Units Sold
- Inventory Level
- Units Ordered
- Price
- Discount
- Holiday/Promotion
- Competitor Pricing
- Seasonality
- Weather Condition

Initial exploratory analysis showed that some key variables did not meaningfully influence demand, which limited the realism of the data. To improve the usefulness of the dataset for modelling, I introduced more realistic relationships between demand and key retail drivers such as price, discount, and promotions.

## Exploratory Data Analysis
Key findings from the initial analysis included:
- Demand Forecast was perfectly correlated with Units Sold, indicating data leakage
- Price, Discount, and Holiday/Promotion initially had almost no relationship with sales
- Competitor Pricing was highly correlated with Price
- The dataset required refinement before meaningful modelling could take place

After improving the data, the analysis showed:
- A clear negative relationship between price and units sold
- Positive effects of discount and promotions on demand
- Stronger and more interpretable feature relationships overall

## Modelling
I trained and compared multiple models:
- Linear Regression
- Random Forest Regressor
- XGBoost

### Best Model
Linear Regression achieved the best cross-validated performance for this dataset.

- Cross-validated RMSE: approximately 10.01 units

This result was expected because the improved dataset contained strong linear relationships between key variables and demand.

## Feature Importance
Feature importance analysis showed:
- Linear Regression: Inventory Level, Discount, Holiday/Promotion
- Random Forest: Inventory Level, Price, Discount
- XGBoost: Price, Discount, Inventory Level

This comparison highlighted how different models interpret the same data:
- Linear models focused on direct relationships
- Tree-based models captured more distributed, non-linear interactions

## Stock Optimisation
Predicted demand was compared with current inventory levels to classify stock into:
- Overstock
- Understock
- Optimal

### Results
- Overstock: 39,532
- Understock: 27,030
- Optimal: 6,538

This means that only a small proportion of stock was at optimal levels, while the majority was either over
