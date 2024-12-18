# **DBSCAN Clustering from Scratch**

This project demonstrates the implementation of the **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** algorithm from scratch using Python. The goal is to cluster data points based on density while identifying noise points.

---

## **Project Overview**

DBSCAN is a density-based clustering algorithm that groups data points based on their proximity and density. Unlike K-Means, DBSCAN does not require the number of clusters to be specified in advance and can identify **outliers (noise)** naturally.

### **Key Features of DBSCAN**:
1. **Core Points**: Points with at least `min_samples` neighbors within a distance `eps`.
2. **Border Points**: Points within `eps` distance of a core point but with fewer than `min_samples` neighbors.
3. **Noise Points**: Points that do not belong to any cluster.

---

## **Dataset**

### **Mall Customer Segmentation Dataset**
The dataset contains customer information:
- **Annual Income (k$)**: Annual income of the customer in thousands of dollars.
- **Spending Score (1-100)**: A score assigned to the customer based on their spending habits.

### **Features Used**:
- **Annual Income (k$)**
- **Spending Score (1-100)**

### **Source**:
- [Mall Customers Dataset on Kaggle](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial-in-python)

---

## **Steps in the Project**

### **1. Data Preprocessing**
- **Selected Features**: Chose **Annual Income (k$)** and **Spending Score (1-100)** as features for clustering.
- **Standardization**: Scaled the features using **StandardScaler** to ensure equal treatment of all dimensions.

### **2. DBSCAN Clustering**
- **Implemented DBSCAN from scratch**:
  - Identified core points, border points, and noise points.
  - Used parameters:
    - `eps=0.5`: Maximum radius for neighborhood points.
    - `min_samples=5`: Minimum points required to form a dense region.
- Cluster labels were assigned to each data point, with noise points labeled as `-1`.

### **3. Visualization**
- Plotted the clusters with noise points clearly marked.
- Used different colors to represent different clusters and noise points.

### **4. Results Analysis**
- Counted the number of clusters formed and identified noise points.

---

## **Results**

1. **Clusters Identified**:
   - DBSCAN automatically determined the number of clusters based on density.

2. **Noise Points**:
   - Noise points that do not belong to any cluster were identified and labeled as `-1`.

3. **Visualization**:
   - Clusters were displayed in different colors.
   - Noise points were marked distinctly.

---

## **Visualizations**

1. **DBSCAN Clustering Plot**  
   ![Clustering Plot](image_path.png)  
   *Clusters based on Annual Income and Spending Score.*

---

## **Key Insights**

1. **Automatic Cluster Detection**:
   - DBSCAN identifies clusters without requiring the number of clusters to be predefined.

2. **Outlier Detection**:
   - Noise points that do not belong to any dense region were successfully detected.

3. **Impact of Parameters**:
   - Tuning `eps` and `min_samples` significantly influenced the clustering results and the number of noise points.

---

## **How to Run**

1. **Setup Environment**:
   Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib scikit-learn

