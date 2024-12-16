### **Project: Mall Customer Segmentation Using K-Means Clustering**

---

#### **Introduction**
This project applies the **K-Means Clustering** algorithm to segment customers in a shopping mall based on their spending patterns and annual income. Clustering helps identify groups of customers with similar behaviors, enabling targeted marketing strategies and better business decisions.

---

### **Objective**
The goal of this project is to group mall customers into clusters based on their annual income and spending score. This segmentation provides actionable insights for improving customer engagement and revenue generation.

---

### **Dataset Overview**
- **Name**: Mall Customer Segmentation Dataset
- **Source**: [Kaggle - Mall Customer Segmentation Dataset](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial-in-python)
- **Number of Records**: 200
- **Features**:
  - `CustomerID`: Unique identifier for each customer (not used in clustering).
  - `Gender`: Gender of the customer.
  - `Age`: Age of the customer.
  - `Annual Income (k$)`: Customer’s annual income in thousands of dollars.
  - `Spending Score (1-100)`: Score assigned by the mall based on customer behavior and spending nature.

For clustering, we use **Annual Income** and **Spending Score** as the features.

---

### **Steps in the Project**

1. **Exploratory Data Analysis (EDA)**:
   - Visualized distributions of `Annual Income` and `Spending Score` using histograms.
   - Examined feature relationships using scatter plots.

2. **Data Preprocessing**:
   - Selected `Annual Income` and `Spending Score` as features for clustering.
   - Standardized the features using **StandardScaler** to ensure proper scaling for K-Means.

3. **Determine Optimal Number of Clusters**:
   - Used the **Elbow Method** to find the optimal number of clusters by plotting the Within-Cluster Sum of Squares (WCSS) for different values of `k`.

4. **Apply K-Means Clustering**:
   - Implemented the K-Means algorithm with the optimal number of clusters (`k=5`).
   - Assigned cluster labels to each data point.

5. **Visualize Clusters**:
   - Plotted clusters with distinct colors and marked centroids.

6. **Evaluation**:
   - Computed the **Silhouette Score** to evaluate clustering performance.

---

### **Results**

1. **Clusters Identified**:
   - Five distinct customer clusters:
     - High-income, high-spending customers.
     - Low-income, low-spending customers.
     - Moderate-income, moderate-spending customers.
     - High-income, low-spending customers.
     - Low-income, high-spending customers.

2. **Silhouette Score**:
   - Achieved a Silhouette Score of **0.55**, indicating well-separated clusters.

3. **Visualization**:
   - Created a scatter plot showing clusters in different colors, with centroids marked for each cluster.

---

### **Key Insights**

- **High-Spending Customers**:
  - Identify these customers for premium services and personalized marketing campaigns.
- **Low-Spending Customers**:
  - Design promotional offers or loyalty programs to increase engagement.
- **Moderate-Spending Customers**:
  - Target these customers with upselling opportunities.
- **Outliers**:
  - Analyze unusual customer behavior and investigate potential anomalies.

---

### **How to Reproduce This Project**

1. Clone the repository:
   ```bash
   git clone <repository_link>
   cd mall-customer-segmentation-kmeans
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook mall_customer_segmentation.ipynb
   ```

---

### **Future Improvements**

1. **Feature Engineering**:
   - Include additional features like `Age` and `Gender` for more nuanced segmentation.

2. **3D Visualization**:
   - Extend the clustering analysis to three dimensions for better interpretation.

3. **Compare Algorithms**:
   - Compare K-Means with other clustering algorithms like **DBSCAN** or **Gaussian Mixture Models**.

4. **Interactive Dashboards**:
   - Build interactive visualizations using tools like **Plotly** or **Dash**.

---

### **Conclusion**
The K-Means clustering algorithm successfully segmented mall customers into five distinct clusters based on their income and spending habits. This segmentation provides actionable insights for targeted marketing strategies and improving customer satisfaction. The project highlights the versatility of K-Means for business applications.

---



