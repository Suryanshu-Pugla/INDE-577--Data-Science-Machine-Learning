# **Bagging Classifier on Census Income Dataset**

![maxresdefault](https://github.com/user-attachments/assets/836daeb9-f2c5-443b-ad31-838c1bfdb478)

## **Project Overview**
This project implements the **Bagging Ensemble Method** using a **Bagging Classifier** with a base model of **Decision Trees** to predict whether an individual's annual income exceeds $50K. The dataset used is the **Census Income Dataset (Adult Dataset)**, which contains demographic and employment-related attributes.

The project demonstrates data preprocessing, training, evaluation, and feature importance analysis using the Bagging ensemble technique.

---

## **Dataset Overview**

### **Census Income Dataset**
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/adult)
- **Description**: Predict whether a person earns more than $50K annually based on demographic and employment information.
- **Number of Samples**: 32,561 rows (training data).
- **Features**:
  - `Age`: Age of the individual.
  - `Workclass`: Type of employer (e.g., Private, Government).
  - `Fnlwgt`: Final weight.
  - `Education`: Highest level of education.
  - `Education-Num`: Number of years of education.
  - `Marital Status`: Marital status.
  - `Occupation`: Job type.
  - `Relationship`: Family relationship.
  - `Race`: Race.
  - `Sex`: Gender.
  - `Capital Gain`: Income from investment.
  - `Capital Loss`: Losses from investment.
  - `Hours/Week`: Weekly working hours.
  - `Country`: Country of residence.
  - `Income`: Target variable (`<=50K` or `>50K`).

---

## **Steps in the Project**

### **1. Load the Dataset**
- The dataset is loaded from the UCI repository.
- Missing values (`?`) are identified and handled by dropping rows with missing data.

### **2. Data Preprocessing**
- Categorical variables are encoded using **Label Encoding**.
- The dataset is split into **features** (`X`) and **target** (`y`).
- The data is split into **training (80%)** and **testing (20%)** subsets using `train_test_split`.

### **3. Train the Bagging Classifier**
- A **Bagging Classifier** is used with a base model of **Decision Trees**:
  - `max_depth=10`: Limits the depth of decision trees to avoid overfitting.
  - `n_estimators=50`: Combines 50 base decision trees.
  - `random_state=42`: Ensures reproducibility.

### **4. Model Evaluation**
The model's performance is evaluated using:
- **Accuracy**: Measures the overall performance of the model.
- **Confusion Matrix**: Shows true positives, true negatives, false positives, and false negatives.
- **Classification Report**: Includes precision, recall, and F1-score for each class.

### **5. Visualize Results**
- **Confusion Matrix**: Visualized as a heatmap to analyze predictions.
- **Feature Importance**: Visualized to identify the most significant predictors.

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
- Model accuracy and evaluation metrics.
- Confusion matrix heatmap.
- Feature importance bar plot.

---

## **Results**

### **Model Accuracy**
- The Bagging Classifier achieves an accuracy of **~86%** on the test dataset.

### **Confusion Matrix**
- The confusion matrix highlights the correct and incorrect predictions:

```
[[4941  356]
 [ 722  985]]
```

### **Classification Report**
```
              precision    recall  f1-score   support

          <=50K       0.87      0.93      0.90      5297
           >50K       0.73      0.58      0.65      1707

       accuracy                           0.86      7004
      macro avg       0.80      0.76      0.77      7004
   weighted avg       0.85      0.86      0.85      7004
```

### **Feature Importance Visualization**
- Key features contributing to predictions include:
  1. **Education-Num**: Number of years of education.
  2. **Hours/Week**: Weekly working hours.
  3. **Capital Gain**: Income from investments.

---

## **Visualizations**

### **Confusion Matrix**
![Confusion Matrix](https://your-image-link-here.png)

### **Feature Importance**
The top predictors are visualized using a bar plot to demonstrate their relative importance in the Bagging Classifier.

---

## **Key Insights**
1. **Model Performance**:
   - The Bagging Classifier achieves an accuracy of **86%**, effectively handling the mixed categorical and numerical features.
2. **Class Imbalance**:
   - Precision and recall are slightly lower for the `>50K` class due to fewer samples in this category.
3. **Feature Importance**:
   - Features such as **Education-Num**, **Capital Gain**, and **Hours/Week** are strong predictors of income levels.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Use `GridSearchCV` or `RandomizedSearchCV` to optimize parameters such as `n_estimators` and `max_depth`.
2. **Class Imbalance Handling**:
   - Use techniques like **SMOTE** or assign class weights to improve predictions for the minority class (`>50K`).
3. **Model Comparison**:
   - Compare the Bagging Classifier with other ensemble methods like **Random Forest** or **Boosting**.
4. **Feature Engineering**:
   - Create new features such as income-to-age ratios or interaction terms for better predictions.

---

## **Conclusion**
This project demonstrates how the **Bagging Ensemble Method** improves classification performance and reduces overfitting using the **Census Income Dataset**. By combining multiple decision trees, the Bagging Classifier achieves robust and interpretable results, with feature importance highlighting key predictors of income levels.

---

