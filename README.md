# 📈 Fraud Detection Model in Financial Transactions

## 📰 Project Description

This is a capstone machine learning project focused on using **Random Forest** for fraud detection.  
It covers core skills such as **data analysis**, **time-series feature engineering**, and building robust **scikit-learn pipelines**.  
The final model achieved an **F1-Score of 0.98** and **100% precision**.  

Additionally, a **Power BI dashboard** was created to visualize key insights from the dataset, helping to better understand fraud patterns, transaction behavior, and feature impact.

---

## 👤 Project Author

**Vimal Raj R**  
GitHub: [VimalRaj73](https://github.com/VimalRaj73)  
LinkedIn: [Vimal Raj R](https://www.linkedin.com/in/vimalraj73/)

---

## 💡 Project Context

This project introduces fundamental concepts in **data science**, **feature engineering**, and **building data-leakage-proof models** using pipelines.  
It emphasizes key skills such as handling **imbalanced datasets**, creating **predictive features**, and **robust model evaluation**.  
The Power BI report complements the machine learning analysis with **interactive visual exploration** of fraud trends.

---

## 🎯 Project Overview & Goal

This project applies machine learning to predict **fraudulent financial transactions**.  
The main goal is to classify each transaction as either:

- **1 → Fraudulent**  
- **0 → Legitimate**

The model achieved an **F1-Score of ~0.98** and **100% Precision**, proving that the engineered features were highly effective at identifying fraud with **zero false positives** (no legitimate users were blocked).

---

## 🛠️ Tools & Libraries

The following tools and Python libraries were used (as listed in `requirements.txt`):

### 🧰 Python Stack
- **Pandas:** Data handling, cleaning, and feature engineering  
- **NumPy:** Numerical computations  
- **Scikit-learn:** RandomForestClassifier, Pipeline, ColumnTransformer, evaluation metrics  
- **Imbalanced-learn:** ImbPipeline wrapper for pipeline compatibility  
- **Matplotlib & Seaborn:** Data visualization (Confusion Matrix, ROC Curve)

### 📊 BI & Visualization
- **Power BI:** For interactive dashboard creation and fraud pattern analysis  

---

## 📝 Project Methodology

### 1. Data Preparation
The project used **`Fraud_Analysis_Dataset.csv`**, a pre-sampled dataset with a 1:10 imbalanced ratio  
(**1,142 fraud cases vs. 10,000 non-fraud cases**).

### 2. Feature Engineering
Generated powerful, context-aware predictors, including:

- **hour_of_day:** Captures time-based transaction patterns  
- **ErrorBalanceOrg** & **ErrorBalanceDest:** “Smoking gun” features that check the math of transactions — an error of **exactly 0** was found to be highly predictive of fraud

### 3. Modeling Pipeline
A **Pipeline** with a **ColumnTransformer** was implemented to automate preprocessing and prevent data leakage.

Preprocessing steps included:
- **OneHotEncoder** for the `type` column  
- **StandardScaler** for numerical features  

**Model Used:**  
- **RandomForestClassifier**, chosen for its high accuracy and robustness against imbalanced data.

---

## 📊 Results and Reflection

The model was evaluated on a 20% test split and showed excellent, generalizable performance.

| Metric | Test Score |
| :--- | :--- |
| **F1-Score (Fraud)** | 0.98 |
| **Recall (Fraud)** | 0.96 |
| **Precision (Fraud)** | 1.00 |
| **AUC-ROC** | 0.99 |

### Reflection
The final **F1-score of ~0.98** and **perfect precision** confirm that the **feature engineering**, particularly the `ErrorBalanceOrg` feature, was highly effective in detecting fraud.  
This demonstrates the impact of **domain-specific feature creation** over complex resampling techniques, with strong results even on **imbalanced data**.  

The accompanying **Power BI dashboard** visually showcases key fraud patterns, helping non-technical users explore and interpret the data easily.

---

## 📈 Power BI Dashboard Highlights

-The dashboard provides a high-level "Transaction Overview" of all business activity.

-It displays key performance indicators (KPIs) like total transaction volume, total fraud amount, and total transaction counts.

-A donut chart visually breaks down the proportion of all transaction types (like payments, transfers, etc.).

-An area chart tracks the trend of total transaction volume over time.

-The report contains a second, dedicated "Fraud Deep Dive" page that is filtered to only show fraudulent transactions.

-This fraud page features a bar chart to compare the total fraudulent amount for each specific transaction type.

-It also includes a table that lists the top 10 largest fraudulent transactions to pinpoint the highest-value cases.

---

✨ *A practical beginner-to-intermediate project combining data science and business intelligence to uncover and visualize fraud detection patterns in financial transactions.*
