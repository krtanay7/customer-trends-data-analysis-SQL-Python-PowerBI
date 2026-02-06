# Customer Trends — Data Analysis (SQL • Python • Power BI)

This repository contains an end-to-end customer shopping behavior analysis pipeline: a cleaned sample dataset, a Jupyter notebook with data preparation and analysis code, and a set of SQL queries to answer business questions. The materials are suitable for portfolio use, teaching, or reproducing the analysis for a similar dataset.

**Project goals:** prepare and explore customer transaction data, run analytics with SQL, and build visual dashboards in Power BI to surface actionable insights.

**Repository snapshot**
- Dataset: [customer_shopping_behavior.csv](customer_shopping_behavior.csv)
- Notebook: [Customer_Shopping_Behavior_Analysis.ipynb](Customer_Shopping_Behavior_Analysis.ipynb)
- SQL queries: [customer_behavior_sql_queries.sql](customer_behavior_sql_queries.sql)
- This README: [README.md](README.md)

**Quick highlights**
- Data cleaning examples (missing values, renaming, feature engineering) in the notebook.
- Export/load patterns for PostgreSQL / MySQL / SQL Server using SQLAlchemy.
- Pre-built SQL queries covering revenue, product performance, discount impact, and customer segmentation.

**Why this is useful**
- Reproducible end-to-end workflow from raw CSV to database and BI dashboard.
- Hands-on examples for analysts learning Python (pandas), SQL, and database connectivity.

**Getting started (quick)**
**High-level project workflow**
1. Business problem & objectives — define the questions the analysis must answer.
2. Python: Data import, cleaning & EDA — import the CSV, clean data, and perform exploratory analysis (single Python phase).
3. Load cleaned data into a SQL database — create a database/table and write the cleaned DataFrame using the notebook's examples.
4. SQL analysis — run analytical queries against the database to prepare tables and aggregate results for reporting and dashboarding.
5. Power BI: Interactive dashboard — build visuals using SQL views / aggregated tables as the data source.
6. Insights & project report — summarize findings and business recommendations.
7. Presentation to stakeholders — present insights; tool choices (Gamma, PowerPoint, etc.) are optional.

**Repository & deliverables (final/parallel)**
 - Publish code, SQL, dashboard files, report and presentation to the GitHub repository as the final deliverable (this is a parallel/final step, not one of the sequential analysis phases).

**Getting started (quick)**
1. Clone the repository and open the notebook:

```bash
git clone https://github.com/krtanay7/customer-trends-data-analysis-SQL-Python-PowerBI
cd customer-trends-data-analysis-SQL-Python-PowerBI
```

2. (Optional) Create a Python environment and install essentials:

```powershell
python -m venv .venv
.
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt  # if provided
```

Minimal packages used in the notebook: pandas, sqlalchemy, and a DB driver such as `psycopg2-binary` / `pymysql` / `pyodbc`.

3. Open and run the notebook: [Customer_Shopping_Behavior_Analysis.ipynb](Customer_Shopping_Behavior_Analysis.ipynb). The notebook's Python phase combines:
 - Importing the raw CSV
 - Data cleaning and imputation
 - Column renaming and basic feature engineering (age groups, purchase frequency mapping)
 - Light EDA (summary statistics, null checks, sample visualizations)
 - Code examples to write the cleaned DataFrame into a SQL database (PostgreSQL / MySQL / SQL Server) — use this to perform the explicit "Load cleaned data into SQL" step.

4. Use [customer_behavior_sql_queries.sql](customer_behavior_sql_queries.sql) as the SQL analysis phase. These queries expect a `customer` table with columns matching the cleaned dataset produced by the notebook.

5. Build the Power BI dashboard using the aggregated SQL outputs or exported CSVs created in step 4.

6. Produce the written report (Insights & Project Report) and prepare the stakeholder presentation. Tool names such as Gamma AI are optional and not required for recruiters or standard presentations.

**Files & purpose**
- [customer_shopping_behavior.csv](customer_shopping_behavior.csv): raw dataset (preview included in the notebook).
- [Customer_Shopping_Behavior_Analysis.ipynb](Customer_Shopping_Behavior_Analysis.ipynb): analysis notebook with code for cleaning, feature engineering, and DB load.
- [customer_behavior_sql_queries.sql](customer_behavior_sql_queries.sql): curated SQL questions (revenue, discounts, product ranking, segmentation).

**Next steps & suggestions**
- Add `requirements.txt` listing packages used by the notebook (`pandas`, `sqlalchemy`, `psycopg2-binary`, `pymysql`, `pyodbc`).
- Add a small `data_preview.py` script that prints a head() and schema to help run checks programmatically.
- If you have a `.pbix` Power BI file for the dashboard, add it to the repo or provide a short video/screenshots of the final visuals.

**Contributing / Contact**
If you'd like improvements (more examples, reproducible Docker/dev container, or a cleaned `requirements.txt`), open an issue or tell me what to add next.

---
If you want, I can (a) add a `requirements.txt`, (b) produce a compact `data_preview.py`, or (c) commit the improved README — tell me which next step you prefer.
