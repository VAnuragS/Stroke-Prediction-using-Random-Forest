# Stroke Prediction using Random Forest

This project presents a streamlined machine learning pipeline for predicting the likelihood of stroke in patients using structured health data. The approach combines comprehensive preprocessing, rigorous class balancing, and a Random Forest classifier optimized for exceptional predictive performance.

---

## Overview

The notebook implements a complete workflow for binary stroke classification, from raw data to final evaluation. Emphasis is placed on interpretability, data quality, and metric-driven validation. A Random Forest model is used for its balance of accuracy and explainability in medical contexts.

---

## Notebook Contents

- Data Loading and Initial Exploration  
- Missing Value Handling  
- Categorical and Numerical Feature Encoding  
- Class Imbalance Correction using SMOTE  
- Correlation and Feature Importance Analysis  
- **Model Training: Random Forest Classifier**
- Evaluation with Accuracy, Precision, Recall, F1, and AUC  
- Final Prediction and Interpretation

---

## Dataset Description

The dataset consists of anonymized health records with the following attributes:

- `age`: Age of the patient  
- `hypertension`: Binary indicator of hypertension  
- `heart_disease`: Binary indicator of heart disease  
- `ever_married`: Marital status  
- `work_type`: Type of employment  
- `Residence_type`: Urban or rural  
- `avg_glucose_level`: Average glucose level in blood  
- `bmi`: Body Mass Index  
- `smoking_status`: Smoking history  
- `stroke`: Target variable (1 = stroke occurred)

Source: [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset)

---

## Approach Summary

**1. Data Preprocessing**  
- Imputed missing BMI values using statistical methods  
- Removed outliers and inconsistencies  
- Applied one-hot encoding to multi-class categorical features

**2. Class Imbalance Handling**  
- Stroke occurrence is rare (~5% of cases)  
- Used SMOTE (Synthetic Minority Oversampling Technique) to balance the dataset

**3. Feature Engineering**  
- Removed irrelevant or highly correlated features  
- Ranked features using Random Forest feature importance

**4. Model Development**  
- Trained and tuned a Random Forest classifier for balanced performance across both classes  
- Model selection based on validation F1-Score and ROC-AUC

**5. Evaluation**  
- Assessed performance with accuracy, precision, recall, F1-score, and ROC-AUC  
- Analyzed confusion matrix with focus on minimizing false negatives

---

## Performance Metrics

**Classification Report:**

- **Accuracy:** 0.99  
- **Precision (Stroke):** 1.00  
- **Recall (Stroke):** 0.97  
- **F1-Score (Stroke):** 0.99  
- **ROC-AUC:** 0.99  

**Confusion Matrix:**

| Actual / Predicted | No Stroke | Stroke |
|--------------------|-----------|--------|
| No Stroke          | 500       | 1      |
| Stroke             | 3         | 96     |

---

## Conclusion

- End-to-end implementation in a single Jupyter Notebook  
- Achieved 99% accuracy using a Random Forest classifier with SMOTE for class balancing  
