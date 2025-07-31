# Predicting Financial Literacy Using Machine Learning  
**Capstone Project – TMU Data Analytics Certificate**  
**Author:** Marisa Donnelly  
**Date:** July 29, 2025  

---

## Project Overview  
This capstone project explores whether machine learning can classify countries by financial literacy levels using behavioural indicators from the [Global Findex Database (2021)](https://globalfindex.worldbank.org/).  

A financial literacy proxy score was first constructed by averaging six key financial behaviour variables (e.g., account ownership, savings, digital payment usage). This proxy was used to label countries as having “high” or “low” financial literacy. The proxy features were then removed from the model input to avoid circular logic, ensuring models relied only on external indicators.  

The goal was to identify the most influential behavioural and socio-economic features associated with financial literacy and to evaluate model performance and interpretability.

---

## Repository Contents  
- `2025-DonnellyCapstoneFinLiteracyFinal.ipynb` – Final Jupyter Notebook with:
  - Data cleaning and missing value imputation  
  - Proxy score construction and binary labeling  
  - Feature preprocessing with `Pipeline` and `ColumnTransformer`  
  - Model training and evaluation (logistic regression, random forest, XGBoost)  
  - SHAP analysis for interpretability  

- `plots/` – Visuals including:
  - Logistic regression coefficients  
  - Random forest feature importances  
  - XGBoost SHAP summary and top predictors  
  - Distribution of proxy scores  

- `data/` – Cleaned version of Global Findex 2021 survey (country-level)  
- `README.md` – This file  

---

## Models Used  
- **Logistic Regression**  
  + Strongest overall accuracy; Transparent and interpretable coefficients  
- **Random Forest**  
  + Captures non-linear relationships and interactions  
- **XGBoost**  
  + Explainability achieved through SHAP  

All models were evaluated using stratified 5-fold cross-validation and a held-out test set. Metrics included accuracy, precision, recall, F1-score, and ROC-AUC.

---

## Key Findings  
- Features related to credit card ownership, borrowing from family, and inactive accounts were strong predictors of financial literacy.  
- XGBoost achieved the highest test accuracy (88%), followed by logistic regression (90.5%) and random forest (82%).  
- SHAP plots helped interpret non-linear effects and highlighted the marginal impact of key behavioural features.  
- Removing proxy variables from model inputs improved validity and interpretability.

---

## Limitations and Next Steps  
The proxy variable was based on observable behaviour rather than conceptual financial understanding. In addition, country-level aggregation limited insight into demographic subgroups. Future directions include:
- Applying models to household-level microdata  
- Performing temporal analysis using Findex survey waves  
- Incorporating fairness-aware ML and hyperparameter tuning  

---

## Video Presentation  
🎥 [Watch the 5-Minute Final Presentation](https://drive.google.com/file/d/1SeUPu6MJffuIA-PALKsyZXHffuWP5NN0/view?usp=sharing)

---

## References  
- Demirgüç-Kunt et al. (2018). *The Global Findex Database 2017*.  
- Lusardi & Mitchell (2014). *The Economic Importance of Financial Literacy*.  
- Fernandes et al. (2014). *Financial literacy and downstream financial behaviors*.  
- Grohmann et al. (2018). *Does Financial Literacy Improve Financial Inclusion?*  
- Yue & Zhu (2025). *Unlocking Financial Literacy with Machine Learning*.  
- Lu et al. (2024). *Financial Literacy in Predicting Credit Default*.  
- Huston (2010). *Measuring Financial Literacy*.  
- Haag & Brahm (2025). *The Gender Gap in Financial Literacy*.  
- Lokanan et al. (2021). *Predicting Fraud Victimization Using ML*.  

Full reference list included in the [Final Report (PDF)](Donnelly_Marisa_FinalReport.pdf).
