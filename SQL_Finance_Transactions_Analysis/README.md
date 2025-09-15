# SQL Finance Transactions Analysis  

This project demonstrates an **end-to-end financial data analytics pipeline** using SQL, Python, and Excel.  
The dataset simulates **50,000 financial transactions** (user, merchant, amount, date).  

---

## 🔹 Objectives
- Practice SQL queries for financial datasets.  
- Detect abnormal (fraud-like) transactions using statistical methods (3σ rule).  
- Visualize insights with Python (matplotlib) and Excel Dashboard.  
- Build a portfolio-ready project showcasing SQL ↔ Python ↔ Dashboard integration.  

---

## 📂 Project Structure
SQL_Finance_Transactions_Analysis/
│
├── data/
│   ├── transactions.csv            # raw dataset (50k rows)
│   ├── top_users.csv               # output: spending by user
│   ├── daily_avg_spending.csv      # output: daily average spending
│   └── fraud_like_transactions.csv # output: flagged anomalies
│
├── notebooks/
│   ├── data.ipynb                  # create DB, first queries
│   └── anomaly_and_charts.ipynb    # anomaly detection + charts
│
├── scripts/
│   └── queries.sql                 # main SQL queries
│
├── images/
│   ├── daily_avg_spending.png      # daily trend chart
│   └── fraud_scatter.png           # scatter with anomalies
│
├── excel/ (optional)
│   └── Project 2.xlsx              # Excel dashboard
│
├── docs/ (optional)
│   └── Project 2.pdf               # full report
│
└── README.md
---

## 🛠️ Tech Stack
- **SQL (SQLite)** → Data queries and anomaly detection  
- **Python (pandas, matplotlib)** → Data processing + charts  
- **Excel / Power BI** → Interactive dashboard for stakeholders  

---

## 📊 SQL Queries
Key examples from [`queries.sql`](scripts/queries.sql):  
```sql
-- Top 5 users by spending
SELECT user_id, SUM(amount) AS total_spent
FROM transactions
GROUP BY user_id
ORDER BY total_spent DESC
LIMIT 5;

-- Daily average spending
SELECT date, AVG(amount) AS avg_spent
FROM transactions
GROUP BY date
ORDER BY date;

-- Fraud detection (3σ rule per user)
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


🚀 Key Takeaways
	•	Designed an SQL–Python pipeline analyzing 50k+ transactions.
	•	Implemented fraud detection using the 3σ rule.
	•	Delivered both code reproducibility (Python/SQL) and business dashboard (Excel).

📌 CV/Portfolio Highlight

“Built a SQL–Python pipeline to analyze 50k+ transactions, detected anomalies using the 3σ rule, and visualized fraud patterns in a reproducible dashboard.”
