# Portfolio-Optimizer

This project implements a portfolio optimization mwthod based on Mean-Variance Optimization. The objective is to construct an optimal asset allocation that maximizes risk-adjusted returns using historical market data.

The model estimates expected returns and risk, then applies numerical optimization to identify the portfolio with the highest Sharpe ratio.



## Objective
- Maximize Sharpe Ratio  
- Analyze risk vs return tradeoff  
- Identify optimal portfolio weights  


## Methodology

### Data Collection
- Historical price data fetched using yfinance library
- Daily adjusted closing prices used for analysis  

### Return & Risk Estimation
- Daily returns computed using percentage change  
- Mean returns vector calculated  
- Covariance matrix used to estimate portfolio risk  

### Optimization
- Objective Function: Maximize Sharpe Ratio  
- Optimization Method: Sequential Least Squares Programming (SLSQP)  
- Constraints:
  - Sum of weights = 1  
  - No short selling (weights bounded between 0 and 1)
  - Minimum Weight = 0.05

### Portfolio Metrics
- Expected Return  
- Volatility (Standard Deviation)  
- Sharpe Ratio  



## Results

The model produces:
- Optimal portfolio weights  
- Expected portfolio return  
- Portfolio volatility  
- Maximum Sharpe ratio  



## Visualization

- Efficient Frontier (Monte Carlo simulation)  
- Risk vs Return scatter plot  
- Sharpe ratio distribution across portfolios  


## Tech Stack

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- SciPy  
- yfinance  



## Limitations

- Assumes normally distributed returns   
- No transaction costs or slippage considered  
- Static allocation  
