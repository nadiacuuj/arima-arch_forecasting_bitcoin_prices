# ARIMA-ARCH Bitcoin Price Forecasting

This project applies ARIMA-ARCH models to forecast Bitcoin prices in USD using daily data. The dataset is sourced from Kaggle, containing 2836 observations, which are used to predict Bitcoin’s adjusted closing prices. The forecast model is evaluated using one-step ahead predictions, with a focus on capturing volatility through the ARCH model.

## Project Overview
**Objective:** The goal is to predict Bitcoin prices while accounting for volatility using ARIMA for trend modeling and ARCH for capturing heteroscedasticity.

## Data Source:
- **Dataset:** Bitcoin BTC-USD Stock Dataset on Kaggle
- Key Variables:** Date and Adjusted Close Price
 #### Key Steps:
- **Data Preprocessing:** Log transformation and differencing to make the data stationary.
- **ARIMA Model:** Initial fitting of the ARIMA(2,1,0) model based on ACF/PACF analysis.
- **ARCH Model:** Fitting of an ARCH(8) model to capture volatility in the residuals.
- **Forecasting:** Using the ARIMA-ARCH model to forecast Bitcoin prices with a 95% confidence interval.

## Key Methodology
1. Data Preparation
Stationarity Check: The raw data is non-stationary. Log transformation and differencing are used to stabilize the variance.
ARIMA Model: The ARIMA(2,1,0) model was selected based on ACF and PACF plots.
2. Model Fitting
ARIMA Model: The ARIMA(2,1,0) model fits the differenced, log-transformed Bitcoin data, and residuals are checked for randomness and autocorrelation.
ARCH Model: The ARCH(8) model is selected based on AICc criteria, capturing conditional heteroscedasticity in the residuals.
3. Forecasting and Evaluation
Forecasting: The ARIMA-ARCH model generates one-step ahead predictions with narrower confidence intervals, improving precision during volatile periods.
Error Analysis: A normal probability plot of residuals shows deviations from normality, indicating leptokurtosis. The model’s failure rate is about 5%, consistent with the expected behavior for 95% prediction intervals.

## Results
- **ARIMA-GARCH vs ARIMA:** The ARIMA-GARCH model produces more precise predictions, with narrower forecast intervals.
- **Volatility and Prediction:** The model effectively captures periods of heightened volatility but may overfit to specific periods, limiting its ability to generalize.

## Model Evaluation
- **Failures:** 159 instances where the 95% forecast interval did not contain the actual value, resulting in a failure rate of approximately 5%.

## Conclusion
This model provides a robust framework for forecasting Bitcoin prices while accounting for volatility. However, further improvements may be made by exploring alternative models such as GARCH or adjusting for non-normal error distributions.
