# Superstore-Sales-Analysis
# 📊 Superstore Sales Analysis & Prediction

An end-to-end **Superstore Sales Analysis and Prediction** project using **Python, SQL, Machine Learning, and Power BI** to analyze sales, profit, customer segments, product categories, and regional performance.

The project transforms raw sales data into meaningful business insights and uses Machine Learning to support sales prediction and data-driven decision-making.

---

## 🎯 Project Objective

The main objectives of this project are:

- Analyze overall sales and profit performance
- Identify top-performing and low-performing products
- Analyze sales and profit by category and sub-category
- Understand customer segment performance
- Analyze regional and state-wise performance
- Study the impact of discounts on sales and profit
- Identify sales trends over time
- Perform SQL-based business analysis
- Build a Machine Learning model for sales prediction
- Create an interactive Power BI dashboard
- Generate actionable business recommendations

---

# 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **SQL**
- **Power BI**
- **DAX**
- **Jupyter Notebook**

---

# 🔄 Project Workflow

```text
Raw Superstore Dataset
        ↓
Data Cleaning using Python
        ↓
Exploratory Data Analysis
        ↓
SQL Business Analysis
        ↓
Feature Engineering
        ↓
Machine Learning
        ↓
Sales Prediction
        ↓
Power BI Dashboard
        ↓
Business Insights & Recommendations

🐍 1. Python – Data Cleaning & EDA
Python was used to clean, preprocess, analyze, and visualize the Superstore dataset.

Data Cleaning
The following activities were performed:
Checked dataset structure
Checked missing values
Checked duplicate records
Verified data types
Converted date columns
Handled inconsistent values
Created useful analytical features
Prepared data for Machine Learning


Libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns


Exploratory Data Analysis
The analysis focused on:
Sales
Profit
Quantity
Discount
Category
Sub-Category
Segment
Region
State
Ship Mode
Order Date


🗄️ 2. SQL – Business Analysis
SQL was used to perform structured analysis and answer important business questions.
SQL Analysis Includes
Total sales
Total profit
Total orders
Sales by category
Profit by category
Sales by region
Profit by region
Top-performing products
Low-performing products
Customer segment analysis
Discount and profit analysis
Monthly and yearly sales trends


Example: Category-wise Sales & Profit
SELECT
    Category,
    SUM(Sales) AS Total_Sales,
    SUM(Profit) AS Total_Profit
FROM superstore
GROUP BY Category
ORDER BY Total_Sales DESC;
Example: Top 10 Products
SELECT
    Product_Name,
    SUM(Sales) AS Total_Sales
FROM superstore
GROUP BY Product_Name
ORDER BY Total_Sales DESC
LIMIT 10;
Example: Region-wise Performance
SELECT
    Region,
    SUM(Sales) AS Total_Sales,
    SUM(Profit) AS Total_Profit
FROM superstore
GROUP BY Region
ORDER BY Total_Profit DESC;


🤖 3. Machine Learning – Sales Prediction
Machine Learning was used to develop a predictive model for estimating sales based on relevant business and transaction features.


ML Workflow
Cleaned Dataset
      ↓
Feature Selection
      ↓
Feature Engineering
      ↓
Categorical Encoding
      ↓
Train-Test Split
      ↓
Model Training
      ↓
Sales Prediction
      ↓
Model Evaluation


Potential Features
Features can include:
Quantity
Discount
Category
Sub-Category
Segment
Region
Ship Mode
State
Order Date-related features
Model
A regression-based Machine Learning approach can be used for sales prediction.


Example:
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor

X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.2,
    random_state=42
)

model = RandomForestRegressor(
    n_estimators=100,
    random_state=42
)

model.fit(X_train, y_train)

y_pred = model.predict(X_test)
Model Evaluation
The model can be evaluated using:
MAE
MSE
RMSE
R² Score
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

mae = mean_absolute_error(y_test, y_pred)
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)
r2 = r2_score(y_test, y_pred)
Model performance depends on the final features, preprocessing, and model configuration used in the notebook.


📊 4. Power BI – Interactive Dashboard
Power BI was used to create an interactive dashboard for sales and profit analysis.


📌 Dashboard KPIs
Total Sales
Total Profit
Total Quantity
Total Orders
Profit Margin


📈 Dashboard Visualizations
Sales Analysis
Sales by Category
Sales by Sub-Category
Sales Trend over Time
Sales by Region
Sales by State
Profit Analysis
Profit by Category
Profit by Sub-Category
Profit by Region
Profit by State
Customer Analysis
Sales by Segment
Profit by Segment
Discount Analysis
Discount vs Sales
Discount vs Profit
Impact of Discount on Profitability


📐 DAX Measures
Total Sales
Total Sales =
SUM('superstore'[Sales])
Total Profit
Total Profit =
SUM('superstore'[Profit])
Total Quantity
Total Quantity =
SUM('superstore'[Quantity])
Total Orders
Total Orders =
DISTINCTCOUNT('superstore'[Order_ID])
Profit Margin
Profit Margin % =
DIVIDE(
    [Total Profit],
    [Total Sales],
    0
)


🎛️ Power BI Slicers
Interactive filters include:
Order Date
Category
Sub-Category
Region
Segment
Ship Mode
These slicers allow users to explore sales and profit performance dynamically.


💡 Key Business Questions
This project answers questions such as:
Which category generates the highest sales?
Which category generates the highest profit?
Which sub-categories are underperforming?
Which region is most profitable?
Which products generate the most sales?
Which customer segment contributes the most revenue?
How does discount affect profit?
How do sales change over time?
Which states have strong or weak performance?
Can Machine Learning help predict future sales?


💼 Business Insights
The analysis can help businesses:
Identify high-performing categories and products
Detect low-profit or loss-making products
Understand regional performance
Optimize discount strategies
Improve inventory planning
Identify valuable customer segments
Monitor sales trends
Support data-driven sales decisions


🚀 Business Recommendations
Based on the analysis, businesses can consider:
Focusing on high-profit product categories
Reviewing products with consistently low profit
Avoiding excessive discounts that reduce profitability
Strengthening sales strategies in high-potential regions
Improving inventory planning using sales trends
Using predictive analytics to support future sales planning


📂 Project Structure
superstore-sales-analysis/
│
├── data/
│   └── superstore.csv
│
├── notebooks/
│   └── superstore_sales_analysis.ipynb
│
├── sql/
│   ├── 01_basic_analysis.sql
│   ├── 02_sales_profit_analysis.sql
│   └── 03_business_insights.sql
│
├── machine-learning/
│   └── sales_prediction.py
│
├── powerbi/
│   └── superstore_sales_dashboard.pbix
│
├── images/
│   └── dashboard.png
│
├── requirements.txt
├── .gitignore
└── README.md


📋 Dataset Columns
The Superstore dataset contains fields such as:
Row ID
Order ID
Order Date
Ship Date
Ship Mode
Customer ID
Customer Name
Segment
Country
City
State
Postal Code
Region
Product ID
Category
Sub-Category
Product Name
Sales
Quantity
Discount
Profit

🎓 Skills Demonstrated
Python | Pandas | NumPy | Matplotlib | Seaborn | SQL | Machine Learning | Scikit-learn | Power BI | DAX | Data Cleaning | EDA | Data Visualization | Predictive Analytics | Business Analysis

👩‍💻 Author
Poonam Rajora
B.Tech | Aspiring Data Analyst
