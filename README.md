# Capstone-Project-1
#  Property Price Prediction using Machine Learning

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?style=for-the-badge&logo=numpy)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-teal?style=for-the-badge)

</p>

---

#  Project Overview

This project predicts residential property prices using Machine Learning techniques. The complete workflow includes data collection, preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and deployment.

Three regression algorithms were developed and compared to identify the best-performing model for accurate property price prediction.

---

#  Objectives

- Collect and clean real estate property data.
- Handle missing values using appropriate imputation techniques.
- Separate ordinal and nominal categorical variables.
- Apply feature encoding, scaling, and PCA.
- Perform exploratory data analysis (EDA).
- Build and compare multiple regression models.
- Evaluate models using R² Score, MAE, and RMSE.
- Save the final trained model for deployment.

---

#  Dataset Information

| Attribute | Details |
|------------|---------|
| Dataset | Property_data.csv |
| Domain | Real Estate |
| Problem Type | Regression |
| Target Variable | PropPrice |

---

#  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

#  Project Workflow

```text
Data Collection
       │
       ▼
Data Cleaning
       │
       ▼
Missing Value Treatment
       │
       ▼
Exploratory Data Analysis
       │
       ▼
Feature Engineering
       │
       ▼
Encoding
       │
       ▼
Feature Scaling
       │
       ▼
Principal Component Analysis (PCA)
       │
       ▼
Train-Test Split
       │
       ▼
Model Training
       │
       ▼
Model Evaluation
       │
       ▼
Model Deployment (.pkl)
```

---

#  Exploratory Data Analysis (EDA)

## 1. Missing Values Analysis

<img width="700" height="400" alt="Screenshot 2026-06-27 154017" src="https://github.com/user-attachments/assets/fd77dda4-6fab-41a9-81a3-c87583b8c780" />


**Observation**

- Missing values were identified in both numerical and categorical features.
- Median imputation was applied for numerical features.
- Mode imputation was applied for categorical features.
- Only the Property ID column was excluded from modelling.

---

## 2. Property Price Distribution

<img width="700" height="400" alt="Distribution_Property_Price" src="https://github.com/user-attachments/assets/cbbcd9ce-1b31-4960-9239-ecffc5541d2f" />


**Observation**

- Property prices are slightly right-skewed.
- Most properties fall within a moderate price range.

---

## 3. Living Area vs Property Price

<img width="700" height="400" alt="LivArea Vs PrpPrice" src="https://github.com/user-attachments/assets/8f7d4f31-c478-4f76-b5af-e989d716427a" />


**Observation**

- Living area has a positive relationship with property price.
- Larger properties generally have higher selling prices.

---

## 4. Overall Quality vs Property Price

<img width="700" height="400" alt="OverallQual vs PropPrice" src="https://github.com/user-attachments/assets/def895d8-b000-4d9a-8508-040ccf831b33" />


**Observation**

- Better construction quality is associated with higher property prices.
- Overall Quality is one of the strongest predictors.

---

## 5. Correlation Heatmap

<img width="800" height="1000" alt="correlation_heatmap" src="https://github.com/user-attachments/assets/e14e6a9f-094a-4f8b-aea7-4180733e0a3a" />


**Observation**

- The heatmap shows the relationships among numerical variables.
- Highly correlated features were identified and used during feature selection.

---

#  Data Preprocessing

The following preprocessing techniques were applied:

- Duplicate Record Removal
- Missing Value Treatment
- Ordinal Encoding
- One-Hot Encoding
- StandardScaler
- Principal Component Analysis (PCA)

---

#  Feature Engineering

Additional features were created to improve model performance:

- HouseAge
- TotalBathrooms

These engineered features improved the predictive capability of the models.

---

#  Machine Learning Models

The following regression algorithms were implemented:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

---

#  Model Performance

| Model | R² Score | MAE | RMSE |
|--------|---------:|----:|-----:|
| Linear Regression | **0.758544209182954** | **19062.84736342228** | **33147.576518673246** |
| Decision Tree Regressor | **0.6459466253356637** | **26823.76712328767** | **40139.07298244954** |
| Random Forest Regressor | **0.8139482307060701** | **16890.09152475941** | **29097.111029948443** |

---

## Model Performance Comparison

<img width="700" height="400" alt="model_comparison" src="https://github.com/user-attachments/assets/6beecad2-27d2-43f3-be60-728d53e70cb7" />


**Observation**

Random Forest achieved the highest R² score and was selected as the final model for property price prediction.

---

# Model Deployment

The final trained model was saved using Joblib.

```python
joblib.dump(best_model, "final_property_price_model.pkl")
```

The saved model can be loaded later without retraining and used to predict property prices for new data.

---

# Project Structure

```text
Property-Price-Prediction/
│
├── Property_Price_Capstone.ipynb
├── Property_data.csv
├── Property_Metadata.xlsx
├── final_property_price_model.pkl
├── README.md
├── requirements.txt
│
├── images/
│   ├── missing_values.png
│   ├── price_distribution.png
│   ├── living_area_vs_price.png
│   ├── overall_quality_vs_price.png
│   ├── correlation_heatmap.png
│   └── model_comparison.png
```

---

# How to Run

Clone the repository:

```bash
git clone https://github.com/your-username/Property-Price-Prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Run all notebook cells sequentially.

---

# Future Improvements

- Hyperparameter Tuning
- Cross Validation
- XGBoost Regressor
- Streamlit Web Application
- Cloud Deployment

---

# References

- Scikit-learn Documentation
- Pandas Documentation
- NumPy Documentation
- Matplotlib Documentation
- Seaborn Documentation
- Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow by Aurélien Géron

---

# Author:

## Ajay Kumar Sahu

**Machine Learning | Data Science | Python | SQL | Power BI**

