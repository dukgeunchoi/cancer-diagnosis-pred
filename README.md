# Cancer Diagnosis Prediction using Deep Learning

A binary classification project that predicts whether a breast cancer diagnosis is **malignant (M)** or **benign (B)** using neural networks.  
Built in Python using **TensorFlow/Keras**, this project compares the performance of deep learning models against a logistic regression baseline using the **Wisconsin Breast Cancer Dataset**.

---

## 📊 Problem Overview

The model is trained to classify tumors as malignant or benign based on 30 features extracted from digitized images of fine needle aspirates (FNA). These features represent various characteristics of the cell nuclei such as radius, texture, perimeter, area, smoothness, and concavity.

---

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic))
- **Rows**: 569 samples
- **Features**: 30 numerical features
- **Target**: `diagnosis` — Benign (B) or Malignant (M)

---

## 🔧 Preprocessing

- Dropped irrelevant columns (e.g. ID)
- Label encoded the target variable (M = 1, B = 0)
- Normalized features using `StandardScaler`
- Applied `SMOTE` to balance class distribution
- Split dataset into **train (60%) / val (20%) / test (20%)**

---

## 🧪 Models

### ✅ Benchmark Model
- **Logistic Regression**
- Baseline performance: ~96% accuracy

### 🤖 Deep Learning Models

#### 1. Dense Sequential Model
- Feedforward neural network using Keras
- Tuned layers, neurons, activation functions, dropout, and learning rate
- Early stopping used to prevent overfitting

#### 2. Wide and Deep Model
- Combines a shallow linear path with a deep neural network
- Captures both linear and nonlinear relationships
- Tuned similarly to the dense model

---

## 📈 Best Performance

| Model               | Accuracy | Precision | Recall | F1-Score |
|--------------------|----------|-----------|--------|----------|
| Logistic Regression|   0.96   |    1.00   |  0.91  |   0.95   |
| Dense Model (DL)   |   0.98   |    0.99   |  0.97  |   0.98   |
| Wide & Deep (DL)   |   0.98   |    0.99   |  0.97  |   0.98   |

---

## ⚠️ Ethical Considerations

- **Data privacy**: Breast cancer diagnosis data is sensitive; proper consent is needed for real-world use.
- **Accountability**: Responsibility for model misclassification in clinical settings must be clearly defined.

