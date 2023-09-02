# Car_price_prediction
EDA project with boosting modeling from Practicum by Yandex
## Numerical Methods project from Practicum by Yandex
### Goal
Develop a model for Rusty Bargain used car sales service to determine the market value of a car based on historical data (technical specifications, trim versions, and prices).

**Key metrics:**

* the quality of the prediction
* the speed of the prediction
* the time required for training
  
This project's repo includes the project's jupyter notebook (Car_price_prediction_using_gradient_boosting.ipynb)

**We have completed the following steps in this project:**
* Descriptive statistics. We found missing values, wrong features format, 6 categorical features, possible ouliers in several variables.
* Data preprocessing. We have converted column names to lower case, changed data type, filled in missing values and removed duplicates.
* EDA. We have checked for outliers 5 variables, created a new featured (car_age) and dropped non-informative columns.
* Encoding of categorical variables. All categorical variables were one-hot encoded for linear models and ordinal ebcoded for forest-model.
* Splitting data into train, validation and test sets. Data was split into 3 sets to perform best model selection.
* Standard scaling
* Model selection. We have compared Linear Regression, Random Forest, XGBoost, LightGBM and CatBoost models. We have also tuned a few hyperparameters for these algorithms. We have chosen the tuned CatBoost model based on RMSE score and training and prediction speed.
* Retrain the best tuned model. The best model was retrained on the whole training data set in order to increase the volume of data it can learn from. The test score has slightly improved thanks to this step.
* Sanity check. The test score of the Linear regression model, that we use as a baseline to analyze the model quality, is 43.54% higher than our final chosen model. It means that the modeling was useful.
  
### Results
The CatBoost model with the tuned hyperparameters has shown the best results (test RMSE of 1575, time of training 318 seconds, time of prediction 0.79 seconds) in terms of both quality and speed of training and prediction.
