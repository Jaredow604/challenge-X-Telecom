
# 📉 Predictive Customer Churn Modeling

### Transitioning from Reactive to Proactive Retention at Telecom X

## 📖 Executive Summary

This repository contains **Phase 2** of the Telecom X customer analytics initiative. Following the initial Exploratory Data Analysis (EDA), this project focuses on building robust **predictive models** to identify at-risk customers before they cancel their subscriptions (Churn).

By leveraging machine learning, this tool empowers the business to transition from a reactive customer service model to a **data-driven, proactive retention strategy**.

## 🧠 The Machine Learning Pipeline

### 1. Data Engineering & Preprocessing

* **Feature Selection:** Purged non-predictive identifiers (e.g., `customerID`) to reduce noise.
* **Categorical Encoding:** Applied One-Hot Encoding (`pd.get_dummies`) to transform text-based categorical variables into a machine-readable numerical format.
* **Class Balancing (SMOTE):** Addressed the inherent dataset imbalance by generating synthetic data for the minority class (churned customers), ensuring a strict 50/50 distribution for unbiased model training.

### 2. Model Training & Evaluation

The dataset was split into an **80% training** and **20% testing** subset. Two primary algorithms were trained and evaluated:

* **Logistic Regression:** Implemented as a baseline model, utilizing `StandardScaler` for feature normalization.
* **Random Forest Classifier:** An ensemble learning method utilizing multiple decision trees to capture complex, non-linear patterns.

## 📊 Key Insights & Results

After rigorous evaluation using Confusion Matrices, Precision, Recall, and F1-Scores, a clear winner emerged.

* 🏆 **Champion Model:** The **Random Forest** algorithm outperformed the baseline, achieving an **84% Accuracy** on the testing data and demonstrating a high success rate in isolating true at-risk accounts.
* 🔍 **Primary Churn Drivers:** Feature Importance analysis revealed the top three variables dictating customer departure:
1. **Tenure** (Customer lifespan with the company)
2. **Monthly Charges**
3. **Total Accumulated Charges**



## 💡 Strategic Business Recommendations

* **Early Intervention Programs:** The risk of churn spikes during the initial months. Implementing a robust onboarding sequence is critical for day-one loyalty.
* **Proactive Price Optimization:** Deploy the model to trigger automated alerts when a customer's monthly charge pushes them into the "risk zone," allowing retention teams to offer targeted plan adjustments.
* **Long-Term Contract Incentives:** Month-to-month contracts are highly volatile. The business should heavily incentivize the transition to annual commitments through exclusive benefits.

## 🛠️ Tech Stack

* **Language:** Python
* **Data Manipulation:** `Pandas`, `NumPy`
* **Visualization:** `Matplotlib`, `Seaborn`
* **Machine Learning:** `Scikit-Learn`
* **Data Balancing:** `Imbalanced-Learn`

## ⚙️ Quick Start Guide

To replicate this environment and run the analysis locally, follow these steps:

1. **Clone the repository:**
```bash
https://github.com/Jaredow604/challenge-X-Telecom.git

```


2. **Install the required dependencies:**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn

```


3. **Execute the analysis:** Open the main `.ipynb` notebook and run it cell by cell.

---
