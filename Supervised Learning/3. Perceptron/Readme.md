### **Perceptron Model on Social_Network_Ads Dataset**

<img src="https://github.com/user-attachments/assets/09a4323a-92fc-4a43-90a8-6896898f88e4" alt="resized image" width="50%">

### **Project Overview**
This project demonstrates the application of the **Perceptron model** to classify whether a user purchases a product based on their age and estimated salary. The dataset used is the **Social_Network_Ads** dataset, which is widely used for binary classification problems.

The Perceptron algorithm is a simple linear classifier that learns a decision boundary to separate two classes based on input features.

---

### **Dataset Overview**

#### **Social_Network_Ads Dataset**
- **Description**: The dataset contains information about users' age, estimated salary, and whether they purchased a product after viewing an advertisement on a social media platform.
- **Attributes**:
  - **User ID**: Unique identifier for each user (not used for modeling).
  - **Age**: Age of the user.
  - **EstimatedSalary**: Estimated annual salary of the user.
  - **Purchased**: Target variable (1 = Purchased, 0 = Did not purchase).

---

### **Steps in the Project**

#### **1. Data Preprocessing**
- Loaded the dataset and explored its structure.
- Removed unnecessary columns like **User ID**.
- Standardized the features (**Age** and **EstimatedSalary**) using **StandardScaler** to bring them to the same scale.
- Split the dataset into **training** and **testing** sets (80% training, 20% testing).

#### **2. Model Training**
- Implemented the **Perceptron model** using scikit-learn's `Perceptron` class.
- Trained the model on the training data to learn the linear decision boundary.

#### **3. Model Evaluation**
- Evaluated the model using:
  - **Accuracy**: Overall classification accuracy on the test set.
  - **Confusion Matrix**: Insights into correct and incorrect predictions.
  - **Classification Report**: Precision, recall, and F1-score for each class.

#### **4. Visualization**
- Plotted the decision boundary to visualize how the Perceptron separates the two classes.
- Generated a confusion matrix heatmap to evaluate model predictions.

<img src="https://github.com/user-attachments/assets/0074671f-227d-490f-a02b-4183fdee9e1b" alt="resized image" width="70%">


### **Results**

#### **Key Metrics**
- **Accuracy**: 75%
- **Confusion Matrix**:
  | Actual \ Predicted | 0   | 1   |
  |--------------------|-----|-----|
  | **0**             | 44  | 8   |
  | **1**             | 12  | 16  |

- **Classification Report**:
  ```
              precision    recall  f1-score   support

           0       0.79      0.85      0.81        52
           1       0.67      0.57      0.62        28

    accuracy                           0.75        80
   macro avg       0.73      0.71      0.72        80
  ```

---

### **Graphs and Visualizations**

1. **Decision Boundary Visualization**:
   - Visualized the linear decision boundary created by the Perceptron model.
   - Users in different regions of the graph represent whether they purchased the product (1) or not (0).

2. **Confusion Matrix Heatmap**:
   - Plotted a heatmap to display the confusion matrix, showing the true positives, true negatives, false positives, and false negatives.

---

### **Key Insights**
1. **Model Performance**:
   - The Perceptron achieved an accuracy of 75%, indicating reasonable performance for a linear classifier on this dataset.
   - Class 0 (Did not purchase) is better predicted compared to Class 1 (Purchased), as indicated by higher precision and recall values for Class 0.

2. **Decision Boundary**:
   - The Perceptron learned a **linear decision boundary** to separate the two classes.
   - However, some misclassifications suggest that the data may not be perfectly linearly separable.

3. **Feature Impact**:
   - Both **Age** and **EstimatedSalary** are useful predictors, but further analysis (e.g., feature importance) could be performed to determine their exact contributions.

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
python perceptron_social_network_ads.py
```
#### **3. Dataset**
Ensure the Wholesale Customers Dataset is in the working directory or update the file path in the script.

---

### **Next Steps**

1. **Non-Linear Classifiers**:
   - Explore non-linear models like Support Vector Machines (SVMs) or decision trees to handle datasets that are not linearly separable.

2. **Data Imbalance**:
   - Address potential class imbalance to improve performance on the minority class.

3. **Feature Engineering**:
   - Create interaction terms or polynomial features to improve the Perceptron's performance.

4. **Comparison with Other Models**:
   - Compare the Perceptron model with logistic regression, SVM, or ensemble methods.

---

