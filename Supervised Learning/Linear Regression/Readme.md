### Linear Regression on Advertising Dataset**

< img src="https://github.com/user-attachments/assets/c9f347ec-4930-46b0-9116-0ef73ea02b84)" alt="Resized Image" width="60%">

### **Project Overview**
This project demonstrates the use of **linear regression** to predict sales based on advertising expenditure. The dataset contains information on advertising budgets across three channels—TV, radio, and newspaper—and their impact on sales. The goal is to understand the relationships between advertising spending and sales and to build a predictive model.

---

### **Dataset Overview**

#### **Advertising Dataset**
- **Source**: A hypothetical dataset often used in regression analysis.
- **Description**: The dataset includes information about advertising budgets for TV, radio, and newspaper campaigns, and their corresponding sales figures.
- **Attributes**:
  - **TV**: Advertising budget spent on TV (in thousands of dollars).
  - **Radio**: Advertising budget spent on radio (in thousands of dollars).
  - **Newspaper**: Advertising budget spent on newspapers (in thousands of dollars).
  - **Sales**: Sales of a product (in thousands of units).

---

### **Steps in the Project**

#### **1. Data Preprocessing**
- Loaded the dataset and explored its structure.
- Checked for missing or anomalous values.
- Visualized relationships between features (TV, radio, newspaper) and the target variable (sales).

#### **2. Exploratory Data Analysis (EDA)**
- Generated scatter plots to visualize the correlation between each advertising medium and sales.
- Calculated correlation coefficients to quantify relationships between features and the target variable.

#### **3. Model Training**
- Implemented a **linear regression model** using scikit-learn’s `LinearRegression` class.
- Split the dataset into training (80%) and testing (20%) subsets.
- Trained the model on the training dataset.

#### **4. Model Evaluation**
- Evaluated the model using metrics such as:
  - **Mean Squared Error (MSE)**.
  - **Mean Absolute Error (MAE)**.
  - **R-squared Score (R²)**.
- Visualized the actual vs. predicted sales values.

" img src="https://github.com/user-attachments/assets/5caa6633-de9d-4c0c-ab5e-01b142f06d8b" alt="Resized Image" width="80%"> 


### **Results**

#### **Key Metrics**
- **Mean Squared Error (MSE)**: 4.08
- **Mean Absolute Error (MAE)**: 1.56
- **R-squared Score (R²)**: 0.99

The high R² value indicates that the model explains 99% of the variance in sales, demonstrating an excellent fit to the data.

---

### **Graphs and Visualizations**

#### **1. Correlation Heatmap**
- A heatmap was generated to visualize the correlation between features and the target variable. TV and radio showed a strong positive correlation with sales, while the newspaper had a weaker correlation.

#### **2. Actual vs. Predicted Sales**
- The scatter plot of actual vs. predicted sales demonstrates a strong alignment, indicating that the model predictions are close to the actual values.

---

### **Key Insights**

1. **TV Advertising**:
   - TV advertising has the strongest positive correlation with sales.
   - Increasing TV budget significantly impacts sales.

2. **Radio Advertising**:
   - Radio advertising also positively correlates with sales, though its impact is slightly less than TV.

3. **Newspaper Advertising**:
   - Newspaper advertising shows the weakest correlation with sales, suggesting it may be less effective for this product.

4. **Overall Fit**:
   - The high R² score indicates that the model fits the data very well, making it reliable for predicting sales based on advertising budgets.

---

### **How to Run the Project**

#### **1. Clone the Repository**
```bash
git clone <repository_link>
cd linear-regression-advertising
```

#### **2. Install Dependencies**
Ensure Python is installed along with the required libraries:
```bash
pip install numpy pandas matplotlib scikit-learn
```

#### **3. Run the Script**
Execute the script to preprocess the data, train the model, and view results:
```bash
python linear_regression_advertising.py
```

---

### **Next Steps**

1. **Feature Engineering**:
   - Explore polynomial terms or interaction effects (e.g., TV * Radio).

2. **Regularization**:
   - Apply techniques like Ridge or Lasso regression to prevent overfitting if additional features are added.

3. **Cross-Validation**:
   - Perform k-fold cross-validation to validate the robustness of the model.

4. **Comparison with Other Models**:
   - Compare the performance of linear regression with non-linear models such as decision trees or random forests.

---


