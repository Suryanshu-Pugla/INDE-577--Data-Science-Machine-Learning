### **K-Nearest Neighbors on Wine Dataset**

<img src="https://github.com/user-attachments/assets/d6739369-4322-40f6-b97b-e24676d0d1a1" alt="resized" width="40%">

### **Project Overview**
This project demonstrates the application of the **K-Nearest Neighbors (KNN)** algorithm for **multi-class classification** using the **Wine Dataset**. The goal is to classify wines into one of three classes based on their chemical composition.

KNN is a distance-based supervised machine learning algorithm that classifies data points based on the majority class of their nearest neighbors.

---

### **Dataset Overview**

#### **Wine Dataset**
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/wine)
- **Description**: The dataset contains 178 samples of wine from three different classes, with 13 features describing the chemical composition of each wine sample.
- **Attributes**:
  1. **Alcohol**
  2. **Malic Acid**
  3. **Ash**
  4. **Alcalinity of Ash**
  5. **Magnesium**
  6. **Total Phenols**
  7. **Flavanoids**
  8. **Nonflavanoid Phenols**
  9. **Proanthocyanins**
  10. **Color Intensity**
  11. **Hue**
  12. **OD280/OD315 of diluted wines**
  13. **Proline**
- **Target Variable**: Wine class (0, 1, or 2).

---

### **Steps in the Project**

#### **1. Data Preprocessing**
- Loaded the dataset using scikit-learn's `datasets` library.
- Scaled the features using **StandardScaler** to ensure all features contribute equally to distance calculations.
- Split the dataset into **training** (80%) and **testing** (20%) subsets for evaluation.

#### **2. Model Training**
- Implemented the **KNN algorithm** using scikit-learn's `KNeighborsClassifier`.
- Selected an optimal value of **k (number of neighbors)** using hyperparameter tuning.

#### **3. Model Evaluation**
- Evaluated the model performance using:
  - **Accuracy**: Overall correctness of predictions.
  - **Confusion Matrix**: Insight into the distribution of correct and incorrect predictions.
  - **Classification Report**: Precision, recall, and F1-score for each class.

#### **4. Visualization**
- Visualized the accuracy for different values of **k** to determine the best-performing k.
- Plotted the **confusion matrix** to better understand model predictions.

<img src="https://github.com/user-attachments/assets/dbf568fe-8641-42b4-a789-946a2c333a30" alt="resized" width="60%">

### **Results**

#### **Key Metrics**
- **Accuracy**: 94% on the test dataset.
- **Confusion Matrix**:
  | Actual \ Predicted | Class 0 | Class 1 | Class 2 |
  |--------------------|---------|---------|---------|
  | **Class 0**       | 14      | 0       | 0       |
  | **Class 1**       | 1       | 12      | 1       |
  | **Class 2**       | 0       | 0       | 9       |

- **Classification Report**:
  ```
              precision    recall  f1-score   support

           0       0.93      1.00      0.97        14
           1       1.00      0.86      0.92        14
           2       0.89      1.00      0.94         8

    accuracy                           0.94        36
   macro avg       0.95      0.94      0.94        36
  ```

---

### **Graphs and Visualizations**

1. **Accuracy vs. k (Number of Neighbors)**:
   - Plotted the accuracy scores for various values of k to identify the optimal k.

2. **Confusion Matrix Heatmap**:
   - Visualized the confusion matrix to analyze model performance across classes.

---

### **Key Insights**
1. **Optimal Value of k**:
   - The best performance was achieved at **k = 5**, with an accuracy of 97%.

2. **Class Performance**:
   - The model achieved perfect precision and recall for Class 3.
   - Minor misclassifications occurred between Class 1 and Class 2, but the overall performance remained high.

3. **Feature Scaling**:
   - Scaling the features significantly improved the performance of the KNN model, as distance-based models are sensitive to feature magnitudes.

---

### **How to Run the Project**

#### **1. Clone the Repository**
```bash
Load the dataset in the working directory of the colab everytime before executing the code. If you want to access the code from the source then you need to change the code for loading the data set.
```

#### **2. Install Dependencies**
Ensure Python is installed along with the required libraries:
```bash
pip install numpy pandas matplotlib scikit-learn
```

#### **3. Run the Script**
Execute the script to preprocess the data, train the model, and visualize results:
```bash
python knn_wine_dataset.py
```

---

### **Next Steps**

1. **Feature Importance**:
   - Analyze which features contribute most to the classification.

2. **Dimensionality Reduction**:
   - Use Principal Component Analysis (PCA) to reduce feature dimensions and improve computational efficiency.

3. **Comparison with Other Algorithms**:
   - Compare KNN performance with logistic regression, decision trees, or support vector machines.

4. **Cross-Validation**:
   - Perform k-fold cross-validation to ensure robust model evaluation.

---

