# Early Prognosis of MAFLD Progression Using Deep Learning

This repository documents our project from the MIT EECS and Sloan MLHC 2025 collaboration, focused on early prognosis of Metabolic Dysfunction-Associated Fatty Liver Disease (MAFLD) using deep learning and structured EHR data from Mass General Brigham.


## Project Overview

We developed and evaluated three models to predict MAFLD progression using structured clinical features:

- A **Binary Classification model** that predicts whether a patient will progress to advanced liver disease.
- A **Time-to-Event model** that estimates the number of days until disease progression.
- A **DeepSurv Survival model** that provides individualized risk scores over time.

We also implemented SHAP interpretation and regression analysis to identify key biomarkers of progression.

The goal: to improve early clinical risk stratification and guide potential treatment strategies.



## Methods

- **Binary Neural Network**: Predicts progression vs. non-progression using 2,850 clinical features.
- **Time-to-Event Regression**: Estimates days to progression using MSE loss.
- **DeepSurv (Survival Net)**: Deep Cox model for time-to-progression with interpretability via SHAP.
- **Baselines**: Logistic regression, linear regression, and Cox PH model for comparison.
- **Class Imbalance Techniques**: SMOTE, downsampling, and weighted loss—none improved generalization.



## Key Insights

- The **Survival Net** achieved a concordance index of 0.55 and Brier score of 0.055.
- **Time-to-event regression** yielded ~376-day MAE, performing well relative to a 6-year progression window.
- SHAP analysis revealed influential features: cholesterol levels, reticulocyte counts, and BMI before diagnosis.
- Class imbalance remains a major limitation—future work may leverage larger datasets or text data.



## Team

Jeannie She, Erica Song, Naiqi Zhang  
Developed as part of MIT’s Machine Learning for Healthcare (MLHC) program.

