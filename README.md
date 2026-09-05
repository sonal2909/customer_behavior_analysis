# customer_behavior_analysis
data analytics to showcase customer behavior analysis using python, power BI and SQL
# 🛍️ Customer Shopping Behavior Analysis

> An end-to-end Data Analytics project using **Python, PostgreSQL, SQL, Power BI, and Gamma** to analyze customer shopping behavior and generate actionable business insights.

---

## 📌 Project Overview

This project analyzes customer shopping behavior using transactional data from **3,900 purchases** across different product categories. The objective is to identify spending patterns, customer segments, product preferences, discount behavior, and subscription trends.

### 🔄 Project Workflow

```text
Raw Dataset
     │
     ▼
🐍 Python
Data Loading + EDA + Cleaning
     │
     ▼
🧹 Data Transformation
Feature Engineering
     │
     ▼
🗄️ PostgreSQL
Database Storage
     │
     ▼
📊 SQL Analysis
Business Questions
     │
     ▼
📈 Power BI
Interactive Dashboard
     │
     ▼
📑 Report + Gamma Presentation
Business Insights & Recommendations
```

---
## 📂 Dataset

The dataset contains:

| Metric         | Details                    |
| -------------- | -------------------------- |
| Total Records  | 3,900                      |
| Total Columns  | 18                         |
| Missing Values | 37 Review Rating values    |
| Analysis Type  | Customer Shopping Behavior |

### Key Features

* Customer demographics
* Product categories
* Purchase amounts
* Subscription status
* Previous purchases
* Discounts
* Review ratings
* Shipping type
* Purchase frequency

---

# 🛠️ Tools & Technologies

| Tool           | Purpose                       |
| -------------- | ----------------------------- |
| 🐍 Python      | Data loading, cleaning, EDA   |
| 🐼 Pandas      | Data manipulation             |
| 🗄️ PostgreSQL | Database storage              |
| 📝 SQL         | Business analysis             |
| 🔗 SQLAlchemy  | Python–PostgreSQL connection  |
| 📊 Power BI    | Dashboard and visualization   |
| 📑 Gamma       | Presentation and storytelling |
| 💻 VS Code     | Development environment       |

---

# 🔍 Project Steps

## 1️⃣ Data Loading

The dataset was loaded into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
df.head()
```

## 2️⃣ Exploratory Data Analysis

EDA was performed to understand:

* Dataset structure
* Data types
* Missing values
* Summary statistics
* Customer demographics
* Purchase behavior
* Product categories
* Ratings and subscriptions

---

## 3️⃣ Data Cleaning

The following cleaning steps were performed:

* Identified missing values
* Filled missing Review Ratings using the median rating of each category
* Standardized column names
* Checked data consistency
* Removed redundant columns

Example:

```python
df['Review Rating'] = df.groupby('Category')['Review Rating'].transform(
    lambda x: x.fillna(x.median())
)
```

---

## 4️⃣ Feature Engineering

New features were created to support deeper analysis.

### Features Created

* `age_group`
* `purchase_frequency_days`
* Customer segmentation

Customers were classified into:

| Segment      | Previous Purchases |
| ------------ | ------------------ |
| 🆕 New       | 1                  |
| 🔄 Returning | 2–10               |
| ⭐ Loyal      | More than 10       |

---

# 🗄️ PostgreSQL Integration

The cleaned dataset was loaded into PostgreSQL using Python.

```text
Python
   ↓
SQLAlchemy + Psycopg2
   ↓
PostgreSQL Database
   ↓
SQL Business Analysis
```

# 📝 SQL Analysis

SQL queries were used to answer important business questions.

### Key Questions

1. Revenue by gender
2. High-spending discount users
3. Top-rated products
4. Shipping type comparison
5. Subscribers vs non-subscribers
6. Discount-dependent products
7. Customer segmentation
8. Top products by category
9. Repeat buyers and subscriptions
10. Revenue by age group

---

# 📊 Power BI Dashboard

An interactive Power BI dashboard was created to visualize important customer and business insights.

### Dashboard Features

* 📈 Revenue analysis
* 👥 Customer demographics
* 🛍️ Category performance
* ⭐ Customer segmentation
* 💳 Subscription analysis
* 🎯 Discount analysis
* 👤 Age group analysis
* 🔍 Interactive filters and slicers
---

# 💡 Results & Insights

The analysis helped identify:

* Important customer spending patterns
* High-value customer segments
* Top-performing products
* Customer loyalty behavior
* Subscription trends
* Discount usage patterns
* Revenue contribution across different groups

### Business Recommendations

* 🎯 Promote subscription benefits to increase conversions.
* ⭐ Develop loyalty programs for repeat customers.
* 💰 Optimize discount strategies to balance sales and profitability.
* 🛍️ Promote highly rated and best-performing products.
* 📈 Focus marketing efforts on high-value customer segments.

---

# 📑 Project Report

A detailed project report was created to document:

* Dataset analysis
* Data cleaning process
* SQL analysis
* Dashboard findings
* Business insights
* Recommendations

📄 **Report:** `report/Customer_Shopping_Behavior_Analysis.pdf`

---

# 🎤 Presentation

A project presentation was created using **Gamma** to communicate:

* Project objectives
* Analysis workflow
* Key insights
* Dashboard findings
* Business recommendations
---

# 📁 Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── notebooks/
│   └── customer_behavior_analysis.ipynb
│
├── sql/
│   └── business_queries.sql
│
├── dashboard/
│   └── customer_dashboard.pbix
│
├── images/
│   ├── dashboard.png
│   ├── python_eda.png
│   ├── postgresql.png
│   └── presentation.png
│
├── report/
│   └── Customer_Shopping_Behavior_Analysis.pdf
│
├── presentation/
│   └── project_presentation.pdf
│
└── README.md
```

---

# 🚀 How to Run the Project

## 1. Clone the Repository

```bash
git clone <your-repository-url>
cd Customer-Shopping-Behavior-Analysis
```

## 2. Install Dependencies

```bash
pip install pandas numpy sqlalchemy psycopg2-binary
```

## 3. Set Up PostgreSQL

Create a database:

```sql
CREATE DATABASE customer_behavior;
```

Update your database credentials in the Python project.

## 4. Run Python Analysis

Run the notebook to:

* Load the dataset
* Perform EDA
* Clean the data
* Create new features
* Load data into PostgreSQL

## 5. Run SQL Queries

Execute the SQL queries in PostgreSQL.

## 6. Open the Power BI Dashboard

Open the `.pbix` file using **Power BI Desktop**.

---

# 💼 Skills Demonstrated

* Python
* Pandas
* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* PostgreSQL
* SQL
* Database Integration
* Power BI
* Dashboard Development
* Business Analysis
* Data Visualization
* Data Storytelling

---

# 📌 Conclusion

This project demonstrates a complete end-to-end data analytics workflow, from raw data to business insights.

It combines **Python for data preparation, PostgreSQL for SQL analysis, Power BI for visualization, and Gamma for presenting findings**.

The project demonstrates the ability to transform raw customer data into meaningful insights and communicate those insights through dashboards, reports, and presentations.
