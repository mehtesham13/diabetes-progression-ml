# Predicting Diabetes Disease Progression with Linear Regression and XGBoost

## Project Overview

This project aims to predict the progression of diabetes in patients one year after a baseline assessment. By building and evaluating multiple machine learning models, the project identifies the most critical clinical features such as BMI and blood serum measurements that drive disease progression.

## Key Objectives

* **Feature Selection**: Identify the single best predictor and the optimal feature pairs for disease progression.


* **Model Comparison**: Compare the performance of standard Linear Regression against the XGBoost ensemble method.


* **Generalization Analysis**: Evaluate how training data size (20 to 200 samples) impacts model overfitting and validation accuracy.



## Methodology

The analysis was conducted through four main tasks:

1. **Single Feature Prediction**: Testing each of the 10 clinical features individually.


2. **Pairwise Prediction**: Exhaustive testing of all 45 unique feature combinations.


3. **Comprehensive Modeling**: Utilizing all 10 features (Age, Sex, BMI, BP, S1-S6) in a multi-variable model.


4. **Ensemble Implementation**: Implementing **XGBoost** to capture non-linear relationships and improve predictive power.



## Key Findings

### 1. The Power of BMI and S5

* **BMI** was identified as the strongest single predictor with a Mean Squared Error (MSE) of **3890.46**.


* Combining **BMI with S5** (blood serum) provided the most accurate pairwise model, reducing error by **17.6%** compared to BMI alone.


* In a full model, **S5** remains the strongest positive driver of progression (Coefficient: 68.48).



## 2. Linear Regression vs. XGBoost

[cite_start]XGBoost significantly outperformed Linear Regression across all test scenarios[cite: 161, 206].

| Scenario | Linear Regression (MSE) | XGBoost (MSE) | Improvement |
| :--- | :---: | :---: | :---: |
| Single Feature (BMI) | 3890 | 2983 | 23% |
| Feature Pair (BMI, S5) | 3205 | 1592 | 50% |
| **All Features** | 2859 | **73** | **97%** |
### 3. Impact of Training Data Size

The project highlighted the importance of dataset volume for model stability:

* **Extreme Overfitting**: Occurred with only 20 training samples, showing a massive gap between training and validation error.


* **Stability**: Model performance stabilized once the training set reached **100-200 samples**.



## Visualizations

The project includes several analytical plots to support the findings:

* **Regression Analysis**: Visualizing the linear relationship between BMI and progression.


* **3D Surface Plots**: Showing how BMI and S5 interact to predict outcomes.


* **Learning Curves**: Comparing training vs. validation MSE across different data sizes.


* **Feature Importance**: Ranking features based on their impact in the XGBoost model.



## Conclusion

While Linear Regression offers high interpretability, **XGBoost** provides a 97% improvement in accuracy when all features are available. The results confirm that combining physiological data (BMI) with clinical biomarkers (S5) is essential for accurate diabetes forecasting.

---

**Author**: Muhammad Ehtesham 
