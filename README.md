# Ames, IA Real Estate Prices: Regression Model and Notebook

The purpose of this project is to predict the price of housing in the city of Ames, IA using real estate feature
data and different regression models. The model with the lowest error score is selected for Real Estate value predictions.

Features such as Lot Size, Number of Bedrooms and the Age of the House are examples of factors to help predict the 
price of real estate in Ames, IA. Feature importance is also calculated and is used to determine the importance of each
Housing feature in the model's prediction.

The models selected for this project are Decision Tree Regression, Random Forest Regression and XGBoost Regression.
Each of these models come from the Sci-Kit Learn machine learning library.

**Root Mean Squared Error (RMSE)** is a metric of evaluation that is used to determine error losses when a
regression model is run. The error is the difference between the predicted
real estate prices with the true real estate prices in each model.

A link to its entire definition is provided [here] (#https://en.wikipedia.org/wiki/Root-mean-square_deviation)

In the case of RMSE, the presence of outliers causes the error value to maginify to a very high value. 
Thus, RMSE is sensitive to outliers. Additionaly, the RMSE value **increases in magnitude if the scale of error increases.**

## Root Mean Log Squared Error

For this project, the **Root Mean Squared Log Error (RMSLE)** metric will be used instead!
With the RMLSE metric, outliers are drastically reduced which minimizes their effect
on the model.

The RMSLE metric only considers the relative error between the Predicted and the Actual value.
Thus the scale of the error is not significant. 

A key advantage of using the RMSLE is that it incurs a larger penalty for the underestimation of the Actual variable than the Overestimation.

Thus, a higher penalty is incurred when the **Predicted Value is less than the Actual Value**. Conversley, less penalty is incurred when the predicted value is more than the actual value. This is useful for scenarios where overestimating a target is less important than underestimating a target![https://medium.com/analytics-vidhya/root-mean-square-log-error-rmse-vs-rmlse-935c6cc1802a]


## Data Analysis

### Display top 10 positively correlated features with target (SalePrice)

<p style="text-align:center;">
    <img width="400" alt="Feature Variable vs. Target Variable (SalePrice) - Correlation Scor" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/Feature_vs_TargetCorrelationScore.png?raw=true">


### Average Price of Home by Neighborhood

<p style="text-align:center;">
    <img width="400" alt="AveragePriceofHomebyNeighborhood" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_AveragePriceofHomebyNeighborhood.png?raw=true">
    
### AmesIA_RealEstate_YearBuilt_vs_SalePrice

<p style="text-align:center;">
    <img width="400" alt="AmesIA_RealEstate_YearBuilt_vs_SalePrice" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstate_YearBuilt_vs_SalePrice.png?raw=true">
    
### AmesIA_RealEstate_OveralQual_vs_SalePric

<p style="text-align:center;">
    <img width="400" alt="AmesIA_RealEstate_OveralQual_vs_SalePrice" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstate_OveralQual_vs_SalePrice.png?raw=true">
    
### RealEstate_OveralQual_vs_SalePrice

<p style="text-align:center;">
    <img width="400" alt="AmesIA_RealEstate_OveralQual_vs_SalePrice" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstate_OveralQual_vs_SalePrice.png?raw=true">
    
### Real Estate Data - Correlation Heatmap

<p style="text-align:center;">
    <img width="400" alt="Ames, IA Real Estate Data - Correlation Heatmap" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstateDataCorrelationHeatmap.png?raw=true">
    
### FinalFeature_vs_TargetCorrelationScore

<p style="text-align:center;">
    <img width="400" alt="FinalFeature_vs_TargetCorrelationScore" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/FinalFeature_vs_TargetCorrelationScore.png?raw=true">
    

# Results

For this project the **XGBoost model had the lowest RMSLE score (~0.119)** and was selected as the best prediction Model!
This indicates that the model is 88% accurate in predicting actual RealEstate value prices.

    
