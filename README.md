
# 📊 Pairs Trading Strategy using Cointegration & Rolling Z-Score

This project implements a **statistically-driven pairs trading strategy** using Python, real historical stock data, and time series analysis techniques.

> 🧠 Built by [Keshav Khandelwal](https://github.com/keshav-kh), this notebook simulates a quantitative trading approach used by hedge funds and prop shops — with a focus on statistical rigor and backtest reliability.

---

## 📌 Project Overview

**Pairs trading** is a market-neutral strategy that takes advantage of the mean-reverting relationship between two historically correlated assets. This notebook performs:

- ✅ **Rolling z-score analysis** to identify divergences in asset price spreads  
- ✅ **Cointegration testing (Engle-Granger)** to filter for statistically meaningful pairs  
- ✅ **Backtesting logic** to simulate entry/exit, calculate PnL, and evaluate strategy performance  
- ✅ **Sharpe ratio ranking** to measure reward vs. risk per pair  
- ✅ **Real equity pair analysis** (e.g., KO/PEP, MSFT/AAPL, WMT/TGT)

---

## 📈 Methodology

### 1. **Data Collection**
- Historical price data from Yahoo Finance (`yfinance`)
- Time range: 2018–2023
- Assets analyzed: `KO`, `PEP`, `MSFT`, `AAPL`, `WMT`, `TGT`

### 2. **Cointegration Filtering**
- Uses **Engle-Granger test** to detect long-term equilibrium between asset pairs
- Only statistically significant pairs (`p-value < 0.15`) are backtested

### 3. **Backtest Logic**
- Enter trades when z-score > ±1.0
- Exit trades when z-score reverts toward 0.5
- Simple transaction cost model
- Tracks trade count, profit/loss, and strategy health

### 4. **Performance Evaluation**
- **Total PnL**
- **Number of Trades**
- **Sharpe Ratio**: risk-adjusted performance metric

---

## 📊 Sample Output

```text
Top Performing Pairs by Sharpe Ratio:

     pair       pnl  sharpe  trades
0  (KO, PEP)   42.8    1.47     93
1  (WMT, TGT)  37.1    1.33     88
2  (MSFT, AAPL) 28.5   1.12     76
```

---


## 🚀 Try It Yourself

Install dependencies:

```bash
pip install yfinance statsmodels matplotlib pandas
```

Run the notebook in Jupyter or any IDE to explore live results.

---

## 📘 Credits

Thanks to:
- [Statsmodels](https://www.statsmodels.org/)
- [Yahoo Finance](https://finance.yahoo.com/)
- Quant Twitter and GitHub for inspiring this project.

---

## ⭐️ Star This Repo

If you liked this project or learned something, consider giving it a ⭐️ — it helps more people discover it!
