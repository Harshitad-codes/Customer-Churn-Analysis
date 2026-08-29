# Customer Churn Analysis & Customer Intelligence

An end-to-end data analytics project that connects a SQL database to Python, cleans and engineers features, performs exploratory analysis, and visualizes the key drivers of customer churn for a subscription business.

## Tech Stack
- **Python** - sqlite3, pandas, numpy
- **Visualization** - matplotlib, seaborn
- **Environment** -Jupyter Notebook

## Workflow

1. **Data Import** - Connected to a SQLite database and loaded customer, subscription, and support tables into pandas using SQL queries via `sqlite3`.
2. **Data Cleaning** - Renamed columns, corrected data types (dates), standardized categorical values (e.g. gender), handled missing values, and resolved duplicate records.
3. **Feature Engineering** - Built a churn flag from cancellation dates, merged tables (customer + subscription + support), and derived fields such as customer tenure, complaint counts, and churn-risk tiers.
4. **Exploratory Data Analysis** - Used pandas groupby, aggregation, and pivot tables to calculate churn rate, retention rate, ARPU, revenue at risk, escalation rate, and complaint metrics.
5. **Visualization** - Built time-series trends, bar charts, a correlation heatmap, a pairplot, and a multi-dimensional cat-plot with matplotlib and seaborn to surface churn drivers.

## Key Insights

| Metric | Value |
|---|---|
| Overall churn rate | 28.57% |
| Retention rate | 71.43% |
| Churn — Basic plan | 60.00% |
| Churn — Standard plan | 22.22% |
| Churn — Premium plan | 14.29% |
| Average revenue per user (ARPU) | 18.85 |
| Revenue at risk (churned users) | 73.94K |
| Escalation rate | 19.05% |
| Avg. complaints per user | 0.43 |
| Correlation: escalations vs. churn | 0.77 (strong) |

**Takeaway:** Basic-plan customers churn at roughly 4x the rate of Premium customers, and support escalations are strongly correlated with churn — suggesting retention efforts should prioritize early escalation resolution and Basic-tier engagement.

## How to Run

1. Clone this repo
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `Customer_Churn_Analysis.ipynb` in Jupyter Notebook, JupyterLab, or VS Code
4. Run all cells top to bottom

## Note on the Data

The underlying dataset is a sample dataset and is not included in this repo — see the notebook's first cell for instructions on generating the database locally.
