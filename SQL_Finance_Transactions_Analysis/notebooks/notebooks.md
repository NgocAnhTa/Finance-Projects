# Notebooks

This folder contains Jupyter notebooks used for the **SQL–Python integration** and **data visualization** steps of the project.  

---

## 📂 Files

### 🔹 data.ipynb
- Purpose: **Data preparation & database setup**.  
- Main steps:
  - Load `transactions.csv` (50k rows).  
  - Create a SQLite database `finance.db`.  
  - Write initial SQL queries (row count, preview, sanity check).  
- Output:
  - SQLite database file `finance.db`.  
  - CSV export of clean transactions data.

---

### 🔹 anomaly_and_charts.ipynb
- Purpose: **Fraud detection & visualization**.  
- Main steps:
  - Connect to `finance.db` with SQLite.  
  - Run SQL queries:
    - Top users by spending  
    - Daily average spending  
    - Fraud detection using the **3σ rule per user**  
  - Export results into CSV files:
    - `top_users.csv`  
    - `daily_avg_spending.csv`  
    - `fraud_like_transactions.csv`  
  - Visualize results using **matplotlib**:
    - Line chart of daily average spending  
    - Scatter plot with flagged fraud-like transactions
- Output:
  - Charts saved in `/images/` folder.  

---

## 📝 Notes
- Notebooks are complementary:  
  - `data.ipynb` → prepares the data.  
  - `anomaly_and_charts.ipynb` → analyzes and visualizes.  
- Run them in order for full reproducibility.  
