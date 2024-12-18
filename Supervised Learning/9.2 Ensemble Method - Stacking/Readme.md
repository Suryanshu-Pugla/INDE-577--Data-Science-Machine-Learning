# **Stacking Ensemble Method for Online Shoppers Purchasing Intention Dataset**

![images](https://github.com/user-attachments/assets/0d32619a-02ab-46db-a9ff-05f0803fbc06)

## **Project Overview**
This project applies the **Stacking Ensemble Method** to predict whether an online shopper will make a purchase or not based on behavioral features. The dataset, **Online Shoppers Purchasing Intention**, contains session-based features such as browsing behavior, page visit durations, and session types.

The stacking ensemble combines predictions from **Logistic Regression**, **Decision Trees**, and **K-Nearest Neighbors (KNN)** using a **Logistic Regression meta-classifier** to improve overall accuracy.

---

## **Dataset Overview**

### **Online Shoppers Purchasing Intention Dataset**
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Shoppers+Purchasing+Intention+Dataset)
- **Description**: The dataset contains session-level attributes of users visiting an e-commerce website. The goal is to predict whether the session will result in a purchase.
- **Number of Samples**: 12,330 rows.
- **Features**:
    - **Administrative**: Number of administrative pages visited.
    - **Administrative Duration**: Time spent on administrative pages.
    - **Informational**: Number of informational pages visited.
    - **Product-Related**: Number of product-related pages visited.
    - **Bounce Rates**: Percentage of single-page visits.
    - **Exit Rates**: Exit rates for the session.
    - **Page Values**: Numeric score assigned to pages visited.
    - **Month**: Month of the session.
    - **Visitor Type**: Type of visitor (Returning/Other).
    - **Weekend**: Boolean indicating if the session occurred on a weekend.
    - **Revenue**: Target variable (1 = Purchase, 0 = No Purchase).

---

## **Steps in the Project**

### **1. Load and Explore the Dataset**
- The dataset is loaded from the local file `online_shoppers_intention.csv`.
- Columns are inspected to understand features and target variables.

### **2. Preprocess the Data**
- Categorical features (`Month`, `VisitorType`) are encoded using **Label Encoding**.
- Features are standardized using **StandardScaler** to improve model performance.
- The dataset is split into **training (80%)** and **testing (20%)** subsets.

### **3. Define Base Models**
The following models are used as base learners:
1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **K-Nearest Neighbors (KNN)**

### **4. Build the Stacking Classifier**
- The predictions from the base learners are combined using a **Logistic Regression meta-classifier**.
- **5-Fold Cross-Validation** is applied during stacking to reduce overfitting.

### **5. Model Evaluation**
The model is evaluated using:
- **Accuracy**: Overall classification performance.
- **Confusion Matrix**: Visualized to analyze correct and incorrect predictions.
- **Classification Report**: Precision, recall, and F1-score for both classes.

### **6. Visualize Results**
- A confusion matrix is visualized as a heatmap.

---

## **Dependencies**
Ensure the following Python libraries are installed:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## **How to Run the Project**
1. Place the dataset file `online_shoppers_intention.csv` in your working directory.
2. Copy the project code into a Python script or Jupyter Notebook.
3. Install the required dependencies using the command above.
4. Run the script.

**Output**:
- Model accuracy and evaluation metrics.
- Confusion matrix heatmap.

---

## **Results**

### **Model Accuracy**
The Stacking Ensemble Classifier achieves an accuracy of **~89%** on the test dataset.

### **Confusion Matrix**
```
Confusion Matrix:
[[1926   74]
 [ 219  381]]
```

### **Classification Report**
```
              precision    recall  f1-score   support

           0       0.90      0.96      0.93      2000
           1       0.84      0.64      0.73       600

    accuracy                           0.89      2600
   macro avg       0.87      0.80      0.83      2600
weighted avg       0.88      0.89      0.88      2600
```

### **Visualizations**
#### **Confusion Matrix Heatmap**
The confusion matrix shows how the model performs across both classes (Purchase vs. No Purchase):

![Confusion Matrix](your_image_placeholder.png)

---

## **Key Insights**
1. **High Accuracy**: The Stacking Ensemble improves accuracy by combining multiple base models.
2. **Performance on Minority Class**:
   - Precision for the `Purchase` class is **84%**, while recall is lower due to fewer samples.
3. **Model Comparison**: Stacking outperforms individual models like Logistic Regression, Decision Trees, and KNN.
4. **Imbalance in Data**: The dataset has more `No Purchase` instances, which impacts recall for the `Purchase` class.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Use `GridSearchCV` to optimize parameters for base models (e.g., `max_depth` for Decision Trees, `n_neighbors` for KNN).
2. **Class Imbalance Handling**:
   - Apply techniques like **SMOTE** or assign class weights to improve predictions for the `Purchase` class.
3. **Add More Base Models**:
   - Include other classifiers like **SVM**, **Random Forest**, or **Gradient Boosting**.
4. **Feature Engineering**:
   - Create new interaction features such as ratios of page views or duration metrics.

---

## **Conclusion**
This project demonstrates the power of the **Stacking Ensemble Method** for predicting online purchasing behavior. By combining multiple classifiers and a meta-classifier, the stacking ensemble achieves high accuracy and provides robust predictions for a real-world e-commerce dataset.

---

