# Capstone-Project-1
# 🏠 Property Price Prediction using Machine Learning

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?style=for-the-badge&logo=numpy)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Visualization-teal?style=for-the-badge)

</p>

---

# 📖 Project Overview

This project predicts residential property prices using Machine Learning techniques. The complete workflow includes data collection, preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and deployment.

Three regression algorithms were developed and compared to identify the best-performing model for accurate property price prediction.

---

# 🎯 Objectives

- Collect and clean real estate property data.
- Handle missing values using appropriate imputation techniques.
- Separate ordinal and nominal categorical variables.
- Apply feature encoding, scaling, and PCA.
- Perform exploratory data analysis (EDA).
- Build and compare multiple regression models.
- Evaluate models using R² Score, MAE, and RMSE.
- Save the final trained model for deployment.

---

# 📂 Dataset Information

| Attribute | Details |
|------------|---------|
| Dataset | Property_data.csv |
| Domain | Real Estate |
| Problem Type | Regression |
| Target Variable | PropPrice |

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

# 🔄 Project Workflow

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

# 📊 Exploratory Data Analysis (EDA)

## 1. Missing Values Analysis

<img src="images/missing_values.png" width="800">

**Observation**

- Missing values were identified in both numerical and categorical features.
- Median imputation was applied for numerical features.
- Mode imputation was applied for categorical features.
- Only the Property ID column was excluded from modelling.

---

## 2. Property Price Distribution

<img src="images/price_distribution.png" width="800">

**Observation**

- Property prices are slightly right-skewed.
- Most properties fall within a moderate price range.

---

## 3. Living Area vs Property Price

<img src="images/living_area_vs_price.png" width="800">

**Observation**

- Living area has a positive relationship with property price.
- Larger properties generally have higher selling prices.

---

## 4. Overall Quality vs Property Price

<img src="images/overall_quality_vs_price.png" width="800">

**Observation**

- Better construction quality is associated with higher property prices.
- Overall Quality is one of the strongest predictors.

---

## 5. Correlation Heatmap

<img src="images/correlation_heatmap.png" width="800">

**Observation**

- The heatmap shows the relationships among numerical variables.
- Highly correlated features were identified and used during feature selection.

---

# ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

- Duplicate Record Removal
- Missing Value Treatment
- Ordinal Encoding
- One-Hot Encoding
- StandardScaler
- Principal Component Analysis (PCA)

---

# ⚡ Feature Engineering

Additional features were created to improve model performance:

- HouseAge
- TotalBathrooms

These engineered features improved the predictive capability of the models.

---

# 🤖 Machine Learning Models

The following regression algorithms were implemented:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

---

# 📈 Model Performance

| Model | R² Score | MAE | RMSE |
|--------|---------:|----:|-----:|
| Linear Regression | **Your Score** | **Your Score** | **Your Score** |
| Decision Tree Regressor | **Your Score** | **Your Score** | **Your Score** |
| Random Forest Regressor | **Your Score** | **Your Score** | **Your Score** |

---

## Model Performance Comparison

<img src="images/model_comparison.png" width="700">

**Observation**

Random Forest achieved the highest R² score and was selected as the final model for property price prediction.

---

# 💾 Model Deployment

The final trained model was saved using Joblib.

```python
joblib.dump(best_model, "final_property_price_model.pkl")
```

The saved model can be loaded later without retraining and used to predict property prices for new data.

---

# 📁 Project Structure

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

# 🚀 How to Run

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

# 💡 Future Improvements

- Hyperparameter Tuning
- Cross Validation
- XGBoost Regressor
- Streamlit Web Application
- Cloud Deployment

---

# 📚 References

- Scikit-learn Documentation
- Pandas Documentation
- NumPy Documentation
- Matplotlib Documentation
- Seaborn Documentation
- Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow by Aurélien Géron

---

# 👨‍💻 Author

## Ajay Kumar Sahu

**Machine Learning | Data Science | Python | SQL | Power BI**

⭐ If you found this project useful, consider giving it a star on GitHub.
