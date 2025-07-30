# Predicting Financial Literacy Using Machine Learning  
**Capstone Project – TMU Data Analytics Certificate**  
**Author:** Marisa Donnelly  
**Date:** July 29, 2025

---

## Project Overview  
This capstone project investigates whether machine learning can classify countries by financial literacy levels using behavioural indicators from the [Global Findex Database (2017)](https://globalfindex.worldbank.org/).  

A proxy score was constructed by averaging key financial behaviour variables (e.g., saving, borrowing, digital payments). Models were trained to classify countries into high vs. low financial literacy based on this score. The objective was to build models that are both accurate and interpretable for potential use in financial outreach or policy planning.

---

## Repository Contents  
- `2025-DonnellyCapstoneFinLiteracyFinal.ipynb` – Jupyter Notebook containing:
  - Data cleaning and exploratory analysis  
  - Construction of the proxy score  
  - Feature preprocessing with `Pipeline` and `ColumnTransformer`  
  - Model training: logistic regression, random forest, XGBoost  
  - Model evaluation: metrics, ROC/PR curves  
  - SHAP visualizations and feature importance plots  

- `plots/` – Visuals including:
  - Logistic coefficients  
  - Random forest importances  
  - SHAP summary and dependence plots  
  - Proxy score distribution  

- `data/` – Cleaned dataset derived from the Global Findex survey  
- `README.md` – This file  

---

## Models Used  
- **Logistic Regression**  
  + Highly interpretable; ideal for understanding directionality  
- **Random Forest**  
  + Good generalization; highlights important features  
- **XGBoost**  
  + Best performance; interpreted using SHAP  

Models were evaluated using stratified 5-fold cross-validation and tested on a held-out test set. Metrics included accuracy, precision, recall, F1-score, and ROC-AUC.

---

## Key Findings  
- Emergency savings, digital payment use, and account ownership were the strongest predictors of high financial literacy.  
- XGBoost yielded the best accuracy (96%) but required SHAP to explain predictions.  
- Logistic regression was more interpretable and suitable for communicating policy insights.  
- SHAP dependence plots revealed non-linear feature effects consistent with financial inclusion research.

---

## Limitations and Next Steps  
The project used behavioural proxies instead of direct knowledge-based assessments, which may not fully capture conceptual financial literacy. Additionally, using country-level data limits our ability to understand within-country disparities. Future work should extend the analysis to household- or individual-level data, integrate additional datasets, and explore transfer learning or fairness-aware models for broader generalizability.

---

## Video Presentation  
A five-minute overview video is available as part of the final submission.  
🎥 [Watch the Video Presentation](https://drive.google.com/file/d/1SeUPu6MJffuIA-PALKsyZXHffuWP5NN0/view?usp=sharing)

---

## References  
- Demirgüç-Kunt et al. (2018) – *The Global Findex Database 2017*  
- Lusardi & Mitchell (2014) – *The Economic Importance of Financial Literacy*  
- Fernandes et al. (2014) – *Financial literacy and downstream financial behaviors*  
- Grohmann et al. (2018) – *Does Financial Literacy Improve Financial Inclusion?*  
- Yue & Zhu (2025) – *Unlocking Financial Literacy with Machine Learning*  
- Lu et al. (2024) – *Financial Literacy in Predicting Credit Default*  
- Huston (2010) – *Measuring Financial Literacy*  
- Haag & Brahm (2025) – *The Gender Gap in Financial Literacy*  
- Lokanan et al. (2021) – *Predicting Fraud Victimization Using ML*  
See the full list in the [Final Report](Donnelly_Marisa_FinalReport.pdf).
