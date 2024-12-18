# **Decision Tree Classifier for Banknote Authentication**
<img src="banknote-authetication.webp" alt="resized" width="50%">


## **Project Overview**
This project demonstrates the use of a **Decision Tree Classifier** to predict whether a banknote is **genuine** or **forged** based on numerical features extracted from images. The model is implemented using the **scikit-learn library** and evaluated on the **Banknote Authentication Dataset**.

The project includes model training, evaluation, and visualization of the decision tree to understand the feature-based splits.

---

## **Dataset Overview**

### **Banknote Authentication Dataset**
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/banknote+authentication).
- **Description**: The dataset contains numerical features extracted from **Wavelet Transformed Images** of banknotes. It is used to classify the banknotes as **genuine** or **forged**.
- **Number of Samples**: 1,372
- **Features**:
   - **Variance**: Variance of the wavelet transformed image.
   - **Skewness**: Skewness of the wavelet transformed image.
   - **Kurtosis**: Kurtosis of the wavelet transformed image.
   - **Entropy**: Entropy of the image.
- **Target**:
   - `0`: Forged Banknote.
   - `1`: Genuine Banknote.

---

## **Steps in the Project**

### **1. Data Loading**
- The dataset is loaded from the UCI Machine Learning Repository into a pandas DataFrame.
- The feature columns and target variable are separated for model training.

### **2. Data Splitting**
- The dataset is split into **80% training** and **20% testing** subsets using scikit-learn's `train_test_split`.

### **3. Train the Decision Tree Classifier**
- A **Decision Tree Classifier** is trained using the `DecisionTreeClassifier` class from scikit-learn.
- **Parameters**:
   - `criterion='gini'`: Gini Impurity is used to measure split quality.
   - `max_depth=5`: The maximum depth of the tree is limited to prevent overfitting.

### **4. Model Prediction**
- The trained model is used to predict class labels (0 or 1) for the test dataset.

### **5. Model Evaluation**
- The model is evaluated using the following metrics:
   - **Accuracy**: Measures the overall performance.
   - **Confusion Matrix**: Analyzes true/false positives and negatives.
   - **Classification Report**: Provides precision, recall, and F1-score.

### **6. Visualization of the Decision Tree**
- The decision tree is visualized using scikit-learn's `plot_tree` function.
- Splits are displayed along with feature names and class labels.

---

## **Code Dependencies**
The following libraries are required to run the project:

```bash
pip install pandas scikit-learn matplotlib
```

---

## **How to Run the Project**
1. Copy the project code into a Python file (e.g., `decision_tree_banknote.py`) or Jupyter Notebook.
2. Install the required dependencies using the above command.
3. Run the script.
4. Ensure the Wholesale Customers Dataset is in the working directory or update the file path in the script.

**Output**:
- Model accuracy, confusion matrix, classification report, and decision tree visualization.

---

## **Results**
The decision tree classifier achieves high accuracy on the Banknote Authentication Dataset:

- **Accuracy**: ~97%

**Confusion Matrix**:
```
[[148   0]
 [  9 118]]
```

**Classification Report**:
```
               precision    recall  f1-score   support

           0       0.94      1.00      0.97       148
           1       1.00      0.93      0.96       127

    accuracy                           0.97       275
   macro avg       0.97      0.96      0.97       275
```

---

## **Key Insights**
1. **High Accuracy**: The Decision Tree Classifier achieved an accuracy of ~96%.
2. **Feature Importance**: Features like **Variance** and **Skewness** play significant roles in differentiating between genuine and forged banknotes.
3. **Tree Visualization**: Visualizing the tree helps understand the decision boundaries and splitting logic based on the features.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Use GridSearchCV to optimize parameters like `max_depth` and `min_samples_split`.
2. **Feature Importance Analysis**:
   - Evaluate which features contribute the most to the model's predictions.
3. **Ensemble Methods**:
   - Use **Random Forest** or **Gradient Boosting** to improve performance further.

---

## **Conclusion**
This project showcases the power of Decision Trees for binary classification tasks like **Banknote Authentication**. With simple preprocessing and parameter tuning, the model achieves high accuracy and provides interpretable insights into the classification process.

---


