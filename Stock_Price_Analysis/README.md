# Stock Price Analysis 📊

## Overview
Analyzed 30-day performance of **Apple (AAPL), Tesla (TSLA), and Amazon (AMZN)** using Python + Excel.  
Focus: daily returns, volatility, and trading volume.

## Methodology
- Pulled data from Yahoo Finance (`yfinance`).
- Calculated % change & log returns with pandas/numpy.
- Built Excel dashboard:
  - PivotTables (Volume by Ticker, Price by Date, Volume by Sector).
  - PivotCharts (Stock Price Trend, Total Volume).
  - Conditional Formatting (abnormal moves > ±5%).

## Key Insights
- **TSLA**: highest volatility, frequent ±5% moves.
- **AAPL**: most stable stock, lowest volatility.
- **AMZN**: moderate fluctuations, upward bias late period.
- **Sectors**: Tech & Auto dominate trading activity vs. Retail.

## Files
- `Stock_Report_Week1.xlsx` – Excel dashboard
- `Stock_Report_Week1.pdf` – Exported PDF report
- `make_week1_data.ipynb` – Python notebook for data pull & cleaning
