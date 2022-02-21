# Ames, IA Real Estate Prices: Regression Model and Notebook

The purpose of this project is to predict the price of housing in the city of Ames, IA using real estate feature
data and different regression predictive models. 

Features such as Lot Size, Number of Bedrooms and the Age of the House are examples of factors to help predict the 
price of real estate in Ames, IA. Feature importance is also calculated and is used to determine the importance of each
Housing feature in the model's prediction.

The models selected for this project are Decision Tree Regression, Random Forest Regression and XGBoost Regression.
Each of these models come from the Sci-Kit Learn machine learning library.

Root Mean Squared Error (RMSE) is the method of evaluation that is used to determine error losses when a
regression model is run. The error is the difference between the predicted
real estate prices with the true real estate prices in each model.

From Wikipedia, RMSE is defined as the following:

The root-mean-square deviation (RMSD) or root-mean-square error (RMSE) is a frequently used measure of the differences between values (sample or population values) predicted by a model or an estimator and the values observed. The RMSD represents the square root of the second sample moment of the differences between predicted values and observed values or the quadratic mean of these differences. These deviations are called residuals when the calculations are performed over the data sample that was used for estimation and are called errors (or prediction errors) when computed out-of-sample. 

**The RMSD serves to aggregate the magnitudes of the errors in predictions for various data points into a single measure of predictive power. RMSD is a measure of accuracy, to compare forecasting errors of different models for a particular dataset and not between datasets, as it is scale-dependent.[1]**

RMSD is always non-negative, and a value of 0 (almost never achieved in practice) would indicate a perfect fit to the data. **In general, a lower RMSD is better than a higher one. However, comparisons across different types of data would be invalid because the measure is dependent on the scale of the numbers used. **

RMSD is the square root of the average of squared errors. The effect of each error on RMSD is proportional to the size of the squared error; thus larger errors have a disproportionately large effect on RMSD. Consequently, RMSD is sensitive to outliers.[2][3] 

## RMSLE

For this project, Root Mean Squared Log Error (RMSLE) will be used in place of RMSE for determining error losses for each model that is run.
- y_valid = True ground truth values
- y_pred = Predicted target values

## Feature Importance
Feature Importance is a method of determining attributes/features that are of importance in predicting the Target Variable (Housing Price)
in each Regression model. Top features for the XGBoost model are displayed in an interactive Plotly graph. 

The model with the lowest RMSLE score is selected for Real Estate value predictions.


## Project Process

The following is a Table of Contents for how the project is broken down:

**Import libraries**

**EDA (Exploratory Data Analysis)**
- Check number of features with missing values
- Check Correlation between SalePrice (Target Feature) and house Feature
- Average SalePrice visual
- Drop statistical outliers for TotalSquareFeet attribute (z-score > 3)

**Preprocessing**
- Features and target feature selection
- Train Test Split
- Numeric/Category Pipeline 
  - Define numerical and categorical columns in training data
  - Replace null numeric values with SimpleImputer()
  - Replace null categorical values (string, object, bool) with most frequent values by column
  - Encode each categorical value as unique category using OneHotEncoder()
  - Setup preprocessor ColumnTransformer Pipeline with numeric and category transformers as steps
    in process
    
**Define Root Mean Squared Log Error function (RMSLE)**
- Calculate RMSE of log(y_test) and log(y_pred) 
- y_test = test features
- y_pred = predicted features

**Model Selection**
- Test Decision Tree
  - Preprocessing Pipeline -> Decision Tree Regression Model -> Fit train-test data
- Test Random Forest
  - Preprocessing Pipeline -> Random Forest Regression Model -> Fit train-test data
- Test XGBoost
  - Preprocessing Pipeline -> XGBoost Regression Model -> Fit train-test data

- Determine Feature Importance score for XGBoost Model

- Display predicted values (RMSLE) in XGBoost mode

- Compare predicted model values (RMSLE)

- Select model

- Run GridSearchCV (CrossValidation) to select best parameters
  for use in final model
  
- Run high performance (hp) model

- Select Features for use in final model
- Repeat preprocessing pipeline steps then run model
- Print the final RMSLE results of the model

