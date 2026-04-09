# Breast-Cancer-Busi-Mobilenet

# Breast Ultrasound Classification & Depthwise-Pointwise CNN (BUSI Dataset)

## 📌 Overview

This project focuses on classifying breast ultrasound images into three categories — **Benign, Malignant, and Normal** — using a custom deep learning model. Along with classification, the project also demonstrates the working of **depthwise and pointwise convolutions**, which are key components of efficient architectures like MobileNet.

---

## 🎯 Objective

* Develop an automated system for breast ultrasound image classification
* Implement a custom CNN using depthwise separable convolution
* Understand and demonstrate the role of depthwise and pointwise operations

---

## 📂 Dataset

* **Dataset:** BUSI (Breast Ultrasound Images Dataset)
* **Source:** Kaggle
* **Classes:** Benign, Malignant, Normal

Mask images provided in the dataset are excluded during preprocessing, and only original ultrasound images are used.

---

## ⚙️ Methodology

### 🔹 Data Preprocessing

* Removed mask images
* Resized images to **128 × 128**
* Normalized pixel values (0–1)
* Converted grayscale images to 3-channel format

---

### 🔹 Dataset Splitting

* **Training:** 70%
* **Validation:** 15%
* **Testing:** 15%

---

### 🔹 Model Architecture

A custom convolutional neural network is designed using:

* Initial convolution layer
* Multiple **depthwise + pointwise convolution blocks**
* Batch normalization and ReLU activation
* Global average pooling
* Fully connected layers
* Softmax output layer (3 classes)

---

### 🔹 Depthwise & Pointwise Convolution

#### Depthwise Convolution

* Applies a separate **3×3 filter to each input channel**
* Extracts spatial features such as edges and textures

#### Pointwise Convolution

* Uses **1×1 convolution**
* Combines information across channels
* Reduces computational complexity

Together, these form a **depthwise separable convolution**, improving efficiency compared to standard convolution.

---

### 🔹 Training Configuration

* **Optimizer:** Adam
* **Learning Rate:** 0.0001
* **Loss Function:** Cross Entropy Loss
* **Epochs:** 10
* **Batch Size:** 16

---

## 🧠 Conclusion

This project demonstrates that deep learning can effectively classify breast ultrasound images into clinically relevant categories. The use of depthwise and pointwise convolutions provides an efficient alternative to standard convolution while maintaining learning capability. The approach highlights how lightweight architectures can be applied to medical imaging tasks for faster and scalable solutions. Overall, the system shows the potential of combining efficient CNN design with medical datasets for practical diagnostic support.
