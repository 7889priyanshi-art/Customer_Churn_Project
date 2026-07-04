 ## Telco Customer Churn Prediction & Segmentation

## Project Overview

Customer retention is critical for subscription-based businesses. This project leverages machine learning to predict customer churn and applies unsupervised learning to segment high-risk users. By identifying at-risk customers and grouping them by behavioral traits, this solution enables businesses to deploy data-driven, targeted retention strategies that maximize customer lifetime value (LTV).



## Dataset Profile

* **Dataset:** Telco Customer Churn Dataset
* **Volume:** 7,043 unique customer records
* **Features:** Customer demographics, account profiles, subscribed services, tenure metrics, and billing configurations.

---

## End-to-End Workflow

### 1. Data Engineering & Preprocessing

* **Data Cleaning:** Isolated and resolved missing values within `Total Charges`, aligned mismatched data types, and stripped out non-predictive identifiers.
* **Feature Encoding:** Transformed categorical variables using **One-Hot Encoding** to construct a model-ready feature space.

### 2. Predictive Modeling (Supervised Learning)

* **Validation Strategy:** Implemented an 80:20 train-test split to ensure robust evaluation.
* **Algorithm:** Trained a **Random Forest Classifier**.
* **Imbalance Mitigation:** Integrated `balanced` class weights to counter dataset skewness and boost minority class (churners) sensitivity.
* **Hyperparameter Tuning:** Conducted grid searches over key parameters, including *Number of Trees* ($n\_estimators$) and *Maximum Tree Depth* ($max\_depth$).

### 3. Feature Intelligence & Evaluation

* **Feature Importance:** Extracted tree-based feature importances to pinpoint the primary drivers behind customer attrition.
* **Performance Metrics:** Evaluated comprehensively using:
* Accuracy Score
* Confusion Matrix
* Precision, Recall, and F1-Score (via Classification Report)
* ROC-AUC Score



### 4. Behavioral Segmentation (Unsupervised Learning)

* **Feature Synthesis:** Extracted individual churn probabilities from the Random Forest model and combined them with standardized customer attributes.
* **Clustering:** Applied **K-Means Clustering** to discover distinct, actionable customer personas.

---

##  Identified Customer Segments

Based on the clustering analysis, three strategic customer personas emerged:

* **Budget Loyal Customers:** Low-spending users with high tenure; highly stable but price-sensitive.
* **High-Risk New Customers:** High-churn probability segments characterized by low tenure and volatile early behavior.
* **Loyal Premium Customers:** High-value, high-spending accounts with a strong footprint of subscribed services and low propensity to leave.

---

##  Tech Stack

* **Language:** Python
* **Data Wrangling:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Visualization:** Matplotlib, Seaborn

---

## Key Outcomes

The Random Forest classifier successfully flags high-risk churners before they exit. By feeding these insights into the K-Means pipeline, the project provides a seamless bridge between raw data prediction and automated marketing execution—allowing businesses to target the *High-Risk New Customers* with proactive incentives while maintaining the LTV of *Loyal Premium Customers*.

---

##  Roadmap & Future Scope

* [ ] **Gradient Boosting:** Implement **XGBoost** and **LightGBM** to push predictive boundaries.
* [ ] **Advanced Optimization:** Utilize Optuna or Bayesian Optimization for hyperparameter tuning.
* [ ] **Interactive Dashboard:** Build and deploy a **Streamlit** web application for business stakeholders.
* [ ] **M LOps Integration:** Transition toward real-time stream processing for instant churn-risk scoring.
