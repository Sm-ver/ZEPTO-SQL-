Here’s a **README** you can include at the top of your SQL project or Jupyter Notebook. It explains your work clearly and professionally:

---

# 📘 README — Zepto Product Dataset Analysis

## 🔍 Objective:

The purpose of this project is to explore, clean, and analyze the `ZEPTO_V2` dataset to generate actionable insights related to product pricing, inventory, revenue, discounts, and stock status.

---

## 📁 Sections Covered:

### 1. **Data Exploration**

* View complete dataset:
  `SELECT * FROM ZEPTO_V2;`
* Total number of rows:
  `SELECT COUNT(*) FROM ZEPTO_V2;`
* Preview first 10 rows (sample data):
  `SELECT * FROM ZEPTO_V2 LIMIT 10;`
* Identify missing/null values:
  Checks for `NULL` in all key columns like `name`, `MRP`, `discountPercent`, etc.
* List of unique product categories:
  `SELECT DISTINCT CATEGORY FROM ZEPTO_V2;`
* Product availability (in stock vs out of stock):
  Grouped count based on `OUTOFSTOCK` column.

---

### 2. **Data Cleaning**

* Identified and removed products with `MRP` or `DiscountedSellingPrice` equal to 0.
* Converted price data from **paise to rupees** for accurate calculations.
* Checked for products with same name appearing multiple times (potential duplicates).

---

### 3. **Data Analysis Queries**

#### 🔟 Q1: Top 10 Best Value Products

* Sorted by highest discount percentage.

#### 🛒 Q2: High MRP Products That Are Out of Stock

* MRP > ₹300 and `OUTOFSTOCK = 'true'`.

#### 💰 Q3: Estimated Revenue Per Category

* Revenue = `DiscountedSellingPrice * AvailableQuantity`.

#### 📉 Q4: Products with High MRP and Low Discount

* MRP > ₹500 and Discount < 10%.

#### 📦 Q5: Top 5 Categories by Average Discount

* Categories offering best value via average discounts.

#### ⚖️ Q6: Price per Gram for Products > 100g

* Sorted to find best value per gram.

#### 🏷️ Q7: Weight-Based Product Grouping

* Categorized into `LOW`, `MEDIUM`, `BULK` based on weight.

#### 🏋️ Q8: Total Inventory Weight by Category

* `weightInGms * availableQuantity` grouped by category.

---

## ✅ Summary of Insights:

* High discounts offer value to price-sensitive customers (Q1, Q5, Q6).
* Some expensive products are out of stock, suggesting demand or supply chain issues (Q2).
* Certain categories drive higher revenue and inventory load (Q3, Q8).
* Weight and pricing patterns help in planning logistics and pricing strategy (Q4, Q6, Q7).

---

## 📌 Notes:

* Ensure to run **data cleaning steps** before analysis.
* Consider indexing or optimizing queries for large datasets.
* Handle repeated product names cautiously during aggregation.

---

Let me know if you'd like this as a downloadable `.md` or `.txt` file too!





