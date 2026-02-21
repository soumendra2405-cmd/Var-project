# Var on Python
# Historical Value at Risk (VaR) – Multi-Asset Portfolio
Overview
This project implements the Historical Simulation method to estimate the 5-day Value at Risk (VaR) of an equally weighted portfolio using 15 years of real market data.
The objective is to measure potential downside risk at a 95% confidence level without assuming any specific probability distribution.

The portfolio consists of the following ETFs:
SPY – S&P 500 ETF
BND – Total Bond Market ETF
GLD – Gold ETF
QQQ – NASDAQ 100 ETF
VTI – Total Stock Market ETF

Approach
The model follows these steps:
Download 15 years of historical daily price data using yfinance
Calculate daily logarithmic returns
Construct an equally weighted portfolio
Compute rolling 5-day cumulative portfolio returns
Estimate Historical VaR using the percentile method
Convert VaR into dollar terms based on a $100,000 portfolio
Visualize the return distribution and VaR cutoff
The Historical VaR is calculated as the 5th percentile of the rolling 5-day portfolio returns and represents the maximum expected loss over 5 days with 95% confidence.

Model Assumptions
15-year historical data window
5-day holding period
95% confidence level
Equal portfolio weights
Log returns
Non-parametric (no distributional assumptions)

Libraries Used
Python
NumPy
Pandas
Matplotlib
SciPy
yfinance

Output
The script produces:
5-day Historical VaR (95% confidence) in dollar terms
Distribution plot of rolling 5-day portfolio returns
Visualization of the VaR threshold

# Portfolio Value at Risk (VaR) – Variance-Covariance Method
Portfolio Value at Risk (VaR) – Variance-Covariance Method

This project calculates Portfolio Value at Risk (VaR) using the parametric (variance-covariance) approach in Python. It analyzes a 5-asset portfolio (SPY, AAPL, TSLA, AMZN, MSFT) using 15 years of historical data.

The model computes log returns, estimates portfolio volatility using the covariance matrix, and calculates 5-day VaR at 90%, 95%, and 99% confidence levels. A histogram of portfolio returns is generated with VaR thresholds to visualize downside risk.

This project demonstrates practical implementation of portfolio risk measurement, volatility estimation, and statistical risk modeling using Python
