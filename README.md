# 🛒 Customer Shopping Trends & Revenue Analysis System

This project establishes an end-to-end data analytics pipeline designed to analyze retail customer behavior, optimize sales strategies, and evaluate the effectiveness of loyalty programs. It covers the full data lifecycle: performing ETL (Extract, Transform, Load) using **Python**, conducting advanced exploratory analysis using **SQL**, and visualizing KPIs with **Power BI**.

## 📌 Business Problem Statement
A retail organization required a detailed analysis of their customer database (3,900+ records) to address stagnating retention rates and optimize marketing spend. The primary business goals were to:
1.  **Evaluate Subscription ROI:** Determine if subscribed customers actually generate higher Lifetime Value (LTV) than non-subscribers.
2.  **Optimize Shipping Logistics:** Analyze if "Express" shipping leads to higher average basket sizes compared to standard options.
3.  **Demographic Segmentation:** Identify which age groups and genders drive the highest revenue to tailor marketing campaigns.
4.  **Discount Efficiency:** Identify products that rely too heavily on discounts to sell, indicating potential pricing strategy issues.

## 🛠️ Tech Stack & Methodology

### 1. Data Engineering & Preprocessing (Python/Pandas)
* **Data Cleaning:** Handled missing values in the `Review Rating` column using median imputation grouped by product category to preserve distribution integrity.
* **Standardization:** implemented `snake_casing` for all column headers to ensure SQL compatibility.
* **Feature Engineering:**
    * Converted textual purchase frequency (e.g., "Weekly") into numeric intervals for temporal analysis.
    * Created `Age Group` bins to segment customers into demographic cohorts.
* **Database Loading:** Utilized `SQLAlchemy` to construct a robust connection string and push the cleaned dataframe into a PostgreSQL/MySQL environment.

### 2. Exploratory Data Analysis (Advanced SQL)
Executed complex SQL queries to extract actionable insights, utilizing:
* **Window Functions (`ROW_NUMBER`, `RANK`):** To identify top-selling products within specific categories.
* **Common Table Expressions (CTEs):** To restructure complex logic for customer segmentation (New vs. Recurring vs. Loyal).
* **Aggregations & Grouping:** To calculate revenue contributions by gender, location, and season.
* **Case Statements:** To categorize transaction types and shipping methods dynamically.

### 3. Business Intelligence (Power BI)
Developed an interactive dashboard to visualize the SQL findings:
* **DAX Measures:** Custom calculations for Average Transaction Value (ATV), Conversion Rates, and Total Revenue.
* **Data Modeling:** Established relationships between fact and dimension tables (Star Schema approach).
* **Interactive Filtering:** Slicers for Region, Subscription Status, and Product Category to allow stakeholders to drill down into specific data points.

## 📂 Project Structure

```bash
├── data/
│   └── customer_shopping_behavior.csv    # Raw dataset
├── notebooks/
│   └── Customer_Shopping_Behavior_Analysis.ipynb  # Python ETL & EDA steps
├── sql/
│   └── customer_behavior_sql_queries.sql # SQL scripts for business questions
├── dashboard/
│   └── customer_behavior_dashboard.pbix  # Power BI source file
└── README.md

```bash


🚀 How to Run This Project
Prerequisites
Python 3.x (Pandas, SQLAlchemy, PyODBC/Psycopg2)

PostgreSQL, MySQL, or MS SQL Server

Power BI Desktop

Here is the revised README.md.

My "Consultant" Logic for these changes:

Cut the "Influencer" Fluff: I removed all the "Watch my video," "Subscribe to my channel," and "Perfect for aspirants" text. That stuff makes a GitHub repo look like a marketing funnel rather than a technical workspace.

Added Technical Depth: Instead of just saying "Data Analysis," I specified the types of analysis (e.g., Cohort Analysis, Window Functions, ETL).

Business Context: I added a "Business Problem Statement" section. Technical skills are useless if you can't frame them as business solutions. This makes the project look like real work, not a homework assignment.

Markdown

# 🛒 Customer Shopping Trends & Revenue Analysis System

This project establishes an end-to-end data analytics pipeline designed to analyze retail customer behavior, optimize sales strategies, and evaluate the effectiveness of loyalty programs. It covers the full data lifecycle: performing ETL (Extract, Transform, Load) using **Python**, conducting advanced exploratory analysis using **SQL**, and visualizing KPIs with **Power BI**.

