### **README: Image Compression Using Singular Value Decomposition (SVD)**

---

### **Project Overview**
This project demonstrates the application of **Singular Value Decomposition (SVD)** for compressing grayscale images using the **Fashion MNIST dataset**. SVD is used to decompose an image into its singular values and reconstruct it with reduced dimensions, balancing compression efficiency and reconstruction quality.

---

### **Dataset Overview**

#### **Fashion MNIST Dataset**
- **Source**: [Fashion MNIST](https://keras.io/api/datasets/fashion_mnist/)
- **Description**: A dataset of grayscale images (28x28 pixels) of 10 different fashion categories, such as T-shirts, shoes, and bags.
- **Size**: 60,000 training images and 10,000 test images.

---

### **Steps in the Project**

#### **1. Load the Dataset**
- The Fashion MNIST dataset is loaded using TensorFlow/Keras.
- A single grayscale image is selected from the dataset for demonstration.

#### **2. Apply SVD**
- Singular Value Decomposition is applied to decompose the image into three matrices:
  - **U**: Left singular vectors.
  - **Σ**: Singular values.
  - **Vᵀ**: Right singular vectors.

#### **3. Reconstruct Image Using Top-κ Singular Values**
- Images are reconstructed using a subset of the singular values (κ) to demonstrate the trade-off between compression and quality.

#### **4. Batch Processing**
- Multiple images from the dataset are compressed and their average reconstruction error is calculated for different κ-values.

#### **5. Evaluate Reconstruction Quality**
- Reconstruction errors are computed using the Frobenius norm.
- Singular values are visualized to show their contribution to the image's variance.

---

### **Graphs and Visualizations**

#### **1. Original and Reconstructed Images**
Below is a comparison of the original image and reconstructed images for different κ-values:

![Original and Reconstructed Images](path/to/reconstructed_images.png)

#### **2. Singular Values**
The plot below shows the singular values of the image, highlighting the rapid decay of values:

![Singular Values](path/to/singular_values_plot.png)

#### **3. Reconstruction Error vs. κ**
The trade-off between κ (number of singular values) and reconstruction error is shown here:

![Reconstruction Error Plot](path/to/reconstruction_error_plot.png)

---

### **Key Insights**

1. **Dimensionality Reduction**:
   - The majority of the image's variance is captured by the first few singular values.
   - For example, using only 20 singular values (κ = 20), the reconstruction error is significantly reduced.

2. **Compression Quality Trade-Off**:
   - Lower κ-values result in higher compression but lower quality.
   - At κ = 50, the images are reconstructed perfectly due to the dataset's small size (28x28 pixels).

3. **Singular Value Distribution**:
   - Singular values decay rapidly, confirming that most of the information is concentrated in the first few components.

---

### **How to Run the Project**

1. **Clone the Repository**:
   ```bash
   git clone <repository_link>
   cd svd-image-compression
   ```

2. **Install Dependencies**:
   ```bash
   pip install numpy matplotlib tensorflow
   ```

3. **Run the Script**:
   ```bash
   python svd_image_compression.py
   ```
4. Dataset:
    Ensure the Wholesale Customers Dataset is in the working directory or update the file path in the script.
---

### **Next Steps**

1. **Batch Processing**:
   - Extend the analysis to compress a larger set of images and calculate average reconstruction errors.

2. **Color Image Compression**:
   - Apply SVD to RGB images by processing each color channel separately.

3. **Interactive Visualization**:
   - Build a dynamic dashboard using tools like Plotly or Streamlit to adjust κ-values and visualize changes in real time.

4. **Comparison with JPEG**:
   - Compare SVD-based compression with standard JPEG compression techniques.

---




