# Time Series Forecasting with XGBoost

This repository contains Python code for performing time series forecasting using the XGBoost algorithm. The code explores a dataset of hourly energy consumption and demonstrates various stages of time series forecasting, including data preprocessing, feature creation, model creation, and evaluation.

## Dataset

The dataset used in this project is "PJME_hourly.csv," and it was collected from the kaggle website: https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption?select=DOM_hourly.csv 
The dataset contains hourly energy consumption data. The goal is to forecast energy consumption based on time-related features.

## Stages of the Code

The code is organized into several stages:

### 1. Data Preprocessing

- The dataset is loaded, and the index is set to the 'Datetime' column.
- The 'Datetime' column is converted to a datetime data type for time-based analysis.

### 2. Data Exploration & Cleaning

- The dataset is examined for its structure and data types.
- A time series plot is generated to visualize energy consumption trends over time.

### 3. Train/Test Split

- The dataset is split into a training set (prior to January 2015) and a test set (from January 2015 onward).
- A plot visualizes the train/test split.

### 4. Feature Creation

- Time series features are created based on the time series index, including hour, day of the week, quarter, month, year, and day of the year.

### 5. Visualize Relationship Features/Target

- Box plots show the relationship between features (e.g., hour, month) and the energy consumption target, highlighting patterns and trends.

### 6. Model Creation

- The XGBoost model is created and trained using the training dataset with defined features.
- Hyperparameters, such as the number of estimators and learning rate, are specified.

### 7. Feature Importance

- Feature importance values are calculated, indicating how much each feature was used in the model.

### 8. Forecast on Test Set

- The trained model is used to make predictions on the test set.
- The test set predictions are merged with the original dataset.

### 9. Evaluation Metric

- The root mean squared error (RMSE) is calculated to evaluate the model's performance on the test set.

### 10. Calculate Error

- The model's errors are calculated, identifying the discrepancies between actual and predicted values.
- Days with the largest errors (both worst and best) are identified.

## Conclusion

This code demonstrates a complete workflow for time series forecasting using the XGBoost algorithm. It covers data preprocessing, feature creation, model creation, and evaluation. While the model provides insights into energy consumption trends, it may benefit from further parameter tuning and additional features, such as holidays and weather forecasts, to improve accuracy.

The RMSE score provides a measure of the model's predictive accuracy, and the code identifies days with the best and worst predictions.

Feel free to adapt and use this code for your own time series forecasting projects.

## Dependencies

The code relies on the following Python libraries:

- pandas
- numpy
- seaborn
- matplotlib
- xgboost
- scikit-learn

Ensure that these libraries are installed before running the code.

