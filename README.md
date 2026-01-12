# Diabetes Diagnosis Classification (Group Coursework)

## Overview
Group coursework project investigating whether demographic, lifestyle, and self-reported health factors
can predict an individual’s diabetes status, and which factors contribute most to model decisions.

The project followed a two-stage workflow:
- **Stage 1:** exploratory analysis to understand data structure and identify potentially influential predictors.
- **Stage 2:** model comparison under a unified, leakage-safe preprocessing + resampling pipeline.

## Data & Task
- Binary classification: **Diabetes vs No Diabetes**
- Mixed feature types (numerical + categorical)
- Moderate class imbalance (handled during modelling)

## Methodology (Stage 2)
Models compared under a consistent evaluation setup:
- Logistic Regression
- Decision Tree
- Calibrated Linear SVM

Evaluation design:
- Train/test split: **80/20**, with all preprocessing and tuning performed on training only to prevent leakage
- **Stratified 10-fold cross-validation** for hyperparameter tuning and model selection
- Primary metric: **Macro F1** (chosen to balance performance across classes in an imbalanced health screening context)
- Additional metric: ROC-AUC (One-vs-Rest)

## My Contribution
This was a group coursework project.

My main responsibilities included:
- **Data cleaning and preprocessing**, ensuring dataset quality and modelling readiness
- Building and evaluating a **Logistic Regression** model, including hyperparameter tuning (regularisation strength)
- Interpreting results and explaining modelling choices clearly in the final report

## Key Takeaways
- In imbalanced health screening tasks, Macro F1 provides a more meaningful optimisation target than accuracy alone.
- Keeping preprocessing, resampling, and training inside cross-validation is essential to avoid information leakage.
- Consistent pipelines make multi-model comparisons reliable and reproducible.

## Tools
Python, Pandas, NumPy, scikit-learn, imbalanced-learn, Jupyter Notebook

## Repo Contents
- `diabetes_diagnosis_workflow.ipynb` — end-to-end workflow (preprocessing → modelling → evaluation)
- `report.pdf` — final report
- `archive/` — optional exploratory materials (Stage 1)
