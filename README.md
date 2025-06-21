# 🛍️ Retail Product Price Optimization

## 📌 Project Overview

This project aims to build a **Machine Learning model** that determines the **optimal pricing** for retail products. The goal is to **maximize profitability** while staying competitive in the market.

We utilize **historical sales data**, **competitor prices**, and **product features** to predict the **next optimal price (`lag_price`)** for each product.

---

## 🚨 Problem Statement

Retail companies often struggle to set the right prices across various product categories:

* **High prices** → Lower sales
* **Low prices** → Reduced profit margins

This project solves the issue through **data-driven price optimization**, ensuring a balanced strategy between **profitability** and **market competitiveness**.

---

## ✅ Key Benefits

* 💰 **Increased Profitability** via optimized pricing
* 🏆 **Better Market Positioning** by analyzing competitor pricing
* 📊 **Actionable Insights** on seasonality, competition, and product features

---

## 📂 Dataset Information

| Feature                         | Description                               |
| ------------------------------- | ----------------------------------------- |
| `product_id`                    | Unique product ID                         |
| `product_category_name`         | Product category                          |
| `month_year`                    | Timestamp of the sales record             |
| `qty`                           | Quantity sold                             |
| `total_price`                   | Total sales value                         |
| `freight_price`                 | Shipping cost                             |
| `unit_price`                    | Price per unit                            |
| `product_score`                 | Product rating                            |
| `customers`                     | Number of customers                       |
| `weekday`, `weekend`, `holiday` | Calendar-based flags                      |
| `volume`                        | Product volume                            |
| `comp_1`, `comp_2`, `comp_3`    | Competitor pricing                        |
| `ps1`, `ps2`, `ps3`             | Competitor product scores                 |
| `fp1`, `fp2`, `fp3`             | Competitor freight prices                 |
| `lag_price`                     | Target variable (previous period’s price) |

---

## 🔁 Project Workflow

1. **Data Preprocessing**

   * Handle missing values (median imputation)
   * Convert `month_year` to datetime
   * Remove irrelevant columns (`product_id`, `product_category_name`)

2. **Exploratory Data Analysis (EDA)**

   * Monthly sales trends
   * Price vs Quantity sold
   * Price comparison with competitors
   * Feature correlations

3. **Feature Engineering**

   * Competitor price differences
   * Extract `month` and `year` from date

4. **Model Building**

   * 🎯 Primary: **Random Forest Regressor**
   * 📏 Benchmark: **Ridge Regression**

5. **Model Evaluation**

   * Metrics: R² Score, MAE
   * Interpretability: SHAP summary plots, permutation importance

6. **Visualizations**

   * Sales trends over time
   * Feature importance
   * Actual vs Predicted prices

---

## 📊 Results Summary

| Model            | R² Score  | MAE    |
| ---------------- | --------- | ------ |
| Random Forest    | \~0.98881 | \~3.79 |
| Ridge Regression | \~0.98802 | \~4.31 |

> 📌 *Final results may vary based on hyperparameter tuning and data splits.*

---

## 🛠 Tools & Technologies

* 🐍 Python
* 📦 Pandas, NumPy
* 📈 Seaborn, Matplotlib
* 🤖 Scikit-learn
* 🔍 SHAP (Model Explainability)

---

## 📁 Project Structure

```bash
.
├── Determining Optimal Pricing for Retail Products.ipynb  # Jupyter notebook
├── retail_price.csv                                       # Dataset
└── README.md                                              # Project summary
```

---

## ▶️ How to Run

1. **Install dependencies:**

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn shap
   ```

2. **Launch the notebook:**

   ```bash
   jupyter notebook
   ```

3. **Open & run:**
   Run `Determining Optimal Pricing for Retail Products.ipynb` step-by-step.

---

## 📬 Contact

For feedback, questions, or collaboration opportunities, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/ask-pratik-bokade/).
