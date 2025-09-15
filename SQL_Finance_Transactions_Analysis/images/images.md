# Images

This folder contains **visual outputs** generated from the SQL + Python analysis.  

---

## 📂 Files

### 🔹 daily_avg_spending.png
- **Type:** Line Chart  
- **Description:** Shows the **average daily spending** across all users in 2024.  
- **Insight:** Reveals seasonal or temporal spending trends, useful for understanding consumer behavior.  
- **Source:** Generated in [`anomaly_and_charts.ipynb`](../notebooks/anomaly_and_charts.ipynb) using matplotlib.

---

### 🔹 fraud_scatter.png
- **Type:** Scatter Plot  
- **Description:** Plots all transactions with **flagged outliers (>3σ per user)** highlighted.  
- **Insight:** Clearly separates normal transactions (blue) from suspicious ones (red), useful for fraud detection.  
- **Source:** Generated in [`anomaly_and_charts.ipynb`](../notebooks/anomaly_and_charts.ipynb).

---

## 📝 Notes
- All charts are reproducible by running the notebooks in [`/notebooks`](../notebooks/).  
- Use these images directly in documentation (e.g., [`README.md`](../README.md)) or reports for visual storytelling.  
