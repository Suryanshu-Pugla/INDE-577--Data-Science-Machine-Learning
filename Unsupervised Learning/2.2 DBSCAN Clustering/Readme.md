### **Project: Mall Customer Segmentation Using DBSCAN**

<img src="https://github.com/user-attachments/assets/7790bc21-b87a-4abb-b96c-683a7d71567e" width="50%">

#### **Introduction**
This project applies the **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** algorithm to cluster customers in a shopping mall based on their annual income and spending scores. DBSCAN is a powerful clustering algorithm capable of identifying clusters of arbitrary shapes and detecting outliers, making it an excellent choice for this segmentation task.

---

### **Objective**
The primary objective of this project is to group mall customers into clusters based on their spending patterns and income levels. This segmentation provides insights into customer behavior, which can be used for targeted marketing and business decision-making.

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
   - Examined feature relationships with pair plots and correlation heatmaps.

2. **Data Preprocessing**:
   - Selected `Annual Income` and `Spending Score` as the clustering features.
   - Standardized the features using **StandardScaler** to ensure proper scaling for DBSCAN.

3. **DBSCAN Implementation**:
   - Applied DBSCAN with initial parameters (`eps=0.3`, `min_samples=5`).
   - Identified clusters and noise points (-1 labels).

4. **Parameter Tuning**:
   - Generated a **k-distance plot** to find the optimal `eps` value.
   - Adjusted `min_samples` to fine-tune clustering results.

5. **Evaluation**:
   - Evaluated clustering performance using the **Silhouette Score**.
   - Visualized the resulting clusters and noise points.

---

### **Results**
1. **Clusters**:
   - Identified multiple customer clusters based on income and spending behavior.
   - Noise points (`-1`) represented outliers or customers that did not fit into any cluster.

2. **Silhouette Score**:
   - The clustering achieved a **Silhouette Score of 0.56**, indicating moderate separation between clusters.

3. **Visualization**:
   - Plotted clusters with distinct colors and noise points separately.

---

### **Key Insights**
- **Cluster Characteristics**:
  - High-income, high-spending customers.
  - Low-income, low-spending customers.
  - Moderate-income, varied-spending customers.
- **Noise Points**:
  - Represented unusual or outlier customer behavior.

---

### **Challenges and Solutions**

1. **Choosing Optimal Parameters**:
   - Used a k-distance plot to determine the best `eps` value.
   - Adjusted `min_samples` based on dataset density.

2. **Handling Noise**:
   - Noise points were identified and excluded from the main clusters.

3. **Interpreting Silhouette Score**:
   - While the score was moderate, it highlighted room for improvement in parameter tuning.

---

### **How to Reproduce This Project**

1. Clone the repository:
   ```bash
   git clone <repository_link>
   cd mall-customer-segmentation-dbscan
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

1. **Parameter Optimization**:
   - Automate `eps` and `min_samples` selection using grid search.

2. **Feature Engineering**:
   - Include additional features like `Age` and `Gender` for deeper insights.

3. **Advanced Clustering Algorithms**:
   - Compare DBSCAN results with other clustering techniques like **K-Means**, **OPTICS**, or **Gaussian Mixture Models**.

4. **Visualizations**:
   - Create interactive plots using libraries like **Plotly** for better interpretation.

---

### **Conclusion**
The project successfully demonstrated the application of DBSCAN for customer segmentation. It highlighted the algorithm’s ability to identify clusters of arbitrary shapes and detect outliers. The insights gained can aid in personalized marketing strategies and improved customer engagement.

---




