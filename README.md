
# Heavy Equipment Selling Price Prediction

### Machine Learning Practice Project | IIT Madras

**Author:** Renee Noronha  
**Degree:** BS in Data Science and Applications, IIT Madras  
**Domain:** Supervised Machine Learning | Regression  
**Tech Stack:** Python, Pandas, NumPy, Scikit-learn, LightGBM, CatBoost, Matplotlib

---

## Project Overview

This project focuses on predicting the selling prices of heavy equipment using historical transaction data and supervised machine learning.

The objective was to develop an accurate regression model by performing exploratory data analysis, preprocessing, feature engineering, model selection, hyperparameter tuning, and performance evaluation.

The project was completed as part of the Machine Learning Practice course at IIT Madras.

## Dataset

The dataset contains approximately **138,701 training observations**, with numerical and categorical variables describing heavy equipment characteristics and historical transactions.

Key challenges included:
- Missing and inconsistent data
- High-cardinality categorical variables
- Nonlinear relationships between equipment characteristics and prices
- Variation in equipment age, usage, and specifications

**Target variable:** `TargetValue`  
**Evaluation metric:** Root Mean Squared Logarithmic Error (RMSLE)

## Methodology

### 1. Exploratory Data Analysis

- Examined target price distributions and feature relationships.
- Investigated missing values and duplicate records.
- Analysed manufacturing year, equipment age, and operational hours.
- Explored relationships between equipment characteristics and selling prices.

### 2. Data Preprocessing

- Handled missing numerical and categorical values.
- Applied median imputation and categorical encoding.
- Used training-only fitting for preprocessing transformations to reduce data leakage.
- Prepared consistent training, validation, and test features.

### 3. Feature Engineering

Developed additional features to improve predictive performance, including:

- Machine age at the time of sale
- Operational hours per year
- Log-transformed operational hours
- Transaction year, month, and quarter
- Missing-value indicators
- Derived equipment characteristics

### 4. Model Development

Implemented and compared multiple regression algorithms:

| Model | Approach |
|---|---|
| Ridge Regression | Regularised linear baseline |
| Random Forest | Bagging-based tree ensemble |
| LightGBM | Gradient-boosted decision trees |
| CatBoost | Gradient boosting with categorical feature support |

Performed hyperparameter tuning and evaluated training and validation performance.

### 5. Model Evaluation

Used RMSLE to assess prediction quality.

Compared model performance, investigated overfitting, and evaluated weighted blending of LightGBM and CatBoost predictions.

## Results

| Metric | Result |
|---|---|
| Training observations | 138,701 |
| LightGBM validation RMSLE | 0.2003 |
| Reported Kaggle submission RMSLE | **0.19196** |
| Final modelling approach | LightGBM + CatBoost blend |

The final prediction blend combined **60% LightGBM and 40% CatBoost**.

The project demonstrated the importance of careful preprocessing, meaningful feature engineering, systematic model comparison, and validation-based decision-making.

## Key Technical Learnings

- Building end-to-end machine learning workflows for tabular data
- Engineering features using domain knowledge
- Handling missing values and categorical variables
- Comparing linear and ensemble regression methods
- Identifying overfitting and generalisation gaps
- Tuning hyperparameters and blending model predictions
- Evaluating predictive performance using RMSLE

## Limitations and Future Improvements

Potential improvements include:

- Testing chronological or grouped validation strategies
- Using an untouched holdout set for final model assessment
- Investigating repeated-equipment records and possible data leakage
- Refactoring notebook code into reusable Python modules
- Adding automated tests and reproducible dependency management
- Developing an inference API and model monitoring workflow

## Repository Contents

- **Jupyter Notebook (`.ipynb`)** — Data exploration, preprocessing, feature engineering, model development, evaluation, and prediction generation
- **README.md** — Project documentation and results

The notebook was developed in the Kaggle environment. The relevant dataset and dependencies are required to reproduce the experiments.

## About Me

I'm Renee Noronha, a Data Science undergraduate at IIT Madras with an interest in machine learning, predictive analytics, and real-world problem-solving.

Alongside my studies, I'm an endurance athlete. My experience in endurance sports has inspired my interest in applying data science and machine learning to athlete performance, training optimisation, and sports technology.

---

**Renee Noronha**  
BS Data Science and Applications | IIT Madras
