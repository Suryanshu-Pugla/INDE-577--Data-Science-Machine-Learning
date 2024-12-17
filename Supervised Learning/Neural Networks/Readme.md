### **Neural Networks on Social_Network_Ads Dataset**

<img src="img.webp" alt="resized" width="55%">

### **Project Overview**
This project demonstrates the application of a **Dense Neural Network** (DNN) to classify whether a user purchases a product based on their **Age** and **Estimated Salary** using the **Social_Network_Ads dataset**. Neural networks, inspired by the human brain, are used here to model complex relationships between input features and the binary target variable.

The project involves data preprocessing, building a neural network, training the model, and evaluating its performance.

---

### **Dataset Overview**

#### **Social_Network_Ads Dataset**
- **Description**: The dataset contains user demographics (age and salary) and their response to a product advertisement (purchased or not).
- **Attributes**:
  - **User ID**: Unique user identifier (not used in the model).
  - **Age**: Age of the user.
  - **EstimatedSalary**: Estimated annual salary of the user.
  - **Purchased**: Target variable (1 = Purchased, 0 = Did not purchase).
- **Dataset Size**: 400 samples.

---

### **Steps in the Project**

#### **1. Data Preprocessing**
- Loaded the dataset using `pandas`.
- Dropped the **User ID** column as it is irrelevant to the model.
- Standardized the features (**Age** and **EstimatedSalary**) using **StandardScaler** to bring all values to a common scale.
- Split the dataset into **training (80%)** and **testing (20%)** subsets.

#### **2. Model Architecture**
- Built a **Dense Neural Network** (DNN) using **Keras** with the following structure:
  - **Input Layer**: Two input features (Age, EstimatedSalary).
  - **Hidden Layers**:
    - 1st Layer: 8 neurons with ReLU activation.
    - 2nd Layer: 4 neurons with ReLU activation.
  - **Output Layer**: 1 neuron with a **Sigmoid activation** for binary classification.
- Used **binary cross-entropy** as the loss function.
- Optimized the model using **Adam optimizer**.

#### **3. Model Training**
- Trained the neural network on the training dataset for **50 epochs** with a batch size of **16**.
- Monitored the training and validation loss to ensure no overfitting.

#### **4. Model Evaluation**
- Evaluated the model's performance on the test dataset using:
  - **Accuracy**: Proportion of correct predictions.
  - **Confusion Matrix**: True positives, true negatives, false positives, and false negatives.
  - **Precision, Recall, and F1-Score**: For a detailed class-wise evaluation.

#### **5. Visualizations**
- Plotted the confusion matrix to analyze the performance.
- Visualized the training and validation loss curves over epochs.

![artificial-neural-network6](https://github.com/user-attachments/assets/7fb3ccf8-272a-4e56-a22c-e1bdca582c56)

### **Results**

#### **Key Metrics**
- **Accuracy**: 90%
- **Confusion Matrix**:
  | Actual \ Predicted | 0   | 1   |
  |--------------------|-----|-----|
  | **0**             | 49  | 3   |
  | **1**             | 5   | 23  |

- **Classification Report**:
  ```
              precision    recall  f1-score   support

           0       0.91      0.94      0.92        52
           1       0.88      0.82      0.85        28

    accuracy                           0.90        80
   macro avg       0.89      0.88      0.89        80
  ```

#### **Training and Validation Loss**
- The loss curves indicate that the model successfully converged without overfitting.

---

### **Key Insights**
1. **Model Performance**:
   - The neural network achieved **90% accuracy**, demonstrating its ability to capture the relationships between age, salary, and purchasing behavior.

2. **Confusion Matrix Analysis**:
   - A small number of false positives (3) and false negatives (5) suggest that the model is balanced.

3. **Feature Scaling Impact**:
   - Standardizing features significantly improved the performance of the model, as neural networks are sensitive to feature magnitudes.

4. **Sigmoid Activation**:
   - The use of the sigmoid activation function in the output layer enabled binary classification by producing probabilities.

---

### **How to Run the Project**

#### **1. Clone the Repository**
```bash
git clone <repository_link>
cd neural-network-social-network-ads
```

#### **2. Install Dependencies**
Ensure Python and required libraries are installed:
```bash
pip install numpy pandas matplotlib scikit-learn tensorflow keras
```

#### **3. Run the Script**
Execute the script to preprocess the data, train the model, and evaluate results:
```bash
python neural_network_social_ads.py
```

---

### **Next Steps**
1. **Hyperparameter Tuning**:
   - Experiment with different numbers of neurons, layers, and activation functions to optimize performance.

2. **Regularization**:
   - Apply techniques like dropout to prevent overfitting.

3. **Comparison with Other Models**:
   - Compare neural network performance with simpler models like logistic regression or KNN.

4. **Feature Engineering**:
   - Explore additional features or interactions to improve predictions.

---


