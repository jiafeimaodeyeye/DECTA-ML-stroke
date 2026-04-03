# DECTA-ML-stroke

## Overview

This repository contains the complete analysis code for the manuscript:

> **Multimodal Machine Learning Incorporating Dual-Energy CT Plaque and Perivascular Adipose Tissue Parameters for Predicting Acute Ischemic Stroke: A Dual-Center Study**

The code implements a machine learning pipeline that integrates dual-energy CT angiography (DECTA)-derived intraplaque and perivascular adipose tissue (PVAT) parameters with clinical biomarkers to predict acute ischemic stroke risk.

## Study Design

- **Training cohort** (Center 1, n=137) and **external validation cohort** (Center 2, n=75)
- Feature selection via LASSO regression
- Four candidate models compared: Logistic Regression, Random Forest, XGBoost, and SVM
- Final model selected by a composite scoring system integrating AUC, Brier score, and net benefit

## Notebook Structure

The analysis is organized in a single Jupyter Notebook (`V9-SVW-Dual-Center-Code-English.ipynb`) with the following sections:

| Part | Description |
|------|-------------|
| 1 | Data preprocessing and standardization |
| 2 | Between-group statistical comparison |
| 3 | LASSO feature selection |
| 4 | Model training with cross-validation and composite scoring |
| 5 | Final SVM model construction |
| 6–7 | Model evaluation on training and test sets (ROC, PR, calibration, DCA) |
| 8–9 | SHAP interpretability analysis |
| 10 | Risk stratification |

## Requirements

- Python ≥ 3.8
- Key packages: `scikit-learn`, `xgboost`, `shap`, `pandas`, `numpy`, `scipy`, `statsmodels`, `matplotlib`, `seaborn`

Install all dependencies:

```bash
pip install pandas numpy scikit-learn xgboost shap scipy statsmodels matplotlib seaborn joblib
```

## Reproducing the Analysis

1. Place the source data file (`MX.xlsx`,`YZJ.xlsx` ) in the project directory.
2. Open and run `V9-SVW-Dual-Center-Code-English.ipynb` sequentially.
3. All figures and evaluation outputs are generated automatically.

## Contact

Yankai Meng — mengyankai@126.com
