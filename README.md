**Stock Market Analysis Project**

**Introduction:**

This project analyzes the behavior of major tech stocks — Apple (AAPL), Google (GOOG), Microsoft (MSFT), and Amazon (AMZN) — over the past year. Through a series of statistical techniques and visualizations, it answers critical investment-related questions and applies a Monte Carlo simulation to model future price behavior and Value at Risk (VaR).

**Data Source:**

•	Library Used: yfinance

•	Ticker Symbols: AAPL, GOOG, MSFT, AMZN

•	Time Period: Last 1 year from current date

•	Data Includes: Open, High, Low, Close, Adj Close, Volume

**Key Questions Explored:**

1.	What was the change in price of the stocks over time?

2.	What was the average daily return of each stock?

3.	What were the moving averages (10, 20, 50 days)?

4.	What was the correlation between different stocks’ closing prices?

5.	How did the daily returns of the stocks correlate?

6.	How much value is at risk (VaR) when investing in a specific stock?

7.	Can we predict future stock behavior using simulation techniques?

**Tools & Libraries:**

•	Python: pandas, numpy, scipy, datetime

•	Visualization: matplotlib, seaborn

•	Financial Data: yfinance, pandas_datareader

•	Simulation: Monte Carlo method

**Exploratory Data Analysis:**

1. Price Trends

    •	Line plots of stock closing prices and volumes

    •	Scatter plots and histograms of open vs close prices for AAPL

    •	Rolling averages for AAPL over 10, 20, and 50 days

2. Daily Returns

    •	Calculated percentage change in closing prices (pct_change())

    •	Jointplots to visualize relationships and correlations

    •	Pearson correlation coefficient to quantify strength between stocks

3. Correlation Analysis

    •	Pairplots and PairGrids to show daily return relationships

    •	Heatmaps for both daily returns and closing price correlations

**Risk & Return:**

•	Scatter plot of expected return vs. risk (standard deviation)

•	Annotated chart highlighting each stock’s relative risk

**Value at Risk (VaR)**

•	Applied 99% confidence VaR using quantile method

•	Interpretation: $X at risk per unit of investment in 99% of cases

rets['AAPL'].quantile(0.05)  # 5% quantile method for VaR

**Monte Carlo Simulation:**

•	Simulated 100+ possible stock price paths for GOOG over 1 year

•	Ran 10,000 simulations to generate end-of-year price distribution

•	Calculated final price metrics:

    •	Mean final price
    
    •	1st percentile (worst-case)
    
    •	Value at Risk (VaR)

**Final Output Example:**

Start Price: $176.47  
Mean Final Price: $183.23  
VaR(0.99): $7.91

This means there's only a 1% chance of losing more than $7.91 on a single share of GOOG over 365 days, based on the simulation.

**Appendix:**

•	Monte Carlo simulation defined with drift and shock

•	All visualizations plotted inline using Jupyter Notebooks

•	Notebook sections include:

    •	Stock Download & Inspection
    
    •	Price & Volume Trends
    
    •	Rolling Averages
    
    •	Correlation Visualizations
    
    •	Risk Analysis & VaR
    
    •	Forecasting via Simulation

**Conclusion:**

This project provides a comprehensive look at the risk-return tradeoff, correlation behavior, and volatility of top tech stocks. Using Monte Carlo methods and statistical tools, it empowers investors to make data-driven decisions and assess their risk appetite.
