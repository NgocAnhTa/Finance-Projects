# Excel Dashboard

This folder contains the **Excel-based dashboard** built on top of the processed transaction data.  

---

## 📂 Files

### 🔹 Project 2.xlsx
- **Type:** Interactive Excel Dashboard  
- **Description:** Combines pivot tables, charts, and conditional formatting for business-friendly analysis.  
- **Components:**
  1. **Top 10 Users by Spending**  
     - Bar chart from `top_users.csv`.  
     - Identifies the biggest spenders in the dataset.  

  2. **Daily Average Spending Trend**  
     - Line chart from `daily_avg_spending.csv`.  
     - Shows changes in average spending per day over 2024.  

  3. **Fraud-like Transactions**  
     - Table view from `fraud_like_transactions.csv`.  
     - Conditional formatting highlights abnormal transactions (>3σ rule).  

- **Use case:**  
  - Business analysts can explore the dataset without writing SQL/Python.  
  - Useful for quick insights, presentations, or stakeholder meetings.  

---

## 📝 Notes
- This Excel dashboard is **optional** — the core pipeline runs on SQL + Python.  
- For reproducibility, see:  
  - Queries in [`/scripts/queries.sql`](../scripts/queries.sql)  
  - Charts in [`/images`](../images/) generated via Python.  
- Excel dashboard serves as a **business-facing deliverable**, while Python/SQL show the **technical pipeline**.
