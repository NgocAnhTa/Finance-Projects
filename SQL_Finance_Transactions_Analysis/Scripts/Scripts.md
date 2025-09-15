# Scripts

This folder contains the **SQL scripts** used for querying and analyzing the transactions dataset.  

---

## 📂 Files

### 🔹 queries.sql
- Purpose: Collect all SQL queries used in this project.  
- Content includes:  
  1. **Data sanity checks**
     ```sql
     -- Count total rows in the transactions table
     SELECT COUNT(*) FROM transactions;

     -- Preview the first 5 rows
     SELECT * FROM transactions LIMIT 5;
     ```

  2. **User-level aggregation**
     ```sql
     -- Total spending per user
     SELECT user_id, SUM(amount) AS total_spent
     FROM transactions
     GROUP BY user_id
     ORDER BY total_spent DESC;
     ```

  3. **Time-series analysis**
     ```sql
     -- Daily average spending
     SELECT date, AVG(amount) AS avg_spent
     FROM transactions
     GROUP BY date
     ORDER BY date;
     ```

  4. **Fraud detection**
     ```sql
     -- Per-user anomaly detection using 3σ rule
     WITH user_stats AS (
         SELECT user_id,
                AVG(amount) AS mean_amt,
                sqrt((SUM(amount*amount)*1.0/COUNT(*)) - (AVG(amount)*AVG(amount))) AS std_amt
         FROM transactions
         GROUP BY user_id
     )
     SELECT t.*
     FROM transactions t
     JOIN user_stats s USING(user_id)
     WHERE t.amount > s.mean_amt + 3*s.std_amt
        OR t.amount < s.mean_amt - 3*s.std_amt;
     ```

- Output: These queries feed into the CSVs in [`/data`](../data/) and the visualizations in [`/images`](../images/).  

---

## 📝 Notes
- The script is written for **SQLite**, so some functions (like `STDDEV()`) are replaced with manual formulas.  
- To run:  
  - Open the database `finance.db` in VS Code (SQLTools or SQLite extension).  
  - Open `queries.sql` → select query → run.  
- Queries are modular: you can run them independently.  
