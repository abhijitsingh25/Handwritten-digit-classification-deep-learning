# 🖋️ Handwritten Digit Classification using TensorFlow

This project demonstrates how to build, train, and evaluate a simple **neural network** for classifying handwritten digits from the **MNIST dataset** using **TensorFlow** and **Keras**.

---

## 📌 Project Overview

The MNIST dataset consists of **70,000 grayscale images** of handwritten digits (0–9), each of size **28×28 pixels**.  
Our goal is to train a neural network that can correctly classify these digits.

---

## 📚 Dataset

- **Training Data:** 60,000 images  
- **Testing Data:** 10,000 images  
- **Image Size:** 28 × 28 (flattened to 784 for the neural network)  
- **Number of Classes:** 10 (digits 0–9)

---

## 🧰 Libraries Used

- [TensorFlow](https://www.tensorflow.org/)
- [Keras](https://keras.io/)
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)

---

## ⚙️ Steps Followed

### 1. **Data Loading & Exploration**
- Loaded MNIST dataset directly from `keras.datasets`.
- Explored the shape and structure of the training data.
- Visualized sample images using `matplotlib`.

### 2. **Data Preprocessing**
- Normalized pixel values to the range **[0, 1]** by dividing by 255.
- Flattened 28×28 images into 1D vectors of length 784.

### 3. **Model 1 – Basic Neural Network**
- **Architecture:**  
  - 1 Dense layer with 10 neurons and **sigmoid** activation.
- **Loss:** Sparse Categorical Crossentropy  
- **Optimizer:** Adam  
- **Epochs:** 5
- **Training Accuracy:** ~92.5%  
- **Test Accuracy:** ~92.5%

### 4. **Evaluation & Predictions**
- Evaluated on test dataset.
- Generated predictions and visualized a **confusion matrix** using Seaborn’s heatmap.
- Observed most predictions along the diagonal, indicating good model performance.

### 5. **Model 2 – Improved Neural Network**
- **Architecture:**  
  - Dense(100, activation='relu')  
  - Dense(10, activation='sigmoid')
- **Epochs:** 5
- **Training Accuracy:** ~98.4%  
- **Test Accuracy:** ~97.3%

This improved model shows a significant accuracy boost thanks to the added hidden layer with ReLU activation.

---

## 📊 Confusion Matrix

A confusion matrix was plotted to analyze model performance:

- Most values lie along the diagonal — indicating correct classifications.
- Misclassifications were mostly between similar-looking digits (e.g., 3 and 5).

---

## 🚀 How to Run

1. Clone this repository or download the notebook.
2. Install dependencies:
   ```bash
   pip install tensorflow numpy matplotlib seaborn
3. Run the notebook:
   jupyter notebook
4. Open the notebook file and execute the cells sequentially.
5.   
