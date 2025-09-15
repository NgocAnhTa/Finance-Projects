# Data Folder

This folder contains both the **raw dataset** and the **processed outputs** from SQL and Python analysis.  

---

## 📂 Files

### 🔹 Raw Data
- **transactions.csv**  
  - Simulated dataset of ~50,000 financial transactions.  
  - Columns:
    - `transaction_id` – unique transaction ID  
    - `user_id` – simulated customer ID  
    - `merchant` – merchant name  
    - `amount` – transaction amount (USD)  
    - `date` – transaction date (2024)  

### 🔹 Processed Data (SQL/Python outputs)
- **top_users.csv**  
  - Total spending per user (sorted descending).  
  - Used for **Top 10 Users by Spending** chart.

- **daily_avg_spending.csv**  
  - Average daily spending across all users.  
  - Used for **Daily Average Spending Trend** chart.

- **fraud_like_transactions.csv**  
  - Transactions flagged as outliers using the **3σ rule per user**.  
  - Columns:
    - `transaction_id`, `user_id`, `merchant`, `amount`, `date`  
    - Only contains suspicious transactions.  
  - Used for **Fraud Detection Scatter Plot**.  

---

## 📝 Notes
- Dataset is **synthetic** and created for educational purposes only.  
- Outputs are reproducible: run the SQL queries in [`scripts/queries.sql`](../scripts/queries.sql) or the Python notebooks in [`../notebooks/`](../notebooks/).  
