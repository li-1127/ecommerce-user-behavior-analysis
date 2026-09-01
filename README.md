# E-commerce User Behavior Analysis

This project analyzes real-world e-commerce transaction data to identify high-value products and core customer segments. The insights support inventory management and precision marketing strategies.

## 💡 Key Findings

### Top 5 Best-Selling Products (by Revenue)

| Rank | Product Description | Qty Sold | Total Revenue |
| :--- | :--- | :--- | :--- |
| 1 | REGENCY CAKESTAND 3 TIER | 476 | $5,363.40 |
| 2 | BLACK RECORD COVER FRAME | 1,141 | $3,868.35 |
| 3 | WHITE HANGING HEART T-LIGHT HOLDER | 1,014 | $2,665.70 |
| 4 | CHILLI LIGHTS | 572 | $2,379.24 |
| 5 | RED WOOLLY HOTTIE WHITE HEART | 726 | $2,275.14 |

### Top 5 High-Value Customers

| Rank | Customer ID | Frequency | Total Spend |
| :--- | :--- | :--- | :--- |
| 1 | 15061 | 73 | $9,407.34 |
| 2 | 13777 | 33 | $6,585.16 |
| 3 | 17850 | 297 | $5,391.21 |
| 4 | 16210 | 25 | $4,738.54 |
| 5 | 16029 | 12 | $4,271.52 |

## 🛠 Tech Stack
- **Language:** Python 3.x
- **Data Processing:** Pandas
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebook

## 📊 Dataset Overview
- **Source:** `ecommerce_data.csv`
- **Scope:** Dec 1–6, 2010
- **Volume:** 12,462 raw records | 8 fields

| Field | Type | Description |
| :--- | :--- | :--- |
| InvoiceNo | String | Unique transaction ID |
| StockCode | String | Product code |
| Description | String | Product name |
| Quantity | Float | Purchase quantity |
| InvoiceDate | Datetime | Transaction time |
| UnitPrice | Float | Price per unit |
| CustomerID | Int | Unique customer ID |
| Country | String | Customer location |

## 🧹 Data Cleaning
Processed raw data to ensure accuracy:

| Step | Action | Impact |
| :--- | :--- | :--- |
| 1 | Removed missing CustomerID | -3,506 rows |
| 2 | Removed missing Description | -45 rows |
| 3 | Handled other nulls & duplicates | -~191 rows |
| **Final** | **Valid Records Retained** | **8,720 rows** |

## 📂 Project Structure
```text
E-commerce-User-Behavior-Analysis/
├── README.md                 # Project documentation
├── ecommerce_data.csv        # Raw dataset
└── ecommerce_analysis.ipynb  # Analysis code

## 🚀 How to Run

To run this project locally, ensure you have Python installed, then execute the following commands in your terminal:

```bash
# 1. Install required libraries
pip install pandas matplotlib jupyter

# 2. Launch the Jupyter Notebook
jupyter notebook ecommerce_analysis.ipynb

