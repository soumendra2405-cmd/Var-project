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

This project implements Portfolio Value at Risk (VaR) using the Variance-Covariance (Parametric) approach in Python. It analyzes a multi-asset portfolio and estimates potential losses over a 5-day horizon using statistical modeling and historical market data.

The model downloads 15 years of historical price data for SPY, AAPL, TSLA, AMZN, and MSFT using yfinance. Log returns are computed and used to construct an equally weighted portfolio with a total value of $1,000,000. The covariance matrix of asset returns is annualized (multiplied by 252 trading days), and portfolio volatility is calculated using the formula:

σₚ = √(wᵀ Σ w)

where w represents portfolio weights and Σ is the covariance matrix.

The 5-day VaR is then computed at 90%, 95%, and 99% confidence levels using the parametric formula:

VaR = Portfolio Value × [ Z × σₚ × √(T/252) − μ × T ]

where Z is the standard normal quantile, σₚ is portfolio volatility, μ is the average portfolio return, and T is the time horizon in days.

The script also generates a histogram of 5-day portfolio returns scaled to portfolio value and overlays VaR cutoff lines, providing a clear visualization of downside risk exposure.

This project demonstrates practical implementation of risk modeling concepts including log return calculation, covariance estimation, portfolio volatility computation, and parametric risk measurement. It highlights how statistical assumptions (such as normally distributed returns) influence risk estimates

# VaR on Excel

# Excel Implementation – Historical & Monte Carlo VaR
This project also includes an Excel-based implementation of Value at Risk modeling.

The Excel model includes:

Historical VaR using empirical return distribution
Monte Carlo simulation to generate stochastic return paths
95% and 99% confidence level risk estimation
Portfolio loss calculation in monetary terms
Statistical summary (mean, standard deviation, min, max returns)
The Excel version demonstrates practical financial risk modeling without external programming libraries and highlights simulation-based risk estimation techniques.
