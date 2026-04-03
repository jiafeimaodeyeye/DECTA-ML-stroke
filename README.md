# DECTA-ML-stroke

## Description
This repository provides the code used in the study:

“Multimodal Machine Learning Incorporating Dual-Energy CT Plaque and Perivascular Adipose Tissue Parameters for Predicting Acute Ischemic Stroke: A Dual-Center Study”.

## Study Design
A dual-center retrospective study with:
- Training cohort (Center 1)
- Independent external validation cohort (Center 2)

## Workflow
1. Data preprocessing  
   - Z-score normalization based on the training cohort  

2. Feature selection  
   - LASSO regression with 10-fold cross-validation  

3. Model development  
   - Logistic Regression  
   - Random Forest  
   - XGBoost  
   - Support Vector Machine (SVM)  

4. Hyperparameter tuning  
   - Grid search with 10-fold cross-validation  

5. Model evaluation  
   - Discrimination: AUC  
   - Calibration: Brier score  
   - Clinical utility: Net benefit (decision curve analysis)  

6. Model selection  
   - Composite scoring system integrating AUC, Brier score, and Net benefit  

7. External validation  
   - Independent cohort evaluation  

## Notes
- Patient data are not publicly available due to privacy restrictions  
- The code can be executed with user-provided datasets following the same structure  

## Environment
Python 3.13  
Key packages: scikit-learn, xgboost, shap, pandas, numpy  

## Contact
For questions, please contact the corresponding author.
