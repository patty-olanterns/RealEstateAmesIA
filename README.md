# Ames, IA Real Estate Prices: Regression Model and Notebook

The purpose of this project is to predict the price of housing in the city of Ames, IA using real estate feature
data and different regression models. The model with the lowest error score is selected for Real Estate value predictions.

Features such as Lot Size, Number of Bedrooms and the Age of the House are examples of factors to help predict the 
price of real estate in Ames, IA. 

The regression models used in this project are Decision Tree Regression, Random Forest Regression and XGBoost Regression.
Each of these models come from the Sci-Kit Learn machine learning library.

## Root Mean Squared Error

**Root Mean Squared Error (RMSE)** is a metric of evaluation that is used to determine error losses when a
regression model is run. The error is the difference between the predicted
real estate prices with the true real estate prices in each model.

A link to its entire definition is provided [here] (https://en.wikipedia.org/wiki/Root-mean-square_deviation)

In the case of RMSE, the presence of outliers causes the error value to maginify to a very high value. 
Thus, RMSE is sensitive to outliers. Additionaly, the RMSE value **increases in magnitude if the scale of error increases.**

## Root Mean Log Squared Error

For this project, the **Root Mean Squared Log Error (RMSLE)** metric is used instead!
Outlier values have a neglible impact on the RMSLE, producing a lower error value.

The RMSLE metric only considers the relative error between the Predicted and the Actual value.

A key advantage of using the RMSLE is that it incurs a larger penalty for the underestimation of the actual variable than the overestimation.

Thus, a higher penalty is incurred when the **Predicted Value is less than the Actual Value**. Conversley, less penalty is incurred when the predicted value is more than the actual value. This is useful for scenarios where overestimating a target is less important than underestimating a target![https://medium.com/analytics-vidhya/root-mean-square-log-error-rmse-vs-rmlse-935c6cc1802a]


## Data Analysis

- The following is a quick visual breakdown of insights between SalePrice (Target feature)
  and all other features in the data set

### Display top 10 positively correlated features with target (SalePrice)

<p style="text-align:center;">
    <img width="800" alt="Top 10 Correlated Features" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/Feature_vs_TargetCorrelationScore.png?raw=true">

### Average Price of Home by Neighborhood

<p style="text-align:center;">
    <img width="800" alt="AveragePriceofHomebyNeighborhood" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_AveragePriceofHomebyNeighborhood.png?raw=true">
    
### Year Built vs. Sale Price

<p style="text-align:center;">
    <img width="400" alt="AmesIA_RealEstate_YearBuilt_vs_SalePrice" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstate_YearBuilt_vs_SalePrice.png?raw=true">
    
### Year Remod Add vs. Sale Price

<p style="text-align:center;">
    <img width="400" alt="Year Remod Add vs. Sale Pricee" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_YearRemodAdd_vs_AvgSalePrice.png?raw=true">
    
### Overall Qual vs. Sale Price

<p style="text-align:center;">
    <img width="800" alt="Overall Qual vs. Sale Price" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstate_OveralQual_vs_SalePrice.png?raw=true">
  
### Real Estate Data - Correlation Heatmap
    
This heatmap displays positive and negative correlations between features for Real Estate in Ames, IA.

<p style="text-align:center;">
    <img width="800" alt="Real Estate Data - Correlation Heatmap" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/AmesIA_RealEstateDataCorrelationHeatmap.png?raw=true">
    
### Select all homes with TotalSF z-score value < 3
   - In a statistical normal distribution, it is good practice to sample data
     with a statistical z-score less than 3. This means any data that within 3 standard deviations
     from the mean of the dataset. Thus, all outliers have a z-score greater than 3 and are dropped
     from analysis.
   - In this dataset, all TotalSF values with a z-score > 3 are dropped                                             
    
### Final Top 10 Correlated Features
    
    - The model with the lowest RMSLE score (XGBoost) is selected
    and final features are modified and selected for use building a 
    final XGBoost Regression model. We ignore the SalePrice as it is the Target Feature

<p style="text-align:center;">
    <img width="400" alt="Final Top 10 Correlated Features" src="https://github.com/patty-olanterns/RealEstateAmesIA/blob/main/FinalFeature_vs_TargetCorrelationScore.png?raw=true">
    

# Results

For this project the **XGBoost model had the lowest RMSLE score (~0.119)** and was selected as the best prediction model.

The final XGBoost model was improved by adjusting model parameters
to get the lowest RMSLE score.
