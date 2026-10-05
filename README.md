# Diabetes Prediction Using Machine Learning

A machine-learning classification project for predicting diabetes using demographic, health, and lifestyle-related variables.

## Workflow

* Data inspection and cleaning
* Exploratory Data Analysis (EDA)
* Categorical encoding
* Train/test split
* Feature scaling
* Logistic Regression
* Decision Tree
* Random Forest
* Model evaluation
* Feature importance analysis

## Dataset

The original dataset contained **100,000 observations and 9 columns**.

After identifying and removing **3,854 duplicate rows**, the final dataset contained **96,146 observations**.

The target variable is `diabetes`, where:

* `0` = No Diabetes
* `1` = Diabetes

The dataset also contains an imbalanced class distribution, with diabetes cases representing approximately **8.8%** of the cleaned dataset.

## Models Used

### Logistic Regression

Used as a baseline classification model after applying feature scaling using `StandardScaler`.

### Decision Tree

A Decision Tree Classifier with `max_depth=6` was trained on the unscaled feature data.

### Random Forest

A Random Forest Classifier with **200 estimators** was used to evaluate ensemble-based classification performance and feature importance.

## Model Results

| Model               |   Accuracy |   Precision |     Recall |         F1 |    ROC-AUC |     PR-AUC |
| ------------------- | ---------: | ----------: | ---------: | ---------: | ---------: | ---------: |
| Logistic Regression |     95.96% |      86.92% |     63.86% |     73.62% |     95.99% |     81.74% |
| Decision Tree       | **97.16%** | **100.00%** |     67.81% | **80.82%** | **96.18%** |     82.48% |
| Random Forest       |     96.93% |      94.96% | **68.87%** |     79.84% |     96.11% | **85.57%** |

## Key Finding

The Random Forest feature-importance analysis showed that **HbA1c level (39.39%)** and **blood glucose level (32.75%)** were the two most important features in the model, followed by BMI and age.

## Project Outcome

The project compares different classification approaches and shows how model performance can vary depending on the evaluation metric. The Decision Tree achieved the highest F1-score and precision, while the Random Forest achieved the highest PR-AUC and recall among the evaluated models.

## Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Google Colab

## Important Note

This is an educational machine-learning project and is **not a clinical diagnostic system**. The predictions should not be used for medical diagnosis or treatment decisions.
