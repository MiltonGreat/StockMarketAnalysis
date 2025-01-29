# S&P Composite Stock Market Analysis (1880-2024)

### Overview

This project analyzes the S&P Composite stock market data from 1871 to 2024. The primary focus is on:

1. Time Series Analysis – Decomposing stock market data to identify trends, seasonality, and anomalies.
2. Cluster Analysis – Identifying distinct stock market behavior patterns and anomalies.
3. Forecasting – Predicting future stock returns using various statistical and machine learning models.

### Dataset

The dataset consists of monthly stock price, dividends, earnings, interest rates, and the consumer price index (CPI). This allows for the conversion of stock prices to real values and long-term financial trend analysis.

#### Columns in the Dataset:
- Date – Timestamp of the record
- SP500 – S&P Composite Index
- Dividend – Monthly dividends paid
- Earnings – Reported earnings per share
- Consumer Price Index – Inflation measure
- Long Interest Rate – 10-year government bond yield
- Real Price – Inflation-adjusted stock price
- Real Dividend – Inflation-adjusted dividends
- Real Earnings – Inflation-adjusted earnings
- PE10 – 10-year cyclically adjusted price-to-earnings ratio

### Key Features of the Project

1. Data Cleaning & Preprocessing
- Converted the Date column to datetime format.
- Forward-filled and backward-filled missing values.
- Removed duplicate records and columns with all NaN values.

2. Time Series Decomposition
Used seasonal decomposition (seasonal_decompose) to break down the S&P 500 data into:
- Trend – Long-term movement
- Seasonal – Repetitive patterns
- Residual – Random fluctuations

3. Cluster Analysis for Anomalies

Applied K-Means clustering to segment the stock market into different phases.

Features used for clustering:
- Real Price
- Real Dividend
- PE10

4. Anomaly Detection
- Used Isolation Forest to detect anomalies in stock prices.

5. Stock Market Forecasting
- Applied Exponential Smoothing to predict future stock prices.

## Results

![screenshot-localhost_8888-2025 01 29-09_26_54](https://github.com/user-attachments/assets/f7da6930-0fef-440b-ba3d-aedfa3be1ed5)

- The decomposition revealed significant cyclical behavior in the stock market.
- Several sharp declines correspond to known financial crises.
- The clustering analysis identified at least 3 distinct market phases, each representing different stock market conditions (e.g., bull and bear markets).
- Silhouette Score: 0.37 (indicating moderate cluster separation).
- Key anomalies were detected in 1929 (Great Depression), 2008 (Financial Crisis), and recent market fluctuations (2020-2023). These anomalies align with significant economic events.
- Forecasted Values for Next 12 Months: Predicted S&P 500 values showed an upward trend but with uncertainty.
- Mean Absolute Error (MAE): 0.0324
- Root Mean Squared Error (RMSE): 0.0506
- R² Score: 0.0345 (indicating a weak predictive model)

## Key Takeaways

- Time series analysis confirmed historical market trends and volatility.
- Cluster analysis identified distinct stock market phases and anomalies.
- Anomaly detection aligned with historical economic downturns.
- Forecasting models had high error rates and need improvement.
- The forecasting model was unable to accurately predict future stock price anomalies.
- Alternative models such as ARIMA or LSTMs may provide better results.
  
## Future Work

- Improve Predictive Models: Feature engineering might enhance forecasting accuracy.
- Exploring LSTM-based deep learning models could improve time series predictions.
- Compare Global Markets: Compare S&P Composite trends with European, Asian, and emerging markets.
- Refine Clustering Analysis: Test alternative clustering methods like DBSCAN for better anomaly detection.

## Source

Nobel laureate Robert Shiller has made available a dataset that includes long-term U.S. stock market data. This dataset includes the S&P 500 index, dividends, and interest rates.

The data is freely available on Robert Shiller’s website and is often used in academic research. You can access it here: https://shillerdata.com/
