
# Machine Learning Project — Technical Summary

**Project:** Heavy Equipment Selling Price Prediction  
**Author:** Renee Noronha  
**Institution:** IIT Madras | BS in Data Science and Applications  
**Tools:** Python, Pandas, NumPy, Scikit-learn, LightGBM, CatBoost

---

## Project Objective

The objective of this project was to develop a machine learning model capable of predicting heavy equipment selling prices using historical transaction data.

I worked with approximately **138,701 training observations**, exploring how equipment characteristics, manufacturing year, operational hours, transaction timing, and other features relate to selling prices.

My focus was on understanding the dataset, engineering useful features, comparing machine learning algorithms, and improving predictive accuracy through experimentation.

## My Approach

### 1. Understanding and Preparing the Data

I began by exploring the dataset to understand its structure, feature distributions, missing values, and potential relationships with the target variable.

I then cleaned and prepared the data by handling missing values, processing categorical features, and creating consistent training and validation datasets.

### 2. Feature Engineering

I developed additional features to capture information that was not directly represented in the original dataset, including:

- **Machine age:** The age of equipment at the time of sale.
- **Operational hours per year:** A measure of equipment usage relative to its age.
- **Transaction date features:** Year, month, and quarter.
- **Missing-value indicators:** Features capturing patterns in incomplete data.

These features helped represent equipment characteristics in ways that machine learning models could use more effectively.

### 3. Model Development and Evaluation

I trained and compared several regression models:

- Ridge Regression
- Random Forest
- LightGBM
- CatBoost

I evaluated the models using **Root Mean Squared Logarithmic Error (RMSLE)**, compared training and validation performance, and experimented with hyperparameter tuning and prediction blending.

## Results and Key Findings

| Metric | Result |
|---|---|
| Training observations | 138,701 |
| LightGBM validation RMSLE | 0.2003 |
| Blended model validation RMSLE | **0.1956** |
| Reported Kaggle submission RMSLE | **0.19196** |

**My key findings:**

1. **Feature engineering matters.** Machine age, transaction timing, and equipment characteristics provided useful predictive information.

2. **More complex models are not automatically better.** Comparing different algorithms helped me understand their strengths, limitations, and generalisation performance.

3. **Overfitting needs careful attention.** Differences between training and validation performance highlighted the importance of evaluating models on unseen data.

4. **Model blending improved performance.** Combining 60% LightGBM and 40% CatBoost predictions achieved a validation RMSLE of approximately 0.1956, improving on the individual LightGBM result of 0.2003.

## How I Would Improve It

If I were to approach this project again, I would dedicate more time to **exploratory data analysis and preprocessing** before moving into model development.

I would focus on understanding the relationships between features, investigating missing values and outliers, and identifying patterns that could influence selling prices.

This deeper understanding would help me make more informed feature engineering decisions, improve data quality, and potentially achieve better predictive performance.

## What I Learned

This project taught me that successful machine learning is not simply about selecting the most advanced algorithm.

It requires understanding the problem, asking the right questions about the data, making thoughtful preprocessing and feature engineering decisions, and evaluating results critically.

It strengthened my interest in applying machine learning to real-world problems where data can support better decisions.

