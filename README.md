# Customer Churn Prediction (Telco Dataset)

## Overview
This project predicts customer churn for a telecommunications company using machine learning.  
The goal is to identify customers most at risk of leaving and provide actionable business recommendations to reduce churn.  

## Dataset
- **Source:** [Telco Customer Churn (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- **Size:** ~7,000 records  
- **Target Variable:** `Churn` (Yes/No)  
- **Features:** Demographics, contract type, tenure, monthly charges, internet services  

## Methodology
1. **Exploratory Data Analysis (EDA)**  
   - Visualized churn distribution  
   - Identified high-risk groups (contract type, tenure, monthly charges)  

2. **Preprocessing**  
   - Cleaned missing values in `TotalCharges`  
   - Encoded categorical variables with one-hot encoding  
   - Train-test split (70/30)  

3. **Modeling**  
   - Logistic Regression (baseline)  
   - Random Forest (advanced)  

4. **Evaluation**  
   - Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC  
   - ROC and Precision-Recall curves  
   - Threshold tuning for ~0.75 recall to prioritize catching churners  

## Results
- Logistic Regression: ROC-AUC ≈ **0.8X**  
- Random Forest: ROC-AUC ≈ **0.9X** (better performance)  
- At chosen threshold (~0.75 recall), the model detects most churners while keeping precision reasonable.  

## Business Insights
- **Contract Type:** Month-to-month customers churn the most.  
- **Tenure:** Customers with tenure under 12 months are at highest risk.  
- **Charges:** Higher monthly charges correlate with churn.  
- **Key Drivers:** Contract type, tenure, monthly charges, fiber optic internet service.  

### Recommendations
- Incentivize upgrades to long-term contracts (e.g., discounts).  
- Target early-tenure customers with retention campaigns.  
- Offer loyalty rewards to high-value customers.  

## Next Steps
- Hyperparameter tuning for Random Forest  
- Experiment with uplift modeling to target persuadable churners  
- Deploy model in a real-time retention dashboard  

## How to Run This Project
1. Open [Google Colab](https://colab.research.google.com/).  
2. Upload the notebook (`churn_notebook.ipynb`) and dataset CSV.  
3. Run all cells to reproduce results.  

---
