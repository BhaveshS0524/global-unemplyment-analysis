## This analysis helps policymakers and organizations:

- Identify countries with high unemployment risk  
- Understand gender inequality in labor markets  
- Detect global economic shocks (e.g., 2020 spike)  
- Compare stable vs volatile economies

# Global Unemployment Analysis (1991–2025)
### Overview
End-to-end analysis of global unemployment trends across 183 countries, segmented by gender and age groups. The project demonstrates practical data analysis using Pandas, with a focus on trend detection, disparity analysis, and country benchmarking.
________________________________________
### Business Questions
•	How has global unemployment evolved over time?
•	Which countries perform best/worst in recent years?
•	Is there a gender gap in unemployment globally and by country?
•	Which countries are stable vs volatile?
________________________________________
### Tech Stack
•	Python, Pandas, Matplotlib
•	Jupyter Notebook
________________________________________
## Dataset
Columns: iso_code, country, sex, age, year, obs_value
•	57,519 rows | 6 columns
•	No missing values; optimized categorical columns (age, sex)
________________________________________
### Methodology
1.	Data Preparation
o	Type optimization: age, sex → category
o	Validation: schema, nulls, duplicates
2.	Aggregation Strategy
o	Global trends: groupby("year").mean()
o	Country comparisons (latest year): filtered on year=max, sex="Total"
o	Gender analysis: pivot_table + gap (Female - Male)
3.	Stability & Volatility
o	Volatility via standard deviation
o	Consistency via year-over-year change (diff)
________________________________________
## Key Insights
### Global Trend
•	Long-term decline in unemployment until 2019
•	Sharp spike in 2020 (global shock)
•	Stabilization/recovery post-2020
________________________________________
### Country Benchmark (Latest Year)
•	Highest unemployment: Djibouti (~40.7%)
•	Lowest unemployment: Qatar (~0.26%)
### Indicates significant cross-country disparity
________________________________________
## Gender Disparity
•	Female: ~11.74% vs Male: ~9.58%
### Persistent global gender gap (~2 pp)
________________________________________
## Top Gender Gap Countries
•	Egypt, Syrian Arab Republic, Libya
### Female unemployment exceeds male by ~12–16 pp
 
________________________________________
## Stability & Volatility
•	Most volatile: Georgia (high std dev)
•	Stable high performers: Solomon Islands, Tanzania
### Trade-off between performance vs stability
________________________________________
## Best Overall Performers
(High mean + low volatility)
•	Tanzania
•	Madagascar
•	Solomon Islands
________________________________________
## Sample Code
Global Trend
trend = df.groupby("year")["obs_value"].mean()
Country Comparison (Latest Year)
latest_year = df["year"].max()
df_latest = df[(df["year"] == latest_year) & (df["sex"] == "Total")]

country_unemp = df_latest.groupby("country")["obs_value"].mean()
Gender Gap
pivot = df.pivot_table(
    values="obs_value",
    index="country",
    columns="sex",
    aggfunc="mean"
)
pivot["gap"] = pivot["Female"] - pivot["Male"]
________________________________________
## Visualizations
•	Global unemployment trend (line chart)
•	Top 10 countries by gender gap (bar chart)
________________________________________
## What This Project Demonstrates
•	Data cleaning & type optimization
•	Aggregation strategies (groupby, pivot)
•	Comparative & trend analysis
•	Converting data → business insights
________________________________________
## How to Run
pip install pandas matplotlib
Open analysis.ipynb and run all cells.
________________________________________
### Next Improvements
•	Add Power BI dashboard
•	Regional/continent-level analysis
•	Forecasting (time series)
________________________________________
👤 Author
Bhavesh
Aspiring Data Analyst | Python • SQL • Data Storytelling
