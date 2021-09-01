# A Brief Description
This function is designed to automate the process of choosing an ARIMA model with the lowest AIC score. It's designed to be used on stock tickers from the `yfinance` module, but could easily be edited for other applications. It's mostly customizable. All there is to do is to insert your data, choose your start and end dates, and enter the list of p, d, and q values you'd like to "GridSearch" over. It will test all combinations of these three scores while continually updating the best model. Outside knowledge of the pitfalls of ARIMA models is reccommended since not all factors (such as seasonality) are accounted for here.

Once all models are tested, the resulting AIC score, along with MSE, RMSE, and R^2 score of both the training and testing data are displayed. Additionally, the results of the Augmented Dickey-Fuller test show whether the data is stationary or not. Autocorrelation is checked with ACF and PACF graphs. Lastly, the model forecasts and residuals are plotted out.

The example in the iPython notebook uses GOOG stock prices from 2015 through 2020.

This code produces several warnings due to issues with the use of datetime information in the index of the data, so I've included a chunk of javascript code that allows you to toggle them.
