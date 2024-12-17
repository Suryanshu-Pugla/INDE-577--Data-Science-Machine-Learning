# **Random Forest Classifier for Heart Disease Prediction**

## **Project Overview**
This project uses the **Random Forest Classifier** to predict the presence of heart disease based on patient medical attributes. The dataset contains health-related measurements such as cholesterol level, chest pain type, and maximum heart rate. The goal is to build an accurate and interpretable model to classify patients as having heart disease or not.

---

## **Dataset Overview**

### **Heart Disease Dataset**
- **Source**: [Public Heart Disease Dataset](https://github.com/plotly/datasets)
- **Description**: The dataset includes medical attributes of patients to predict the binary target variable `target`:
   - `0`: No Heart Disease.
   - `1`: Heart Disease.
- **Number of Samples**: 303
- **Features**:
   - `age`: Age of the patient.
   - `sex`: Gender (0 = female, 1 = male).
   - `cp`: Chest pain type (categorical: 0-3).
   - `trestbps`: Resting blood pressure (in mm Hg).
   - `chol`: Serum cholesterol (in mg/dl).
   - `fbs`: Fasting blood sugar (> 120 mg/dl, 1 = true, 0 = false).
   - `restecg`: Resting electrocardiographic results.
   - `thalach`: Maximum heart rate achieved.
   - `exang`: Exercise-induced angina (1 = yes, 0 = no).
   - `oldpeak`: ST depression induced by exercise relative to rest.
   - `slope`: Slope of the peak exercise ST segment.
   - `ca`: Number of major vessels colored by fluoroscopy (0-4).
   - `thal`: Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect).
   - `target`: The binary target variable (0 = no heart disease, 1 = heart disease).

---

## **Steps in the Project**

### **1. Load and Explore the Dataset**
- Load the dataset into a pandas DataFrame.
- Analyze the first few rows and check for missing values.

### **2. Data Preprocessing**
- Identify missing values (if any).
- Separate the features (`X`) and the target (`y`).
- Split the dataset into **training (80%)** and **testing (20%)** subsets using `train_test_split`.

### **3. Train the Random Forest Classifier**
- Build a **Random Forest Classifier** using scikit-learn:
   - **n_estimators**: 100 decision trees.
   - **max_depth**: 5 (limits tree depth to prevent overfitting).
   - **random_state**: Ensures reproducibility.

### **4. Model Evaluation**
The model is evaluated using the following metrics:

#### **Accuracy**
Measures the percentage of correct predictions:
$$
Accuracy = \frac{TP + TN}{TP + TN + FP + FN}
$$
Where:
- TP = True Positives, TN = True Negatives
- FP = False Positives, FN = False Negatives

#### **Confusion Matrix**
A table showing true/false predictions for both classes:
```
[[TN  FP]
 [FN  TP]]
```

#### **Classification Report**
Includes precision, recall, and F1-score for each class:
```
              precision    recall  f1-score   support

           0       0.83      0.86      0.85        29
           1       0.87      0.84      0.85        32

    accuracy                           0.85        61
   macro avg       0.85      0.85      0.85        61
weighted avg       0.85      0.85      0.85        61
```

---

### **5. Feature Importance**
The importance of each feature in predicting heart disease is computed and visualized:
- **Most Important Features**:
   - `thalach`: Maximum heart rate achieved.
   - `cp`: Chest pain type.
   - `ca`: Number of major vessels.

---

## **Dependencies**
Ensure the following Python libraries are installed:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## **How to Run the Project**
1. Copy the project code into a Python file or Jupyter Notebook.
2. Install the required dependencies using the command above.
3. Run the script.

**Output**:
- Model accuracy, confusion matrix, and classification report.
- Feature importance bar chart.

---

## **Results**
The Random Forest model achieves the following results on the Heart Disease Dataset:
- **Model Accuracy**: ~85%
- **Confusion Matrix**:
```
[[25  4]
 [ 5 27]]
```
- **Classification Report**:
```
              precision    recall  f1-score   support

           0       0.83      0.86      0.85        29
           1       0.87      0.84      0.85        32

    accuracy                           0.85        61
   macro avg       0.85      0.85      0.85        61
weighted avg       0.85      0.85      0.85        61
```

**Feature Importance Visualization**:
Features like `thalach` (maximum heart rate achieved) and `cp` (chest pain type) are the most important predictors.

---

## **Key Insights**
1. **Accuracy**: The Random Forest Classifier achieved an accuracy of **85%** on the test dataset.
2. **Feature Importance**:
   - `thalach` (maximum heart rate) and `cp` (chest pain type) play significant roles in heart disease prediction.
3. **Interpretability**: Random Forest provides a robust and interpretable method for understanding which features contribute most to predictions.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Use `GridSearchCV` to optimize parameters such as `n_estimators` and `max_depth`.
2. **Handling Imbalanced Data**:
   - Use SMOTE or class weights to handle any imbalance in the dataset.
3. **Model Comparison**:
   - Compare Random Forest with other models like **Logistic Regression**, **SVM**, or **Gradient Boosting**.
4. **Feature Engineering**:
   - Derive new features to improve predictive performance.

---

## **Conclusion**
The Random Forest Classifier effectively predicts heart disease based on medical attributes. With robust evaluation metrics and interpretable feature importance, the model demonstrates strong performance and provides valuable insights into key predictors of heart disease.

---

