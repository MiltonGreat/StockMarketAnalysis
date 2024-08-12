# S&P Composite Stock Market Analysis (1880-2024)

## Overview

This project analyzes the S&P Composite stock market data from 1880 to 2024. The primary focus is on cluster analysis and time series analysis to uncover patterns and trends in the data.

## Columns

This data set consists of monthly stock price, dividends, and earnings data and interest rates and the consumer price index (to allow conversion to real values), starting January 1871. The columns included in this data set are as follows:

- Date
- S&P Comp.
- Dividend
- Earnings
- CPI
- Long Interest Rate GS10
- Real Price
- Real Dividend
- Real Total Return Price
- Real Earnings
- Real TR Scaled Earnings
- CAPE
- TR CAPE
- Excess CAPE Yield
- Monthly Total Bond Returns
- Real Total Bond Returns
- 10 Year Annualized Stock Real Return
- 10 Year Annualized Bond Real Return
- Real 10 Year Annualized Return

## Contents

- Data Preprocessing: Steps taken to clean and prepare the data for analysis.
- Exploratory Data Analysis (EDA): Initial exploration of the data to understand its structure and key characteristics.
- Cluster Analysis: Application of clustering techniques (e.g., K-Means, DBSCAN) to identify distinct groups within the data.
- Time Series Analysis: Analysis of the temporal aspects of the stock market data to identify trends, seasonality, and other time-related patterns.
- Results and Visualizations: Presentation of the results with corresponding visualizations.

## Results

- Cluster Analysis: The data was successfully segmented into 3 (up to 5) meaningful clusters, revealing distinct patterns in the stock market data.
- Time Series Analysis: The time series analysis highlighted key trends and seasonal patterns in the S&P Composite over the analyzed period.

## Key Takeaways

- The cluster analysis shows there are a mininum of 3 (up to 5) clusters (also called: anomalies) to have happened from 1880 to 2024. 
- The time series analysis shows at least 3 (up to 5) large drops in the stock market over the years.
- I was unsuccessful in predicting future anomalies (all the models used had high MSE and MAE).
- I was curious if I could predict future anomalies (stock market crashes) going to 2100, which does offer a valuable insight.
  
## Future Work

- Expand Analysis: Further analysis using additional financial indicators or a more granular time series analysis might work better.
- Predictive Modeling: The predictive model to forecast future stock market trends did not work. Perhaps feature engineering might improve the performance, as I expect it should.
- Comparison with Other Markets: I should compare the S&P Composite with other global markets, which may help with recognizing how their differences.

## Contributing

Nobel laureate Robert Shiller has made available a dataset that includes long-term U.S. stock market data, going back to the 1870s. This data includes the S&P 500 index, dividends, and interest rates, which are useful for analyzing long-term market trends.

The data is freely available on Robert Shiller’s website and is often used in academic research. You can access it here: https://shillerdata.com/