## 📌 Business Problem Statement
A retail organization required a detailed analysis of their customer database (3,900+ records) to address stagnating retention rates and optimize marketing spend. The primary business goals were to:
1.  **Evaluate Subscription ROI:** Determine if subscribed customers actually generate higher Lifetime Value (LTV) than non-subscribers.
2.  **Optimize Shipping Logistics:** Analyze if "Express" shipping leads to higher average basket sizes compared to standard options.
3.  **Demographic Segmentation:** Identify which age groups and genders drive the highest revenue to tailor marketing campaigns.
4.  **Discount Efficiency:** Identify products that rely too heavily on discounts to sell, indicating potential pricing strategy issues.

## 🛠️ Tech Stack & Methodology

### 1. Data Engineering & Preprocessing (Python/Pandas)
* **Data Cleaning:** Handled missing values in the `Review Rating` column using median imputation grouped by product category to preserve distribution integrity.
* **Standardization:** implemented `snake_casing` for all column headers to ensure SQL compatibility.
* **Feature Engineering:**
    * Converted textual purchase frequency (e.g., "Weekly") into numeric intervals for temporal analysis.
    * Created `Age Group` bins to segment customers into demographic cohorts.
* **Database Loading:** Utilized `SQLAlchemy` to construct a robust connection string and push the cleaned dataframe into a PostgreSQL/MySQL environment.

### 2. Exploratory Data Analysis (Advanced SQL)
Executed complex SQL queries to extract actionable insights, utilizing:
* **Window Functions (`ROW_NUMBER`, `RANK`):** To identify top-selling products within specific categories.
* **Common Table Expressions (CTEs):** To restructure complex logic for customer segmentation (New vs. Recurring vs. Loyal).
* **Aggregations & Grouping:** To calculate revenue contributions by gender, location, and season.
* **Case Statements:** To categorize transaction types and shipping methods dynamically.

### 3. Business Intelligence (Power BI)
Developed an interactive dashboard to visualize the SQL findings:
* **DAX Measures:** Custom calculations for Average Transaction Value (ATV), Conversion Rates, and Total Revenue.
* **Data Modeling:** Established relationships between fact and dimension tables (Star Schema approach).
* **Interactive Filtering:** Slicers for Region, Subscription Status, and Product Category to allow stakeholders to drill down into specific data points.

## 📂 Project Structure

```bash
├── data/
│   └── customer_shopping_behavior.csv    # Raw dataset
├── notebooks/
│   └── Customer_Shopping_Behavior_Analysis.ipynb  # Python ETL & EDA steps
├── sql/
│   └── customer_behavior_sql_queries.sql # SQL scripts for business questions
├── dashboard/
│   └── customer_behavior_dashboard.pbix  # Power BI source file
└── README.md
🚀 How to Run This Project
Prerequisites
Python 3.x (Pandas, SQLAlchemy, PyODBC/Psycopg2)

PostgreSQL, MySQL, or MS SQL Server

Power BI Desktop

Step 1: Clone the Repository
Bash

git clone [https://github.com/ishaq019/Customer Shopping Trends & Revenue Analysis System.git]
(https://github.com/ishaq019/Customer Shopping Trends & Revenue Analysis Systemgit)

cd customer-trends-data-analysis-SQL-Python-PowerBI

Step 2: Data Pipeline Execution
Open Customer_Shopping_Behavior_Analysis.ipynb in Jupyter Notebook or VS Code.

Run the cells to clean the data.

Update the database connection string in the final cell to match your local SQL instance credentials.

Execute the load script to populate your SQL database with the customers table.

Step 3: SQL Analysis
Open your SQL Client (pgAdmin, MySQL Workbench, or SSMS).

Load customer_behavior_sql_queries.sql.

Execute queries individually to generate insights regarding customer loyalty, shipping trends, and product performance.

Step 4: Dashboard Visualization
Open customer_behavior_dashboard.pbix in Power BI.

Go to Transform Data > Data Source Settings.

Update the server/database credentials to point to your local SQL instance.

Refresh the data to populate the visuals.


📜 License
MIT License — Free to use for educational and portfolio purposes.
"# Customer-Shopping-Trends-Revenue-Analysis-System-" 
