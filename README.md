# n-Asset-Sharpe-Ratio-Opimization
# Methodology
This script performs portfolio optimization using the Modern Portfolio Theory (MPT) approach and calculates the Value at Risk (VaR) for the optimized portfolio. 
# Assumptions
The risk-free rate is obtained from the FRED API (Federal Funds Rate).
Optimization is performed using the scipy.optimize minimize function with the SLSQP method.
The initial weights are assumed to be equally distributed among the assets.
Portfolio size is assumed to be 1 for VaR calculations.
Expected returns are assumed to be mean historical returns.
# Data Collection:
Historical adjusted close prices are fetched for the specified asset tickers using Yahoo Finance API.
Log returns and covariance matrix are calculated based on the historical data.
# Portfolio Optimization:
The script optimizes the portfolio by maximizing the Sharpe Ratio.
Constraints are set to ensure that the sum of portfolio weights equals 1.
Bounds are defined to restrict the weights between 0 and 1.
Value at Risk (VaR) Calculation:
VaR is calculated at a specified confidence level (default is 95%) for a given number of days (default is 1 day).
# Visualization:
The script visualizes the optimal portfolio weights as a pie chart.
It also plots the distribution of portfolio returns along with the VaR and mean return.
# Required Info
API Key: Ensure you have a valid API key for the FRED API.
Asset Tickers: Provide asset tickers separated by commas when prompted.
