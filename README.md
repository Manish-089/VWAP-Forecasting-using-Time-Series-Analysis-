Nifty 50 Stock Market Data Analysis and Forecasting
This project explores and forecasts the stock market data for ICICI bank from the Nifty-50 index over the last 20 years (2000-2019).

Dataset
The dataset includes historical stock data for ICICI bank, including features such as:

Symbol: Stock symbol (ICICIBANK)
Series: Equity series (EQ)
Prev Close: Previous day's closing price
Open, High, Low, Last, Close: Daily opening, highest, lowest, last, and closing prices
VWAP: Volume Weighted Average Price (Target Variable)
Volume: Daily trading volume
Turnover: Measure of stock liquidity
Trades: Total number of trades
Deliverable Volume: Quantity of shares delivered
%Deliverble: Deliverable volume percentage
Analysis and Findings
The analysis involved:

Data Exploration: Examining missing values, trends, seasonality, and correlations.
Missing Value Handling: Dropping rows with missing 'Deliverable Volume' and imputing 'Trades' with the mean.
Visualization: Plotting trends in Turnover, Volume, High/Low prices, and VWAP.
Time Series Analysis:
Applying Box-Cox transformation to the VWAP series.
Using moving average smoothing.
Analyzing Autocorrelation and Partial Autocorrelation plots.
Performing Augmented Dickey-Fuller test for stationarity.
Decomposing the time series into trend, seasonality, and residual components.
Feature Engineering: Creating lag features (mean and standard deviation) for 'High', 'Low', 'Volume', 'Turnover', and 'Trades' over different window sizes (3, 7, and 30 days). Adding 'month' and 'day' as features.
Model Building and Evaluation:
AutoReg Model: Built an AutoReg model with exogenous features and evaluated its performance using RMSE.
ARIMA Model: Used auto_arima to find the best ARIMA model with exogenous features and evaluated its performance using RMSE and MAE.
Deep Learning Models (LSTM and SimpleRNN): Trained and evaluated LSTM and SimpleRNN models on the scaled data. Compared their performance based on RMSE, MAE, and loss plots.
Results
The AutoReg model showed a good RMSE score.
The ARIMA model with exogenous features also provided fair RMSE and MAE scores.
The LSTM model outperformed the SimpleRNN model in terms of MAE, suggesting its ability to capture long-term dependencies in the data more effectively.
Conclusion
The analysis provides insights into the ICICI bank stock data and demonstrates the application of various time series forecasting techniques. The LSTM model appears to be the most promising among the evaluated models for forecasting VWAP in this dataset.
