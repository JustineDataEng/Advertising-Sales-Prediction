
# Advertising Sales Prediction

This repository contains an **end-to-end machine learning analysis** to predict product sales based on advertising expenditures across various media channels.

The goal of this project is to determine the relationship between advertising budgets and resulting sales. Using the `advertising.csv` dataset, the notebook explores how money allocated to **TV, Radio, and Newspaper** impacts total unit sales.  

This notebook represents a complete data science workflow, from **Exploratory Data Analysis (EDA)** to advanced **regression modeling and evaluation**.

---

## Workflow

### 1. Exploratory Data Analysis (EDA)
- **Correlation Analysis:** Computed the correlation matrix to identify which advertising medium has the strongest impact on sales (TV shows the highest correlation).  
- **Data Visualization:** Created pair plots and scatter plots using Seaborn to visualize linearity and relationships between features.

### 2. Data Preprocessing
- **Feature Scaling:** Applied `StandardScaler` to normalize features for better model convergence.  
- **Train-Test Split:** Divided the data into training (80%) and testing (20%) sets for model validation.  
- **Polynomial Transformation:** Used `PolynomialFeatures` (degree 2) to capture non-linear interactions between advertising channels.

### 3. Machine Learning Models
Tested several regression algorithms:  
- **Linear Regression:** Established a baseline model  
- **Polynomial Regression:** Captured non-linear trends and improved accuracy  
- **Lasso Regression:** Applied L1 regularization to prevent overfitting; hyperparameters tuned with `GridSearchCV`  
- **K-Neighbors Regressor:** Explored a non-parametric approach to capture local patterns  

---

## Model Performance

| Model                  | Training MAE | Testing MAE | R² Score (Test) |
|------------------------|-------------|------------|----------------|
| Linear Regression      | 1.234       | 1.275      | 0.906         |
| Polynomial Regression  | 1.057       | 0.903      | 0.941 ✅       |
| Lasso Regression       | 1.235       | 1.275      | 0.906         |
| KNN Regressor          | 0.000       | 1.308      | 0.893         |

> **Note:** The Polynomial Regression model achieved the lowest Testing MAE, making it the most effective at capturing the complexities of the advertising dataset.

---

## Tools & Libraries Used

- **Python** – Core programming language  
- **Pandas & NumPy** – Data manipulation and numerical operations  
- **Matplotlib & Seaborn** – Statistical data visualization  
- **Scikit-learn** – Model building, preprocessing, and performance metrics  

---

## Conclusion

This project was developed as part of a **learning journey in Data Science and Engineering**, focusing on regression analysis, feature engineering, and model optimization. It demonstrates how machine learning can provide actionable insights for advertising budget allocation.


