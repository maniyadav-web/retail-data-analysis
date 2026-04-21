# 🛒 Online Retail Sales Analysis

A data analysis project built with Python that explores a real-world online retail dataset to uncover revenue trends, top-performing products, seasonal patterns, and country-wise sales distribution.

---

## 📌 Objective

To perform exploratory data analysis (EDA) on an online retail transaction dataset containing over **541,909 records**, with the goal of:

- Cleaning and preprocessing raw transactional data
- Identifying the **top revenue-generating products**
- Analyzing **monthly sales trends** to detect seasonal demand
- Evaluating **country-wise revenue distribution**
- Deriving actionable business insights to support strategic decisions

---

## 📂 Project Structure

```
retail_analysis/
│
├── retail_analysis.ipynb     # Main Jupyter Notebook with full analysis
└── README.md                 # Project documentation
```

---

## 📂 Dataset

The dataset used in this project is publicly available:

🔗 [https://raw.githubusercontent.com/guipsamora/pandas_exercises/master/07_Visualization/Online_Retail/Online_Retail.csv](https://raw.githubusercontent.com/guipsamora/pandas_exercises/master/07_Visualization/Online_Retail/Online_Retail.csv)

---

## 📊 Dataset

| Property | Details |
|---|---|
| **Source** | [Pandas Exercises – Online Retail CSV](https://raw.githubusercontent.com/guipsamora/pandas_exercises/master/07_Visualization/Online_Retail/Online_Retail.csv) |
| **Records** | 541,909 rows |
| **Columns** | 8 |
| **Size** | ~33 MB |
| **Encoding** | Latin-1 |

### Columns Description

| Column | Type | Description |
|---|---|---|
| `InvoiceNo` | object | Unique invoice/transaction number |
| `StockCode` | object | Product/item code |
| `Description` | object | Product name/description |
| `Quantity` | int | Number of units purchased |
| `InvoiceDate` | object → datetime | Date and time of the transaction |
| `UnitPrice` | float | Price per unit (in GBP) |
| `CustomerID` | float | Unique customer identifier (has missing values) |
| `Country` | object | Country of the customer |
``

---

## 🔍 Analysis Breakdown

### 1. 🧹 Data Cleaning
- Loaded dataset from a public URL with Latin-1 encoding
- Identified missing values in `Description` (~1,454 rows) and `CustomerID` (~135,000 rows)
- Dropped rows with missing `Description` values
- `CustomerID` was intentionally ignored since customer-level analysis was out of scope
- Converted `InvoiceDate` from string to datetime format

### 2. 💰 Revenue Analysis
- Created a new `Revenue` column: `Quantity × UnitPrice`
- Calculated **Total Revenue ≈ £9.74 Million**
- Identified **Top 10 Revenue-Generating Products** using grouped aggregation
- Key products: `DOTCOM POSTAGE`, `REGENCY CAKESTAND 3 TIER`, `WHITE HANGING HEART T-LIGHT HOLDER`, `PARTY BUNTING`

### 3. 📅 Monthly Sales Trend
- Extracted month from `InvoiceDate` and grouped revenue by month
- Plotted a line chart to visualize sales over time
- **Peak month: November** — driven by Black Friday and holiday season demand

### 4. 🌍 Country-wise Sales Analysis
- Grouped revenue by `Country` and visualized the top 10 countries
- **United Kingdom** dominates revenue by a large margin
- Other significant markets include Germany, France, and EIRE (Ireland)

---

## 📈 Key Findings

| Insight | Detail |
|---|---|
| Total Revenue | ~£9.74 Million |
| Top Product | DOTCOM POSTAGE |
| Peak Sales Month | November |
| Primary Market | United Kingdom |

- A **small number of products** contribute disproportionately to total revenue (Pareto effect)
- Sales show a strong **seasonal spike** towards the end of the year (Q4)
- The business is **heavily UK-dependent**, suggesting potential for international expansion

---

## 📉 Visualizations

The notebook includes the following charts:

- **Bar Chart** – Top 10 Products by Revenue
- **Line Chart** – Monthly Revenue Trend (with markers and grid)
- **Bar Chart** – Top 10 Countries by Revenue

---

## 💡 Business Recommendations

1. **Stock up on top products** before November to meet seasonal demand
2. **Leverage Black Friday / Christmas campaigns** to maximize Q4 revenue
3. **Explore market expansion** beyond the UK — Germany and France show growth potential
4. **Investigate high-volume postage items** to understand if bundling can drive more product sales

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| Pandas | Data loading, cleaning, and analysis |
| Matplotlib | Data visualization |
| Jupyter Notebook | Interactive development environment |

---

## 👤 Author

> This project, conducted by data analysis student Mani Yadav, investigates real-world retail data using Python.
