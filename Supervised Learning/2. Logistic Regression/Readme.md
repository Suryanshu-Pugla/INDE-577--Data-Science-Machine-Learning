### **Logistic Regression on Pima Indians Diabetes Dataset**

<img src="https://github.com/user-attachments/assets/a04e7bb3-e67a-4681-83af-6ff8fb3a0779" alt="resized Image" width="75%">

### **Project Overview**
This project demonstrates the application of **logistic regression** to classify whether a patient is likely to have diabetes based on specific health measurements. The dataset used is the **Pima Indians Diabetes Dataset**, a widely-used dataset for binary classification problems in machine learning.

---

### **Dataset Overview**

#### **Pima Indians Diabetes Dataset**
- **Source**: [UCI Machine Learning Repository](https://www.kaggle.com/uciml/pima-indians-diabetes-database)
- **Description**: The dataset contains health-related attributes of Pima Indian women and a binary outcome indicating the presence (1) or absence (0) of diabetes.
- **Attributes**:
  - Pregnancies: Number of times pregnant.
  - Glucose: Plasma glucose concentration.
  - BloodPressure: Diastolic blood pressure (mm Hg).
  - SkinThickness: Triceps skinfold thickness (mm).
  - Insulin: 2-Hour serum insulin (mu U/ml).
  - BMI: Body mass index.
  - DiabetesPedigreeFunction: Diabetes pedigree function.
  - Age: Age (years).
  - Outcome: Target variable (1 = Diabetes, 0 = No Diabetes).

---

### **Steps in the Project**

#### **1. Data Preprocessing**
- Loaded the dataset and explored its structure.
- Checked for missing or anomalous values.
- Scaled the feature values to ensure they are on the same scale, using **StandardScaler**.

#### **2. Train-Test Split**
- Split the dataset into training (70%) and testing (30%) subsets.
- Ensured randomization for robust evaluation.

#### **3. Model Training**
- Implemented a **logistic regression model** using scikit-learn’s `LogisticRegression` class.
- Optimized the model using default hyperparameters.

#### **4. Model Evaluation**
- Evaluated the model using:
  - **Accuracy**: Overall classification accuracy.
  - **Precision**: Correct positive predictions among all predicted positives.
  - **Recall (Sensitivity)**: Correct positive predictions among all actual positives.
  - **F1-Score**: Harmonic mean of precision and recall.
  - **Confusion Matrix**: Insights into true positives, true negatives, false positives, and false negatives.

#### **5. Insights from Results**
- Achieved an **accuracy of 75%** on the test dataset.
- Observed the **precision, recall, and F1-score** for both classes.

---

### **Graphs and Visualizations**

#### **1. Confusion Matrix**
- Visualized the confusion matrix to better understand the model's predictions.

#### **2. Precision-Recall Trade-off**
- Explored precision-recall trade-offs using the classification report.

---

![493922_1_En_42_Fig4_HTML](https://github.com/user-attachments/assets/6d59192d-a32c-43fd-a557-fa4c4d422c17)

---

### **Results**

#### **Key Metrics**
- **Accuracy**: 75%
- **Confusion Matrix**:
  - **True Positives (TP)**: 37
  - **True Negatives (TN)**: 79
  - **False Positives (FP)**: 20
  - **False Negatives (FN)**: 18
- **Classification Report**:
  ```
                precision    recall  f1-score   support

           0       0.81      0.80      0.81        99
           1       0.65      0.67      0.66        55

    accuracy                           0.75       154
   macro avg       0.73      0.74      0.73       154

  ```

---

### **Key Insights**

1. **Imbalanced Performance**:
   - The model performs better for the majority class (non-diabetic) due to an imbalanced dataset.
   - Recall for the diabetic class (1) was lower, indicating room for improvement.

2. **Threshold Optimization**:
   - Adjusting the classification threshold might improve recall for the diabetic class.

3. **Feature Importance**:
   - Features like **Glucose** and **BMI** showed strong correlations with diabetes presence, as observed during data exploration.

---

### **How to Run the Project**

#### **1. Load the dataset**
```bash
Load the dataset in the working directory of the colab everytime before executing the code. If you want to access the code from the source then you need to change the code for loading the data set.
```

#### **2. Install Dependencies**
Ensure Python is installed along with the required libraries:
```bash
pip install numpy pandas matplotlib scikit-learn
```
---

### **Next Steps**

1. **Handle Imbalanced Data**:
   - Use techniques like **SMOTE (Synthetic Minority Oversampling Technique)** to balance the dataset.
   - Experiment with class weights in the logistic regression model.

2. **Feature Engineering**:
   - Explore interactions between features (e.g., Glucose * BMI).
   - Apply feature selection methods to identify the most impactful predictors.

3. **Hyperparameter Tuning**:
   - Use grid search or random search to optimize hyperparameters like regularization strength.

4. **Comparison with Other Models**:
   - Compare logistic regression with advanced models like decision trees, random forests, or gradient boosting.

---

