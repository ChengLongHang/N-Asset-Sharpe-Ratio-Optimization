# N-Asset-Sharpe-Ratio-Optimization
# Methodology
This script performs portfolio optimization using the Modern Portfolio Theory (MPT) approach and calculates the Value at Risk (VaR) for the optimized portfolio. <br />
- The script optimizes the portfolio by maximizing the Sharpe Ratio (minimizing -ve Sharpe Ratio).<br />
- Constraints are set to ensure that the sum of portfolio weights equals 1.<br />
- Bounds are defined to restrict the weights between 0 and 1.<br />
- VaR is calculated at a specified confidence level (default is 95%) for a given number of days (default is 1 day, change according to your intended holding period).<br />
- Applied portfolio allocation strategy backtest over the period 2023-10-25 to 2024-10-25 with quarterly rebalancing, achieving a 49.07% return with volatility of  0.0868. <br />
![cumreturns](https://github.com/user-attachments/assets/0ba3c90f-06b1-4dd8-93a0-d2ad89c1ab23)
![weightings over time](https://github.com/user-attachments/assets/b77a38b1-5a3a-4da5-a6aa-e266165070dc)

# Assumptions
- The risk-free rate is obtained from the FRED API (Federal Funds Rate).
- Optimization is performed using the scipy.optimize minimize function with the SLSQP method.<br />
- Portfolio size is assumed to be 1 for VaR calculations.<br />
- Expected returns are assumed to be mean historical returns.<br />
# Data Collection:
Historical adjusted close prices are fetched for the specified asset tickers using Yahoo Finance API. Log returns and covariance matrix are calculated based on the historical data.<br />
# Visualization:
The script visualizes the optimal portfolio weights as a pie chart and also plots the distribution of portfolio returns along with the VaR and mean return.
![optweightings](https://github.com/user-attachments/assets/c8a744cd-63a7-4ec5-bb3c-d054afdf998f)
![VaR](https://github.com/user-attachments/assets/7b399b89-bbc5-4c8f-8f60-2f3a87c58b0d)

# Required Info
API Key: Ensure you have a valid API key for the FRED API.<br />
Asset Tickers: Provide asset tickers separated by commas when prompted.<br />
