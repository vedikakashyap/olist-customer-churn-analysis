# 🛒 Olist Customer Churn Analysis

## Project Overview
This is an end-to-end data analytics project analyzing customer churn on the 
Brazilian Olist e-commerce platform. The goal was to understand why customers 
don't return after their first purchase, predict future churners using machine 
learning, and present findings through an interactive dashboard.

**Dataset:** [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) — Kaggle  
**Tools Used:** Python, Pandas, Matplotlib, Seaborn, Scikit-learn, Power BI, Jupyter Notebook

---

## 🔍 Business Problem
Olist loses a significant portion of its customers after just one purchase. 
This project investigates the key drivers of churn and builds a predictive 
model to identify at-risk customers before they leave.

---

## 📊 Key Findings

| Metric | Value |
|--------|-------|
| Overall Churn Rate | 58.9% |
| Total Customers Analysed | 93,350 |
| Customers with only 1 order | 96.9% |
| Repeat Customers | Only 2,891 (3.1%) |

### Delivery Impact on Churn
- ✅ On-time delivery → **46.8% churn**
- ❌ Very late delivery → **70.9% churn**
- A **24-point gap** — delivery is the single biggest controllable factor

### Product Category
- Worst retention: **Cool Stuff (73.8%)**, **Toys (70.7%)**
- Best retention: **Watches & Gifts (48.8%)**, **Automotive (50.4%)**

### Geography
- Best state: **São Paulo — 55.7% churn**
- Worst state: **Maranhão — 66.7% churn**

---

## 🤖 Machine Learning Model

Built a **Random Forest Classifier** to predict customer churn.

| Metric | Score |
|--------|-------|
| AUC Score | 0.682 |
| Model Accuracy | 65% |
| Churner Recall | 77% |

### Top Features Driving Churn Prediction
1. Total Spend — 24.3%
2. Avg Spend per Order — 24.2%
3. Avg Delivery Delay — 19.6%
4. Favourite Product Category — 16.4%
5. Customer State — 10.0%

---

## 📁 Project Structure
olist-customer-churn-analysis/
│
├── data/                         # Raw CSV files from Kaggle
├── outputs/                      # All charts, model, dashboard
│   ├── master_customer_table.csv
│   ├── chart1_churn_by_review.png
│   ├── chart2_churn_by_delay.png
│   ├── chart3_churn_by_category.png
│   ├── chart4_churn_by_state.png
│   ├── chart5_churn_by_spend.png
│   ├── chart6_orders_distribution.png
│   ├── chart7_roc_curve.png
│   ├── chart8_feature_importance.png
│   ├── ├── churn_model.pkl        # Not included (322MB) - run notebook 04 to regenerate
│   └── Olist_Churn_Dashboard.pbix
├── 01_data_loading.ipynb
├── 02_feature_engineering.ipynb
├── 03_exploratory_analysis.ipynb
├── 04_churn_prediction_model.ipynb
└── README.md
---

## 📈 Dashboard Preview

Built an interactive 4-page Power BI dashboard covering:
- Executive Summary (Churn KPIs)
- Logistics Analysis (Delivery delay vs churn)
- Category & State Analysis
- ML Model Results

---

## 💡 Business Recommendations

1. **Fix delivery first** — Reducing late deliveries is the highest-impact action. 
   A 24-point churn gap between on-time and very late deliveries is significant.
2. **Investigate Cool Stuff & Toys categories** — These have the worst retention 
   and need quality or expectation audits.
3. **Target high-spend customers** — Spend is the top ML predictor. 
   Retention campaigns should prioritise higher-value customers first.
4. **Focus on São Paulo** — Best performing state, ideal for piloting 
   any retention program before scaling nationally.

---

## 🚀 How to Run This Project

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
2. Place all CSV files inside the `data/` folder
3. Run notebooks in order: 01 → 02 → 03 → 04
4. Note: churn_model.pkl is not included in this repo due to file size (322MB).
   Running notebook 04 will automatically regenerate and save it to your outputs folder.
5. Open `outputs/Olist_Churn_Dashboard.pbix` in Power BI Desktop

---

## 👨‍💻 Author
**Vedika**  
BTech Final Year | Aspiring Data Analyst  
[LinkedIn](#) • [GitHub](#)
