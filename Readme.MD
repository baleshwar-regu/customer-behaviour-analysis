# 🛍️ Customer Shopping Behavior Analysis

A full-stack data analytics project that explores customer purchasing patterns across demographics, product categories, and sales behaviors — using Python, PostgreSQL, and Power BI.

---

## 📌 Project Overview

A retail company wanted to better understand its customers' shopping behavior to improve sales, customer satisfaction, and long-term loyalty. This project analyzes 3,900 transactions to uncover trends in spending patterns, customer segmentation, product preferences, discount dependency, and subscription behavior.

> **Business Question:** *How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?*

---

## 🗂️ Project Structure

```
customer-shopping-behavior-analysis/
│
├── data/
│   └── customer_shopping_data.csv        # Raw dataset
│
├── python/
│   └── data_cleaning.py                  # Data loading, cleaning & EDA
│
├── sql/
│   └── business_queries.sql              # SQL queries for business analysis
│
├── powerbi/
│   └── customer_behaviour_dashboard.pbix # Power BI dashboard file
│
├── reports/
│   ├── Customer_Shopping_Behavior_Analysis.pdf
│   └── Business_Problem_Document.pdf
│
└── README.md
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| Python (pandas) | Data cleaning, EDA, feature engineering |
| PostgreSQL | Structured business queries |
| Power BI | Interactive dashboard & visualization |
| GitHub | Version control & project hosting |

---

## 📊 Dataset Summary

- **Rows:** 3,900 transactions
- **Columns:** 18 features
- **Key Fields:** Age, Gender, Location, Category, Item Purchased, Purchase Amount (USD), Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Frequency of Purchases

---

## 🔧 Data Preparation (Python)

- Loaded dataset using `pandas` and explored structure with `df.info()` and `.describe()`
- Imputed 37 missing values in `Review Rating` using **median per product category**
- Renamed columns to **snake_case** for consistency
- Created `age_group` column via binning customer ages
- Created `purchase_frequency_days` derived column
- Dropped redundant `promo_code_used` column (confirmed duplicate of `discount_applied`)
- Exported cleaned data to **PostgreSQL** for SQL analysis

---

## 🗃️ SQL Analysis (PostgreSQL)

Ten business questions were answered using structured SQL queries:

1. **Revenue by Gender** — Male customers generated ~2x the revenue of female customers ($157,890 vs $75,191)
2. **High-Spending Discount Users** — 839 customers used discounts yet spent above the average purchase amount
3. **Top 5 Products by Rating** — Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.78)
4. **Shipping Type Comparison** — Express shipping averages $60.48 vs Standard at $58.46
5. **Subscribers vs Non-Subscribers** — Similar avg spend (~$59.50 vs $59.87); non-subscribers generate 73% of total revenue
6. **Discount-Dependent Products** — Hat (50%), Sneakers (49.66%), Coat (49.07%), Sweater (48.17%), Pants (47.37%)
7. **Customer Segmentation** — Loyal: 3,116 | Returning: 701 | New: 83
8. **Top 3 Products per Category** — Jewelry, Blouse, Sandals, and Jacket lead their respective categories
9. **Repeat Buyers & Subscriptions** — 2,518 non-subscribers vs 958 subscribers among repeat buyers
10. **Revenue by Age Group** — Young Adult ($62,143) > Middle-aged ($59,197) > Adult ($55,978) > Senior ($55,763)

---

## 📈 Power BI Dashboard

An interactive dashboard was built with the following visuals:

- **KPI Cards** — Total Customers (3.9K), Average Purchase Amount ($59.76), Average Review Rating (3.75)
- **Donut Chart** — Subscription status split (73% Non-Subscribers, 27% Subscribers)
- **Bar Charts** — Revenue and Sales by Category (Clothing leads both)
- **Horizontal Bar Charts** — Revenue and Sales by Age Group
- **Slicers** — Subscription Status, Gender, Category, Shipping Type

---

## 💡 Business Recommendations

- **Boost Subscriptions** — Currently only 27% of customers subscribe. Offer exclusive subscriber discounts or early access to drive sign-ups.
- **Customer Loyalty Programs** — With 3,116 loyal customers, a tiered rewards system can deepen retention and increase lifetime value.
- **Review Discount Policy** — ~50% of purchases for certain products use discounts; evaluate margin impact and reduce dependency where possible.
- **Product Positioning** — Promote top-rated products (Gloves, Sandals, Boots) and best-sellers (Blouse, Jewelry) in targeted campaigns.
- **Targeted Marketing** — Focus on Young Adult and Middle-aged segments — they contribute the highest revenue. Express shipping users also spend slightly more.
- **Gender-Based Strategy** — Male customers contribute significantly more revenue; analyze category preferences to tailor offerings for female customers and close the gap.

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
   cd customer-shopping-behavior-analysis
   ```

2. **Install Python dependencies**
   ```bash
   pip install pandas psycopg2 sqlalchemy
   ```

3. **Run the cleaning script**
   ```bash
   python python/data_cleaning.py
   ```

4. **Run SQL queries** in PostgreSQL after the data is loaded by the Python script

5. **Open the Power BI dashboard**
   - Open `powerbi/customer_behaviour_dashboard.pbix` in Power BI Desktop

---

## 📄 License

This project is for educational and portfolio purposes.

---

## 🙋 Author

**Your Name**  
[LinkedIn](https://linkedin.com/in/your-profile) • [GitHub](https://github.com/your-username)
