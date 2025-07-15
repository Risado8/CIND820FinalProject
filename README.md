
# Predicting Financial Literacy Using Machine Learning  
**Capstone Project – TMU Data Analytics Certificate**  
**Author:** Marisa Donnelly  
**Date:** July 14, 2025 

---

## Project Overview  
This project explores how machine learning models can be used to classify financial literacy levels across countries based on behavioural indicators. Using data from the [Global Findex Database (2017)](https://globalfindex.worldbank.org/), I constructed a proxy variable for financial literacy and tested the performance of logistic regression, random forest, and XGBoost classifiers.  

The goal was to identify which behaviours are most predictive of higher financial literacy and to evaluate which model balances performance and interpretability best.

---

## Repository Contents  
- `2025-DonnellyCapstoneFinLiteracy.ipynb` – The main Jupyter Notebook including:
  - Data cleaning and preparation  
  - Proxy score creation  
  - Binary class labeling  
  - Model training and evaluation  
  - SHAP-based feature interpretation  

- `plots/` – Folder containing exported model comparison graphs and feature importance visualizations  
- `data/` – Cleaned dataset used for modeling (derived from Global Findex 2017)  
- `README.md` – This file

---

## Models Used  
- **Logistic Regression** – Offers interpretability and baseline performance  
- **Random Forest** – Strong predictive accuracy, good feature ranking  
- **XGBoost** – Best overall performance, paired with SHAP for interpretability  

Each model was evaluated on precision, recall, F1-score, and accuracy using a held-out test set.  

---

## Key Findings  
- Emergency savings ability, digital payments, and mobile account ownership were the most influential predictors.  
- XGBoost achieved the highest overall performance but required more effort to interpret.  
- Logistic regression provided more transparent insights into feature effects, ideal for policy communication.  

---

## Video Presentation  
A five-minute walkthrough of this project is available as part of the assignment submission. It includes:  
- Project overview and goals  
- Description of key steps in the workflow  
- Summary of model comparisons and results  

---

## References  
The analysis was informed by relevant literature including:  
- Global Findex Database (World Bank, 2017)  
- Lusardi & Mitchell (2014) – *The Economic Importance of Financial Literacy*  
- Fernandes et al. (2014) – *Financial literacy and financial behaviour*  
- Grohmann et al. (2018) – *Does Financial Literacy Improve Financial Inclusion?*  
- Lee et al. (2023), Elouaourti et al. (2024) – *Machine learning applications in financial inclusion*

See the full references list in the main report.
