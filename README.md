# Revenue Forecasting using ARIMA, SARIMA & SARIMAX

## Overview
This project develops a time series forecasting pipeline to predict daily revenue using ARIMA-based models. It compares ARIMA, SARIMA (with weekly seasonality), and SARIMAX (with external variables) to improve forecast accuracy.

## Key Features
- Data cleaning and preprocessing
- Stationarity testing (ADF test) and differencing
- Seasonal decomposition (trend, seasonal, residual)
- ACF & PACF analysis
- ARIMA, SARIMA, and SARIMAX modeling
- Rolling time-series cross-validation
- Hyperparameter tuning (grid search)
- Future forecasting with exogenous variables
- Evaluation using MAE, RMSE, and MAPE

## Workflow
1. Load and clean daily revenue dataset
2. Perform exploratory time series analysis
3. Test and enforce stationarity
4. Train ARIMA → SARIMA → SARIMAX models
5. Validate using forward-chaining cross-validation
6. Tune hyperparameters to minimize RMSE
7. Refit best model and forecast future revenue

## Dataset Requirements

### daily_revenue.csv
- Date column as index
- revenue column (string with commas)
- discount_rate and coupon_rate columns (percentages)

### future_regressors.csv
- Future discount_rate and coupon_rate values
- Date index continuing historical timeline

## Technologies
- Python
- Pandas
- NumPy
- Statsmodels (SARIMAX)
- Scikit-learn
- Matplotlib

## Output
- Forecast comparison plots
- Cross-validation metrics
- Best SARIMAX parameters
- Future revenue predictions
