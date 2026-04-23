# Atm-Fraud-Detection-System
# 🏧 ATM Fraud Detection System

A **Deep Learning-based ATM Fraud Detection System** that uses a Multi-Layer Perceptron (Neural Network) combined with advanced data preprocessing techniques to detect fraudulent ATM transactions with high accuracy.

---

## 📌 Project Overview

ATM fraud is a major cybersecurity threat in the banking sector. This project builds an intelligent fraud detection pipeline that analyzes transaction patterns across multiple data sources, handles class imbalance using SMOTE, and classifies transactions as **fraudulent or legitimate** using a Deep Neural Network.

### Key Highlights:
| Feature | Detail |
|---|---|
| 🧠 Model | Deep Neural Network (MLP) — TensorFlow/Keras |
| ⚖️ Class Imbalance | Handled using SMOTE oversampling |
| 📊 Feature Sources | Geo scores, instance data, queue sets, lambda groups |
| 🔢 Feature Scaling | StandardScaler normalization |
| 📁 Output | Final predictions exported to Excel |

---

## 🗂️ Project Structure

```
atm_fraud_detection/
├── ATM_Fraud_Detection_.ipynb           # Main Jupyter Notebook
├── bank_transactions_data_2.csv         # Transaction dataset
└── ATM-FRAUD-DETECTION-SYSTEM.pptx     # Project presentation
```

---

## 🔄 Project Pipeline

```
Raw Data → Data Cleaning → Feature Engineering → Merging →
Feature Scaling → SMOTE Balancing → Train/Test Split →
Neural Network → Prediction → Excel Output
```

### Step-by-Step:

**1. Data Loading & Exploration**
- Loaded multiple data sources: `geo`, `lambda`, `qset`, `instance`
- Explored value counts, null values, and outliers using boxplots

**2. Data Cleaning**
- Detected missing values in `geo_score` and `qsets_normalized_tat`
- Imputed nulls using **median** values
- Removed outliers

**3. Feature Engineering**
- Grouped data by `id` and merged all sources into one master dataset
- Combined train and test data for unified preprocessing

**4. Handling Class Imbalance**
- Target variable was **highly imbalanced**
- Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance classes

**5. Feature Scaling**
- Applied **StandardScaler** to normalize all features

**6. Model Architecture**
```
Input Layer
    ↓
Dense(50, activation='relu')    ← Hidden Layer 1
    ↓
Dense(10, activation='relu')    ← Hidden Layer 2
    ↓
Dense(1, activation='sigmoid')  ← Output Layer (Fraud / Not Fraud)
```

**7. Model Training**
- Optimizer: **Adam**
- Loss: **Binary Crossentropy**
- Epochs: **10**
- Batch Size: **100**
- Validation split included during training

**8. Evaluation**
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)
- Accuracy Score

**9. Output**
- Final predictions saved to `final_test_outcome.xlsx`

---

## 🚀 How to Run

### Prerequisites
```bash
pip install numpy pandas seaborn scikit-learn imbalanced-learn tensorflow openpyxl
```

### Run the Notebook
1. Open **Jupyter Notebook** or **Google Colab**
2. Upload `ATM_Fraud_Detection_.ipynb` and `bank_transactions_data_2.csv`
3. Run all cells in order (`Kernel` → `Restart & Run All`)
4. Final output will be saved as `final_test_outcome.xlsx`

---

## 🛠️ Technologies Used

| Library | Purpose |
|---|---|
| NumPy & Pandas | Data manipulation |
| Seaborn | Data visualization |
| Scikit-learn | Preprocessing, metrics |
| Imbalanced-learn | SMOTE for class balancing |
| TensorFlow / Keras | Deep Neural Network |
| OpenPyXL | Excel export |

---

## 🔐 Security & ML Concepts Covered

- Fraud Detection & Financial Security
- Deep Neural Networks (MLP)
- SMOTE for Imbalanced Datasets
- Feature Engineering & Multi-source Data Merging
- Binary Classification
- Model Evaluation (Confusion Matrix, F1-Score)

---

## 👩‍💻 Author

**Zoha Shakeel**  
BS Information Technology — NUTECH, Islamabad  
Cybersecurity & Software Development

---

## 📝 License

© 2025 — All Rights Reserved
