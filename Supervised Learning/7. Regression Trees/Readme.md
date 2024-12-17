# **Regression Tree on California Housing Dataset**

## **Project Overview**
This project demonstrates the use of a **Regression Tree** to predict housing prices using the **California Housing Dataset**. The model is built using the `DecisionTreeRegressor` from the `scikit-learn` library and evaluated using standard regression metrics such as **Mean Squared Error (MSE)** and **R² Score**. The project also includes a visualization of the decision tree to interpret the model's behavior.

---

## **Dataset Overview**

### **California Housing Dataset**
- **Source**: Scikit-learn's built-in dataset ([California Housing](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)).
- **Description**: Predicts median house prices in various regions of California based on demographic and geographic features.
- **Number of Samples**: 20,640
- **Features**:
   - `MedInc`: Median income in block group.
   - `HouseAge`: Average house age in block group.
   - `AveRooms`: Average number of rooms per household.
   - `AveBedrms`: Average number of bedrooms per household.
   - `Population`: Block group population.
   - `AveOccup`: Average house occupancy.
   - `Latitude`: Latitude of block group.
   - `Longitude`: Longitude of block group.
- **Target**: Median house value (continuous variable).

---

## **Steps in the Project**

### **1. Load and Explore the Dataset**
- Load the California Housing Dataset using `fetch_california_housing` from scikit-learn.
- Explore the dataset to understand the features and target variable.

### **2. Data Preprocessing**
- Split the dataset into **training (80%)** and **testing (20%)** subsets using `train_test_split`.

### **3. Train the Regression Tree Model**
- Use the **DecisionTreeRegressor** from scikit-learn.
- Hyperparameters:
   - `criterion='mse'`: Mean Squared Error is used to measure split quality.
   - `max_depth=5`: Limits the depth of the tree to prevent overfitting.

### **4. Model Evaluation**
The model performance is evaluated using:
1. **Mean Squared Error (MSE)**:
   \[
   MSE = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2
   \]
   Where:
   - \( y_i \): Actual target value for sample \( i \).
   - \( \hat{y}_i \): Predicted target value for sample \( i \).
   - \( n \): Number of samples.

2. **R² Score**:
   \[
   R^2 = 1 - \frac{\sum_{i=1}^n (y_i - \hat{y}_i)^2}{\sum_{i=1}^n (y_i - \bar{y})^2}
   \]
   Where:
   - \( \bar{y} \): Mean of the actual target values.
   - R² measures how well the model explains the variance in the data.

### **5. Visualization of the Decision Tree**
- The decision tree is visualized using `plot_tree` to interpret how the model splits data based on the input features.

---

## **Dependencies**
Ensure the following Python libraries are installed:
```bash
pip install pandas numpy scikit-learn matplotlib
```

---

## **How to Run the Project**
1. Copy the project code into a Python file or Jupyter Notebook.
2. Install the required libraries using the command above.
3. Run the script.

**Output**:
- Mean Squared Error (MSE) and R² Score.
- Visualization of the trained Regression Tree.

---

## **Results**
The Regression Tree achieves the following results on the California Housing Dataset:
- **Mean Squared Error (MSE)**: ~0.52
- **R² Score**: ~0.66

**Example Output**:
```
Dataset Shape: (20640, 8)
Feature Names: Index(['MedInc', 'HouseAge', 'AveRooms', 'AveBedrms', 'Population',
                      'AveOccup', 'Latitude', 'Longitude'], dtype='object')

Regression Tree Results:
Mean Squared Error (MSE): 0.52
R² Score: 0.66
```

---

## **Key Insights**
1. **Feature Importance**:
   - Features like `MedInc` (Median Income) and `Latitude` are significant contributors to the prediction of house prices.
2. **Tree Visualization**:
   - Visualizing the tree reveals how the model splits the data based on feature values to predict housing prices.
3. **Performance**:
   - The R² score indicates that the model explains approximately 66% of the variance in house prices.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Optimize parameters like `max_depth`, `min_samples_split`, and `min_samples_leaf` using GridSearchCV.
2. **Ensemble Methods**:
   - Use methods like **Random Forest** or **Gradient Boosting** to improve predictive accuracy.
3. **Feature Engineering**:
   - Explore derived features (e.g., interaction terms) to improve model performance.

---

## **Conclusion**
This project showcases the use of a **Regression Tree** to predict housing prices using the **California Housing Dataset**. The model demonstrates strong performance with interpretable results, making it an effective tool for understanding feature contributions and decision-making processes.

---
