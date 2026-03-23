📊 Global Unemployment Analysis (1991–2025)

Project Summary
This project analyzes global unemployment trends across 183 countries to uncover patterns in economic performance, gender inequality, and labor market stability.
Built using Python (Pandas), the analysis simulates real-world business problem-solving and decision-making.
________________________________________
🎯 Key Business Questions
•	How has global unemployment changed over time?
•	Which countries perform best and worst?
•	Is there a gender gap in unemployment?
•	Which countries show stable vs volatile trends?
________________________________________
📊 Key Insights (Executive Summary)
🌍 Global Trend
•	Long-term decline in unemployment (1991–2019)
•	Sharp spike in 2020 → global disruption
•	Gradual recovery post-2020
________________________________________
🌐 Country Performance (Latest Year)
•	🔴 Highest: Djibouti (~40.7%)
•	🟢 Lowest: Qatar (~0.26%)
👉 Highlights extreme global inequality in job markets
________________________________________
⚖️ Gender Inequality
•	Female: 11.74%
•	Male: 9.58%
👉 Women face consistently higher unemployment globally
________________________________________
🚩 Top Gender Gap Countries
•	Egypt
•	Syrian Arab Republic
•	Libya
👉 Gap exceeds 12–16 percentage points
 
________________________________________
📉 Stability vs Volatility
•	🔺 Most volatile: Georgia
•	✅ Most stable performers: Solomon Islands, Tanzania
________________________________________
🏆 Best Performing Countries
(Based on high performance + low volatility)
•	Tanzania
•	Madagascar
•	Solomon Islands
________________________________________
🧰 Tech Stack
•	Python
•	Pandas
•	Matplotlib
•	Jupyter Notebook
________________________________________
📂 Dataset
•	57,519 rows | 6 columns
•	No missing values
•	Features: country, gender, age, year, unemployment rate
________________________________________
🔍 Methodology
Data Preparation
•	Converted categorical columns for efficiency
•	Validated data quality
Analysis Techniques
•	GroupBy → trend analysis
•	Pivot Tables → gender comparison
•	Standard deviation → volatility
•	Year-over-year change → growth trends
________________________________________
📈 Sample Code
# Global trend
df.groupby("year")["obs_value"].mean()

# Country comparison (latest year)
df_latest = df[(df["year"] == df["year"].max()) & (df["sex"] == "Total")]

# Gender gap
pivot["gap"] = pivot["Female"] - pivot["Male"]
________________________________________
📊 Visualizations
•	Global trend (line chart)
•	Gender gap (bar chart)
________________________________________
🧠 What This Project Demonstrates
✔ Real-world data analysis workflow
✔ Business insight generation
✔ Data cleaning & transformation
✔ Analytical thinking (not just coding)
________________________________________
🚀 How to Run
pip install pandas matplotlib
Open notebook and run all cells.
________________________________________
📌 Future Improvements
•	Power BI dashboard
•	Regional analysis
•	Predictive modeling
________________________________________
👤 Author
Bhavesh Suryavanshi
Aspiring Data Analyst
Python | SQL | Data Storytelling

Aspiring Data Analyst
Python | SQL | Data Storytelling
