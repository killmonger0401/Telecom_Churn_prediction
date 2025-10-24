# Telecom Churn Prediction — End-to-End Data Science Project

## Project overview

This repository contains an end-to-end data science project to analyze and predict customer churn for a telecom operator. The workflow includes exploratory data analysis (EDA), feature engineering, handling class imbalance, model training, evaluation, and strategic recommendations for reducing churn. Key insights and high-level results are summarized below. 

---


---

## Notebooks — brief descriptions

### `Telecom_Churn_EDA.ipynb`

* Purpose: data loading, cleaning, exploratory analysis, visualizations, correlation analysis and initial feature observations.
* Typical steps included:

  * Load dataset and inspect missing values / datatypes.
  * Convert/clean tenure, total charges, and other numeric columns.
  * Visualize churn distribution and churn by categorical features (Contract, PaymentMethod, OnlineSecurity, TechSupport, SeniorCitizen).
  * Calculate churn rates across groups and create summary tables/plots.
* Key EDA takeaways: Month-to-month contracts, electronic checks, and lack of Online Security / Tech Support strongly correlate with higher churn. Non-senior citizens showed higher churn propensity in this dataset. 


### `Telecom_Churn_Model_Building.ipynb`

* Purpose: preprocessing, encoding, train/test split, resampling, model selection, training, evaluation and metrics reporting.
* Typical steps included:

  * Encode categorical variables (one-hot encoding).
  * Convert target `Churn` to 1/0.
  * Handle class imbalance using SMOTEENN (synthetic oversampling + cleaning).
  * Train Random Forest and a Decision Tree (resampled) for comparison.
  * Evaluate with accuracy, precision, recall, F1 and confusion matrix; show feature importances.
* Reported model performance : Random Forest (with SMOTEENN) achieved **~93.7% accuracy** and strong precision/recall in the low 90s; model recall reported as **~96%**. A resampled decision tree achieved ~92.6% accuracy but was slightly weaker than the Random Forest. 

---

## Key findings & business recommendations

* **Primary churn drivers:** Contract type (month-to-month), Payment method (electronic checks), and absence of service add-ons (Online Security, Tech Support). 
* **Model capability:** Random Forest with SMOTEENN gives strong classification performance (~93.7% accuracy; ~96% recall) enabling identification of high-risk customers for proactive retention. 

**Actionable recommendations**

1. **Target month-to-month customers** with incentives to upgrade to longer contracts (discounts, bundled offers).
2. **Encourage electronic-check users** to switch to more stable payment methods (e.g., automatic debit) with loyalty incentives.
3. **Bundle or promote Online Security / Tech Support** to at-risk customers — offering a free initial period may lower churn. 

---

