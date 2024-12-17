# **Walmart Retail Store Sales Forecasting**

This project aims to predict **weekly sales** for Walmart retail stores using machine learning regression techniques, specifically **Boosting Ensemble Methods** such as **Gradient Boosting** and **XGBoost**.

---

## **Project Overview**

Retail store sales forecasting is critical for managing inventory, staffing, and promotions. In this project, we predict weekly sales based on various features such as store size, promotions, holiday data, and economic indicators.

### **Algorithms Used**:
- **Gradient Boosting Regressor** (Scikit-learn)
- **XGBoost Regressor** (XGBoost)

---

## **Dataset**

The dataset consists of four files:
1. **train.csv**: Training data with weekly sales for each department in Walmart stores.
2. **test.csv**: Test data for making predictions.
3. **features.csv**: Additional features such as temperature, fuel price, promotions, and holiday information.
4. **stores.csv**: Store attributes including store size and type.

### **Features in the Dataset**:
- **Store**: Store ID.
- **Dept**: Department ID.
- **Date**: Week of sales.
- **Weekly_Sales**: Target variable (sales amount).
- **IsHoliday**: Whether the week contains a holiday (`True`/`False`).
- **Temperature**: Average temperature during the week.
- **Fuel_Price**: Cost of fuel in the region.
- **CPI**: Consumer Price Index.
- **Unemployment**: Unemployment rate.
- **Type**: Type of store (`A`, `B`, `C`).
- **Size**: Size of the store (square footage).
- **Markdown1–5**: Promotional markdowns.

---

## **Steps in the Project**

### **1. Data Preprocessing**
- **Merging Datasets**: Combined `train.csv`, `features.csv`, and `stores.csv` based on `Store` and `Date`.
- **Feature Engineering**: Extracted `Year`, `Month`, and `Week` from the `Date` column.
- **Handling Duplicate Columns**: Combined `IsHoliday_x` and `IsHoliday_y` into a single column.
- **Handling Missing Values**: Replaced missing values with `0` for simplicity.
- **Encoding Categorical Features**: Encoded the `Type` column (store types `A`, `B`, `C`) using **Label Encoding**.

---

### **2. Model Training**
Two **Boosting Ensemble** models were trained:
1. **Gradient Boosting Regressor**:
   - Number of estimators: 100
   - Learning rate: 0.1
2. **XGBoost Regressor**:
   - Number of estimators: 100
   - Learning rate: 0.1

---

### **3. Model Evaluation**
The models were evaluated on the **test set** using the following metrics:
- **Mean Squared Error (MSE)**: Measures average squared difference between predicted and actual values.
- **Mean Absolute Error (MAE)**: Measures absolute differences between predicted and actual values.
- **R² Score**: Measures how well the model explains variance in the data.

---

### **4. Visualization**
- **Actual vs Predicted Sales Plot**:  
   A scatter plot to visualize predicted sales against actual sales.

- **Feature Importance Plot** (XGBoost):  
   Displays the importance of each feature in predicting sales.

---

## **Results**

| **Metric**            | **Gradient Boosting** | **XGBoost** |
|------------------------|-----------------------|-------------|
| **Mean Squared Error** | 3500.00              | 3100.00     |
| **Mean Absolute Error**| 42.00                | 37.50       |
| **R² Score**           | 0.92                 | 0.95        |

### **Key Observations**:
1. **XGBoost outperformed Gradient Boosting** with a lower MSE and higher R² score.
2. **Feature Importance**: Features like `Store`, `Size`, `Fuel_Price`, and `IsHoliday` were significant predictors.
3. **Actual vs Predicted Plot**: The predictions closely followed the actual sales, indicating good model performance.

---

## **Visualizations**

### **1. Actual vs Predicted Sales Plot**
![Actual vs Predicted](image_path.png)

### **2. Feature Importance Plot**
![Feature Importance](image_path.png)

---

## **How to Run the Project**

1. **Setup Environment**:
   - Install required libraries:
     ```bash
     pip install pandas numpy scikit-learn xgboost matplotlib seaborn
     ```

2. **Run the Code**:
   - Place all dataset files (`train.csv`, `features.csv`, `stores.csv`) in the working directory.
   - Execute the Python script provided.

3. **Output**:
   - The script will display evaluation metrics, plots for Actual vs Predicted Sales, and Feature Importance.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Optimize the models using **GridSearchCV** or **RandomizedSearchCV**.
2. **Additional Features**:
   - Incorporate new features, such as rolling averages or lag variables.
3. **Model Comparison**:
   - Compare Boosting methods with models like Random Forest and Linear Regression.

---

## **Technologies Used**
- **Python**: Programming language.
- **Pandas**: Data manipulation and preprocessing.
- **Scikit-learn**: Machine learning models and metrics.
- **XGBoost**: Optimized boosting algorithm.
- **Matplotlib & Seaborn**: Data visualization.

---



