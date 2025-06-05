# singneer_backtesting

# FX Mean-Reversion Strategy Backtester

## Project Overview
This project implements a backtesting engine for a **mean-reversion FX trading strategy** using SGD cross-rates. The approach relies on linear regression to predict a target currency’s price based on a basket of other SGD pairs. A residual (spread) is calculated and tested for mean-reversion using the Augmented Dickey-Fuller (ADF) test.

## Key Features
- **Data Sourcing**: Retrieves historical FX data using Yahoo Finance and MAS NEER index data.
- **Modeling**: Trains an OLS regression model to predict the target currency based on a basket of tickers.
- **Signal Generation**: Computes the spread, optimizes buy/sell thresholds using Sharpe ratio, and generates trading signals.
- **Statistical Testing**: Applies ADF test to ensure the spread is mean-reverting.
- **Performance Evaluation**: Visualizes returns, position histories, and calculates Sharpe ratio.
- **Suggested Improvements**: Includes ideas for enhancing robustness such as prediction smoothing, outlier filtering, and adaptive sizing.

## Getting Started

### Installation
Make sure you have Python 3.x installed. Then install the required packages:

```bash
pip install pandas matplotlib yfinance statsmodels scikit-learn
