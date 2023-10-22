# SMA Backtester

This Python code defines a `SMABacktester` class that can be used for backtesting a simple moving average (SMA) trading strategy using historical stock price data. The class is designed to be informative and easy to use for testing trading strategies.

## How to Use

1. Import necessary libraries at the beginning of your Python script:

   ```python
   import yfinance as yf
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt

Define an instance of the SMABacktester class with the following parameters:
symbol: The stock symbol for which you want to perform the SMA backtest.
SMA_S: The short-term Simple Moving Average period.
SMA_L: The long-term Simple Moving Average period.
start: The start date for historical data retrieval.
end: The end date for historical data retrieval.

Example:
backtester = SMABacktester("AAPL", 50, 200, "2020-01-01", "2021-12-31")

2.Use the following methods of the SMABacktester class:

get_data(): Downloads historical stock price data, calculates daily returns, and computes short-term and long-term SMAs. The data is stored in a Pandas DataFrame called data2.

test_results(): Backtests the trading strategy using historical data. It calculates the position (buy or sell) based on the relationship between the short-term and long-term SMAs. It also calculates the strategy returns and compares them to a buy and hold (B&H) strategy. The results are stored in the results DataFrame.

plot_results(): Visualizes the backtesting results by plotting the returns of the strategy and the buy and hold strategy in a single graph.

Example:
backtester = SMABacktester("AAPL", 50, 200, "2020-01-01", "2021-12-31")
backtester.get_data()
backtester.test_results()
backtester.plot_results()




You can save this content in a file named `README.md` in the root directory of your project to provide clear instructions on how to use the `SMABacktester` class for backtesting SMA trading strategies.
