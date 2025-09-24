# Project 3 – Portfolio Risk Dashboard  

## 1. Data Preparation  
- **Source file**: `calc_metrics.xlsx`  
- **Sheets**:  
  - `stock_returns_wide`: daily returns (AAPL, AMZN, MSFT, TSLA, Portfolio_EQ).  
  - `Metrics`: calculated risk metrics (Annual Return, Annual Volatility, Sharpe, 1-day 95% VaR).  
- **Processing steps**:  
  - Checked missing values.  
  - Calculated daily log returns.  
  - Built cumulative returns (per stock + portfolio).  
  - Aggregated monthly returns.  
  - Computed key risk metrics in Excel.  

---

## 2. Python Validation (`Project3.ipynb`)  
Used to cross-check Excel calculations:  
- Calculated log returns and cumulative performance.  
- Aggregated monthly returns.  
- Verified Annual Return, Volatility, Sharpe Ratio, and VaR.  

---

## 3. Tableau Visualization (`Project 3.twbx`)  
The dashboard contains:  
1. **KPI Cards**  
   - Annual Return  
   - Annual Volatility  
   - Sharpe Ratio  
   - 1-day 95% VaR  
2. **Line Chart** – Cumulative performance of portfolio & stocks.  
3. **Heatmap** – Monthly returns (red = negative, green = positive).  

---

## 4. Output  
- **`Dashboard 1.png`**: Snapshot of the final dashboard.  
- Interactive version can be uploaded to **Tableau Public**.  

---

## 5. Skills Applied  
- **Excel** → data cleaning, risk metrics calculation.  
- **Python** → validation & reproducibility.  
- **Tableau** → KPI dashboard design, heatmap, cumulative return visualization.  

---

## 6. How to Reproduce  
1. Open `calc_metrics.xlsx` to explore raw and processed data.  
2. Run `Project3.ipynb` to replicate metrics.  
3. Open `Project 3.twbx` in Tableau to view and interact with the dashboard.  

---

🔥 This project demonstrates an **end-to-end workflow**: from data prep → risk analysis → interactive visualization.
