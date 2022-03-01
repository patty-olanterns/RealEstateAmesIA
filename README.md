# Ames, IA Real Estate Prices: Regression Model and Notebook

The purpose of this project is to predict the price of housing in the city of Ames, IA using real estate feature
data and different regression models. The model with the lowest error score is selected for Real Estate value predictions.

Features such as Lot Size, Number of Bedrooms and the Age of the House are examples of factors to help predict the 
price of real estate in Ames, IA. Feature importance is also calculated and is used to determine the importance of each
Housing feature in the model's prediction.

The models selected for this project are Decision Tree Regression, Random Forest Regression and XGBoost Regression.
Each of these models come from the Sci-Kit Learn machine learning library.

**Root Mean Squared Error (RMSE)** is the method of evaluation that is used to determine error losses when a
regression model is run. The error is the difference between the predicted
real estate prices with the true real estate prices in each model.

A link to its entire definition is provided [here] (#https://en.wikipedia.org/wiki/Root-mean-square_deviation)

For this project, **Root Mean Squared Log Error (RMSLE)** will be used in place of RMSE for determining error losses for each model that is run.

**The model with the lowest RMSLE is selected as it has the lowest error between Actual and Predicted Real Estate Price values!**

# Results

For this project the **XGBoost model had the lowest RMSLE score (~0.139)** and was selected as the best Prediction Model!

The XGBoost model was further improved by adjusting the model parameters and determining which
attributes of a house (Square Footage, Number of Garages etc.) were most important in the model. 
These attributes are known as **Feature Importance.**

## Feature Importance
Feature Importance is a method of determining attributes/features that are of importance in predicting the Target Variable (Housing Price)
in each Regression model. Top features for the XGBoost model are displayed in an interactive Plotly graph. 
