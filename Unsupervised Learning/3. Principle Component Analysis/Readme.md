### **PCA Analysis on Wholesale Customers Dataset**

<img src="https://github.com/user-attachments/assets/120a0d0d-a598-4cea-96e4-bc1df7ce428d" width="605%">

### **Project Overview**
This project applies the **Principal Component Analysis (PCA)** algorithm to the **Wholesale Customers Dataset** to analyze customer spending patterns across various product categories. PCA is used for dimensionality reduction to uncover hidden patterns and simplify data visualization.

### **Dataset Overview**

- **Dataset Name**: Wholesale Customers Dataset
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers)
- **Number of Records**: 440
- **Features**:
  - `Fresh`: Annual spending on fresh products.
  - `Milk`: Annual spending on milk products.
  - `Grocery`: Annual spending on groceries.
  - `Frozen`: Annual spending on frozen products.
  - `Detergents_Paper`: Annual spending on detergents and paper products.
  - `Delicassen`: Annual spending on delicatessen products.
- **Target**: No explicit target (unsupervised dataset).

---

### **Steps in the Project**

#### **1. Data Loading and Exploration**
- Loaded the dataset using **Pandas**.
- Checked for missing values and explored basic statistics.
- Visualized feature distributions to understand spending patterns.

#### **2. Data Preprocessing**
- Selected relevant features for analysis.
- Standardized the data using **StandardScaler** to ensure all features had a mean of 0 and a variance of 1.

#### **3. Apply PCA**
- Applied **Principal Component Analysis (PCA)** to reduce dimensions while retaining 95% of the variance.
- Identified the number of principal components required to explain 95% of the variance.
- Analyzed the contribution of each original feature to the principal components (loadings).

#### **4. Visualize Results**
- Plotted the explained variance ratio to evaluate the importance of each principal component.
- Visualized data in the reduced 2D space using the first two principal components.
- Created a heatmap of feature loadings to interpret the relationship between original features and principal components.

#### **5. Clustering on PCA-Transformed Data**
- Applied **K-Means Clustering** on the PCA-reduced data.
- Visualized clusters in the PCA space and evaluated cluster quality using the **Silhouette Score**.

---

### **Algorithm Used**

#### **Principal Component Analysis (PCA)**
- **Goal**: Reduce the number of features while retaining most of the variability in the dataset.
- **Key Steps**:
  1. Standardize the features.
  2. Compute the covariance matrix.
  3. Calculate eigenvalues and eigenvectors.
  4. Project the data onto the top principal components.
- **Evaluation**:
  - Explained variance ratio for each principal component.
  - Contribution of features to each principal component (loadings).

#### **K-Means Clustering**
- Performed clustering on the PCA-reduced data to identify distinct customer groups.
- Evaluated cluster quality using the **Silhouette Score**.

<img width="331" alt="PrincipalComponents" src="https://github.com/user-attachments/assets/8604039f-c9e3-4be9-ab10-0130550a1b4a" />

### **Key Insights**

1. **Dimensionality Reduction**:
   - PCA reduced the dataset from 6 features to 3 principal components while retaining 95% of the variance.

2. **Feature Contributions**:
   - `Detergents_Paper` had the highest contribution to the first principal component, indicating it significantly influences variability.
   - `Fresh` and `Frozen` contributed more to the second principal component, suggesting variability in spending behavior for perishable goods.

3. **Clusters Identified**:
   - Applied K-Means clustering identified distinct customer groups based on spending habits.
   - Clusters aligned with different spending priorities (e.g., high spending on groceries vs. high spending on fresh products).

4. **Visual Patterns**:
   - PCA visualization revealed separable clusters in the reduced 2D space, making customer segmentation interpretable.

---

### **How to Reproduce This Project**

1. **Clone the Repository**:
   ```bash
   git clone <repository_link>
   cd wholesale-customers-pca
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Notebook**:
   ```bash
   jupyter notebook wholesale_customers_pca.ipynb
   ```

4. **Dataset**:
   - Ensure the Wholesale Customers Dataset is in the working directory or update the file path in the script.

---



