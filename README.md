# Advertising Sales Prediction Project

This project investigates the relationship between advertising spend across three media channels—**TV, Radio, and Newspaper**—and the resulting **Sales**.  

The goal is to develop machine learning models that can:  
1. **Predict exact Sales figures** based on a given marketing budget (Regression).  


---

## Dataset

The project uses the `advertising.csv` dataset, containing 200 observations:  

- **TV:** Budget spent on TV advertising (in thousands of dollars)  
- **Radio:** Budget spent on Radio advertising  
- **Newspaper:** Budget spent on Newspaper advertising  
- **Sales:** Total units sold (Target Variable)  

---

## Tech Stack

- **Python** – Core programming  
- **Pandas & NumPy** – Data wrangling and numerical analysis  
- **Matplotlib & Seaborn** – Statistical visualizations (Heatmaps, Scatter plots)  
- **Scikit-Learn** – Model building, feature scaling, and evaluation  
- **XGBoost** – High-performance gradient boosting for regression  

---

## Project Structure

### Phase 1: Exploratory Data Analysis (EDA)
- Identified **TV** as the most significant driver of sales (correlation $r \approx 0.78$)  
- Found **Newspaper spend** had weak correlation with sales, suggesting potential budget inefficiency  
- Preprocessed data: handled missing values and applied **StandardScaler** for distance-based models like KNN and SVM  

### Phase 2: Regression (Predicting Unit Sales)
Tested multiple regression algorithms to find the most accurate predictor:  
- **Linear Regression:** Baseline model  
- **Polynomial Regression (Degree 2):** Captured non-linear trends, improved accuracy  
- **Lasso & Ridge:** Regularization to prevent overfitting  
- **XGBoost:** Best performance for complex patterns  

### Phase 3: Classification (Predicting "High Performance" Campaigns)
- Converted target into binary variable: `High_Performance` (1 if Sales > 15, else 0)  
- Models: **Logistic Regression** and **Support Vector Machines (SVM)**  
- Evaluation: **Confusion Matrices** and **ROC-AUC scores** to prioritize detection of high-value campaigns  

---

## Key Results

- **Best Models:** Polynomial Regression and XGBoost outperformed simple linear models by capturing interactions between TV and Radio spend  
- **Business Insight:** TV and Radio advertising should be prioritized; Newspaper budgets could be reallocated to higher-ROI channels  
- **Accuracy:** Final regression models achieved an **R² score > 0.90**  
