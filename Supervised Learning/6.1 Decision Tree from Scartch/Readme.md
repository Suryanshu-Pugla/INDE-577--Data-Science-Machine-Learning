# **Decision Tree Classifier from Scratch Using Breast Cancer Dataset**

<img src="https://github.com/user-attachments/assets/3a67a484-663c-4c46-828b-20c7770c278d" alt="resized" width="60%">

## **Project Overview**
This project demonstrates the implementation of a **Decision Tree Classifier** from scratch in Python to classify whether a breast tumor is malignant or benign. The model is evaluated on the **Breast Cancer Dataset** from the scikit-learn library.

This project highlights key decision tree concepts like **Gini Impurity**, **data splitting**, and **recursive tree building**, all implemented without external machine learning libraries like `sklearn`.

---

## **Dataset Overview**

### **Breast Cancer Dataset**
- **Source**: Scikit-learn's built-in dataset ([Breast Cancer Wisconsin Diagnostic Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)).
- **Description**: The dataset contains medical measurements extracted from breast cancer biopsy images, used to classify tumors as malignant (0) or benign (1).
- **Number of Samples**: 569
- **Features**: 30 continuous numerical features, including:
   - Mean radius, texture, perimeter, area, smoothness, compactness, concavity, symmetry, etc.
- **Target**: 
   - `0`: Malignant (cancerous tumor)
   - `1`: Benign (non-cancerous tumor)

---

## **Steps in the Project**

### **1. Gini Impurity Calculation**
The **Gini Impurity** is used to measure the quality of splits:
\[
Gini = 1 - \sum_{i=1}^k p_i^2
\]
Where \( p_i \) is the probability of a sample belonging to class \( i \).

### **2. Data Splitting**
At each node:
- The dataset is split into two subsets (left and right) based on a feature threshold.
- The split minimizes the weighted **Gini Impurity**.

### **3. Recursive Tree Building**
The tree grows recursively by:
- Evaluating all possible splits for each feature.
- Selecting the split that minimizes impurity.
- Stopping conditions:
   - Reached maximum tree depth.
   - Minimum samples per node threshold is satisfied.

### **4. Model Training**
The training process involves fitting the decision tree using the training dataset.

### **5. Prediction**
For a new sample:
- The tree is traversed based on feature values until a **leaf node** is reached.
- The leaf node returns the **majority class**.

### **6. Model Evaluation**
The model is evaluated on the test dataset using **accuracy** as the performance metric.

---

## **Dependencies**
Ensure the following Python libraries are installed:
```bash
pip install numpy pandas scikit-learn
```

---

## **Code Workflow**
1. **Load the Dataset**:
   - The Breast Cancer Dataset is loaded using `sklearn.datasets`.
2. **Train-Test Split**:
   - Split the data into 80% training and 20% testing.
3. **Train the Decision Tree**:
   - Fit the custom-built decision tree on the training data.
4. **Make Predictions**:
   - Predict class labels for the test dataset.
5. **Evaluate Performance**:
   - Calculate the accuracy of the model on the test data.

---

## **How to Run the Code**
1. Copy the Python script into a `.py` file or Jupyter Notebook.
2. Run the script:
   ```bash
   python decision_tree_breast_cancer.py
   ```
3. Output will display the accuracy of the model.

---

## **Results**
The decision tree classifier achieved the following result:
- **Accuracy**: ~95% on the Breast Cancer Dataset.

**Example Output**:
```
Decision Tree Classifier Results on Breast Cancer Dataset:
Accuracy: 0.95
```

---

## **Key Insights**
1. **Custom Implementation**:
   - This project demonstrates the inner workings of a decision tree without using external libraries like `sklearn.tree`.
2. **Performance**:
   - The model achieves high accuracy on a medical dataset with minimal depth and overfitting controls.
3. **Gini Impurity**:
   - The Gini Impurity effectively measures split quality and reduces class impurity at each node.
4. **Stopping Criteria**:
   - Parameters like `max_depth` and `min_samples_split` prevent overfitting.

---

## **Next Steps**
1. **Visualization**:
   - Visualize the decision tree to better understand the decision-making process.
2. **Feature Importance**:
   - Add functionality to rank features based on their contribution to the splits.
3. **Hyperparameter Tuning**:
   - Optimize `max_depth` and `min_samples_split` for better performance.
4. **Multi-Class Datasets**:
   - Extend the implementation to handle multi-class classification problems.

---

## **Conclusion**
This project successfully implements a **Decision Tree Classifier** from scratch and applies it to the **Breast Cancer Dataset**. The model achieves high accuracy and demonstrates the effectiveness of decision trees for binary classification tasks.

---


