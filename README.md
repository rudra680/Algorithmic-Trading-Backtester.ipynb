# Algorithmic-Trading-Backtester.ipynb
# Algorithmic Trading Backtester: NSE Equities

## Overview
A Python-based quantitative backtesting engine designed to evaluate the performance of momentum-based trading strategies on Indian equities (NSE). This project processes 5 years of historical market data to test signal generation, execute simulated trades, and compare portfolio performance against a standard buy-and-hold benchmark.

## Tech Stack
* **Language:** Python
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib
* **Data Extraction:** yfinance API

## Methodology & Models
The backtester evaluates two distinct trend-following models to demonstrate the impact of volume confirmation on reducing false trade executions.

**1. Baseline Model (Pure Price Action)**
* Implemented a standard Moving Average Crossover system.
* **Buy Signal:** 50-day Simple Moving Average (SMA) crosses above the 200-day SMA (Golden Cross).
* **Sell Signal:** 50-day SMA crosses below the 200-day SMA (Death Cross).

**2. Upgraded Model (Volume Confirmation)**
* Identified false breakouts (whipsawing) in the baseline model during sideways markets. 
* Engineered a secondary filter requiring daily trading volume to strictly exceed the 20-day volume SMA to confirm the price momentum before executing a buy signal.

## Results
* **Buy & Hold Benchmark:** Return of 26%
* **Baseline Strategy Return:** Return of 0.07%
* **Volume-Confirmed Strategy Return:** Return of 28%
* **Conclusion:** The addition of the volume-confirmation filter successfully filtered out low-conviction breakouts, improving the overall alpha of the algorithmic strategy.

## About the Author
I am a second-year undergraduate student at IIT Bombay studying Civil Engineering, actively expanding my skill set in data science and quantitative analysis. I am highly interested in the intersection of finance and technology.

