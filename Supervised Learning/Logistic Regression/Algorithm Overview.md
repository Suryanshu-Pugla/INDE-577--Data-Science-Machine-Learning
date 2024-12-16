### **Logistic Regression Algorithm**

<img src="https://github.com/user-attachments/assets/d15c2a0e-8555-4502-a479-c6d818a404e9" alt="Resized Image" width="75%">

### **Overview**
Logistic regression is a **supervised learning algorithm** used primarily for classification tasks. Despite its name, logistic regression is a classification model, not a regression model. It predicts the probability of an input belonging to a specific class and assigns a label based on a threshold (default: 0.5).

---

### **Key Characteristics**
- **Algorithm Type**: Linear classification model.
- **Output**: Probabilities (values between 0 and 1) and class labels.
- **Applications**: Binary classification (e.g., spam detection) and multi-class classification (with extensions).

---

### **Logistic Regression Mechanics**

#### **1. Linear Combination**
The algorithm starts with a linear combination of the input features:
\[
 z = w_1x_1 + w_2x_2 + \ldots + w_nx_n + b
\]
Where:
- \( w_1, w_2, \ldots, w_n \): Feature weights.
- \( x_1, x_2, \ldots, x_n \): Feature values.
- \( b \): Bias term.

#### **2. Sigmoid Function**
The output of the linear combination is passed through the sigmoid function to map it to probabilities:
\[
 \sigma(z) = \frac{1}{1 + e^{-z}}
\]
This ensures the output lies between 0 and 1.

#### **3. Binary Classification**
The predicted class is determined by comparing the probability to a threshold:
\[
 \hat{y} =
 \begin{cases}
 1 & \text{if } \sigma(z) \geq \text{threshold (default: 0.5)} \\
 0 & \text{if } \sigma(z) < \text{threshold}
 \end{cases}
\]

#### **4. Cost Function**
The algorithm uses the **log-loss (binary cross-entropy loss)** function to optimize weights and bias:
\[
 J(w, b) = - \frac{1}{m} \sum_{i=1}^m \Big[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \Big]
\]
Where:
- \( y_i \): Actual label (0 or 1).
- \( \hat{y}_i \): Predicted probability.
- \( m \): Number of training examples.

#### **5. Optimization**
The weights and bias are optimized using **gradient descent** or its variants (e.g., stochastic gradient descent).

![LogReg_1](https://github.com/user-attachments/assets/687f1b58-4331-4192-a409-b941a5e53531)


### **Extensions of Logistic Regression**

#### **1. Multi-Class Logistic Regression**
- For multi-class problems, logistic regression is extended using techniques like:
  - **One-vs-All (OvA)**: A separate model for each class.
  - **Softmax Regression**: Outputs probabilities for all classes.

#### **2. Regularization**
To prevent overfitting, regularization techniques are applied:
- **L1 Regularization (Lasso)**: Adds \( \lambda \sum |w_i| \) to the cost function.
- **L2 Regularization (Ridge)**: Adds \( \lambda \sum w_i^2 \) to the cost function.

---

### **Advantages**
1. **Simple and Efficient**:
   - Easy to implement and computationally efficient for small to medium datasets.
2. **Interpretable**:
   - Feature weights provide insights into feature importance.
3. **Probability Outputs**:
   - Generates probabilities that can guide decision-making.

---

### **Limitations**
1. **Linear Decision Boundary**:
   - Assumes a linear relationship between features and log-odds, which may not work for non-linear data.
2. **Sensitive to Outliers**:
   - Outliers can significantly affect model performance.
3. **Not Ideal for High-Dimensional Data**:
   - Requires regularization to handle datasets with many features.

---

### **Applications**
1. **Medical Diagnosis**:
   - Predicting the presence of diseases (e.g., diabetes detection).
2. **Spam Detection**:
   - Classifying emails as spam or not spam.
3. **Churn Prediction**:
   - Identifying customers likely to leave a service.
4. **Credit Risk Analysis**:
   - Assessing the likelihood of loan default.
5. **Marketing Campaigns**:
   - Predicting customer responses to advertisements.

---

### **Evaluation Metrics**
1. **Accuracy**: Fraction of correct predictions.
2. **Precision**: Fraction of true positive predictions out of all predicted positives.
3. **Recall (Sensitivity)**: Fraction of true positives out of all actual positives.
4. **F1-Score**: Harmonic mean of precision and recall.
5. **ROC-AUC**: Measures the trade-off between true positive and false positive rates.

---

![linear-regression-vs-logistic-regression](https://github.com/user-attachments/assets/945e2d3b-f4b7-4da2-9fa8-37885882b634)

### **Conclusion**
Logistic regression is a powerful and interpretable algorithm for classification tasks. While it is best suited for linearly separable data, it provides a strong baseline and serves as the foundation for more advanced models. Extensions like regularization and multi-class logistic regression make it versatile for a wide range of applications.

---

