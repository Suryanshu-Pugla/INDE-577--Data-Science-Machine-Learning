# **DBSCAN Clustering from Scratch**

This project demonstrates the implementation of the **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** algorithm from scratch in Python. The algorithm is applied to the **make_moons dataset**, a synthetic dataset widely used for testing clustering methods.

---

## **Overview**

DBSCAN is a density-based clustering algorithm that:
- Groups points into clusters based on density.
- Automatically detects and labels outliers (noise points).
- Does not require the number of clusters (`k`) to be predefined.

### **Key Concepts**:
1. **Core Points**:
   - Points with at least `min_samples` neighbors within a distance `eps`.
2. **Border Points**:
   - Points within the `eps` radius of a core point but do not have enough neighbors to qualify as core points themselves.
3. **Noise Points**:
   - Points that do not belong to any cluster are identified as noise.

---

## **Algorithm Steps**

1. **Neighborhood Query**:
   - For a given point, find all points within the `eps` radius.

2. **Cluster Expansion**:
   - Start from a core point and iteratively expand the cluster by adding all reachable core points and border points.

3. **Noise Detection**:
   - Points not reachable from any cluster are labeled as noise (`-1`).

4. **Cluster Assignment**:
   - Assign unique cluster IDs to connected core points and their associated border points.

---

## **Dataset**

### **make_moons Dataset**
The **make_moons dataset** is a synthetic dataset that generates two interleaving half-circle clusters, making it ideal for testing clustering algorithms.

### **Dataset Features**:
- **Feature 1**: X-coordinate of the point.
- **Feature 2**: Y-coordinate of the point.

### **Dataset Generation**:
The dataset is created using the `make_moons` function from Scikit-learn:
```python
from sklearn.datasets import make_moons
X, y = make_moons(n_samples=300, noise=0.05, random_state=42)
