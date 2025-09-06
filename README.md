
# Engulfing Candle Trading Bot

A Python-based trading bot that uses Alpaca’s brokerage API to analyze candlestick data and place **bracket orders** (with take-profit and stop-loss) automatically based on a custom candlestick strategy.

---

##  Features

-  Analyzes historical OHLC candles
-  Entry logic based on recent candle patterns
-  Automatically calculates Take Profit & Stop Loss based on configurable PnL ratio
-  Uses Alpaca paper trading account for testing
-  Can be run in a loop for continuous trading

---

## Strategy Logic

- Looks at the last 3 candles and identifies bullish or bearish setups
- Places a **market order** with a **bracket (TP/SL)** if a signal is found
- TP and SL levels are calculated using the body of the previous candle and a fixed PnL ratio

> Default PnL ratio: 1:2 (reward:risk)

---

## ⚙️ Requirements

- Python 3.8+
- Pandas
- Alpaca Account
- Alpaca paper trading API key & secret
