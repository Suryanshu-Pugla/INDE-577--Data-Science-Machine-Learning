# **Random Forest Classifier on MNIST Handwritten Digits Dataset**

## **Project Overview**
This project demonstrates the application of a **Random Forest Classifier** to the **MNIST Handwritten Digits Dataset**. The goal is to classify handwritten digits (0-9) based on pixel intensity values of 28x28 grayscale images. The project showcases data preprocessing, model training, evaluation, and visualization of results, including misclassified digits.

---

## **Dataset Overview**

### **MNIST Handwritten Digits Dataset**
- **Source**: Scikit-learn's `fetch_openml` API.
- **Description**: The dataset contains 70,000 images of handwritten digits (0-9), with each image represented as a **28x28 pixel grid**.
- **Number of Samples**: 70,000 (60,000 for training and 10,000 for testing).
- **Features**: 784 features representing pixel intensity values (0-255).
- **Target**: Labels from 0 to 9, representing the digit class.

---

## **Steps in the Project**

### **1. Load and Explore the Dataset**
- The MNIST dataset is loaded using `fetch_openml`.
- Features (`X`) consist of 784 pixel intensity values for each image.
- Targets (`y`) represent the corresponding digit class (0-9).

### **2. Preprocess the Data**
- Split the dataset into **training (80%)** and **testing (20%)** subsets using `train_test_split`.
- No additional scaling is needed since Random Forest does not require feature scaling.

### **3. Train the Random Forest Classifier**
- A **Random Forest Classifier** is built using:
  - **n_estimators**: 100 (number of decision trees).
  - **max_depth**: 20 (limits the depth of trees to prevent overfitting).
  - **random_state**: Ensures reproducibility of results.

### **4. Evaluate the Model**
- Model performance is measured using:
  1. **Accuracy**: Measures overall classification performance.
  2. **Confusion Matrix**: Highlights the correct and incorrect predictions.
  3. **Classification Report**: Provides precision, recall, and F1-score for each class.

### **5. Visualize Results**
- A **confusion matrix** is visualized as a heatmap.
- **Misclassified digits** are displayed with their predicted and actual labels.

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
- Visualization of misclassified digits.

---

## **Results**

### **Model Accuracy**
- The Random Forest model achieves an accuracy of **96%** on the test dataset.

### **Confusion Matrix**
- A heatmap is generated to display the confusion matrix, showing predictions vs. actual labels.

### **Classification Report**
```
              precision    recall  f1-score   support

           0       0.99      0.99      0.99       980
           1       0.98      0.99      0.99      1135
           2       0.96      0.96      0.96      1032
           3       0.95      0.95      0.95      1010
           4       0.96      0.97      0.96       982
           5       0.95      0.94      0.94       892
           6       0.97      0.98      0.97       958
           7       0.96      0.96      0.96      1028
           8       0.94      0.94      0.94       974
           9       0.95      0.94      0.95      1009

    accuracy                           0.96     10000
   macro avg       0.96      0.96      0.96     10000
weighted avg       0.96      0.96      0.96     10000
```

### **Visualization of Misclassified Digits**
- Images of misclassified digits are displayed with their **predicted** and **actual labels**, providing insight into areas for model improvement.

---

## **Key Insights**
1. **High Accuracy**: The Random Forest model achieves an impressive accuracy of **96%** on the test dataset.
2. **Misclassified Digits**: Some digits are misclassified, often due to visual similarity (e.g., 4 and 9).
3. **Feature Importance**: Random Forest can analyze pixel-level importance for predictions, although this is less interpretable for image data.

---

## **Next Steps**
1. **Hyperparameter Tuning**:
   - Use `GridSearchCV` to optimize hyperparameters like `n_estimators`, `max_depth`, and `min_samples_split`.
2. **Dimensionality Reduction**:
   - Apply **PCA (Principal Component Analysis)** to reduce the number of features and improve training speed.
3. **Ensemble Learning**:
   - Combine Random Forest with other models like SVM or Gradient Boosting for further performance gains.
4. **Deep Learning**:
   - Use **Convolutional Neural Networks (CNNs)** for more advanced and accurate image classification.

---

## **Conclusion**
This project demonstrates the effectiveness of **Random Forest** for classifying handwritten digits using the **MNIST Dataset**. The model achieves high accuracy and provides interpretable results through metrics and visualizations. By exploring hyperparameter tuning and advanced techniques, the performance can be further enhanced.

---

