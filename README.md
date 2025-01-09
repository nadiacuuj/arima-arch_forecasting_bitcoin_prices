# ARIMA-ARCH Bitcoin Price Forecasting

This project forecasts Bitcoin prices in USD using ARIMA for trend modeling and ARCH for volatility, leveraging daily data sourced from Kaggle.

## Overview
- **Objective:** Predict Bitcoin prices, incorporating volatility.
- **Dataset:** Bitcoin BTC-USD Stock Dataset on Kaggle

### Tools:
- ARIMA modeling in Minitab
- ARCH modeling in R

## Methodology
1. **Data Preparation:**
   - Log transformation and first-order differencing to achieve stationarity.
2. **ARIMA Model:**
   - Selected ARIMA(2,1,0) based on ACF/PACF analysis using Minitab.
3. **ARCH Model:**
   - Fitted ARCH(8) model in R to capture conditional heteroscedasticity in residuals.
4. **Forecasting:**
   - Generated 95% one-step ahead forecast intervals using the ARIMA-ARCH model.
  
## Results
- **ARIMA-GARCH vs ARIMA:** ARIMA-ARCH provides narrower, more precise forecast intervals.
- **Model Accuracy:** 5% forecast failures, consistent with a 95% prediction interval.

## Plot
Below is the plot of the historical Bitcoin prices along with the ARIMA-ARCH one-step ahead 95% forecast intervals.
