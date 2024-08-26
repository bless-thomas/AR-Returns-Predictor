# AR-Returns-Model

The “AR-Returns-Predictor” project aims to create a model to predict stock returns using an autoregressive (AR) model. We follow a step-by-step process, starting from data collection to model evaluation. Below, I’ll outline the key steps and provide an explanation for each:

## Data Collection and Preprocessing:
- We fetch historical stock data using the yfinance library.
- Calculate log returns from the stock prices to ensure stationarity.

## Stationarity Check:
- Verify that the log returns are stationary using statistical tests (e.g., Augmented Dickey-Fuller test).
- Stationarity is crucial for time series modeling.

## Autocorrelation Analysis:
- Examine the partial autocorrelation function (PACF) and autocorrelation function (ACF) plots.
- Determine the optimal lag (in this case, lag didn't show high correlation hence took lag 1) based on correlation patterns.

## Model Building and Evaluation:
- Split the data into a training set (70%) and a testing set (30%).
- Fit an autoregressive model (AR(1)) using the training data.
- Model showed no significane of lag 1 in predicting the stock returns.
- Predicting and plotting the values on the testing set of the data.

## Residual Analysis:
- Check for endogeneity by examining the correlation between residuals and lagged variables.
- If no significant correlation exists, the model assumptions are met.

## Conclusion
The “AR-Returns-Predictor” project demonstrates how to build an AR model for stock return prediction. While lag 1 might not be significant individually, adding other factors may compensate for its lack of significance.
