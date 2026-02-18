# Federated-Learning-XAI-Bone-Fracture-Classification
Privacy-preserving Federated Learning framework for Bone Fracture Classification using DenseNet121, enhanced with Explainable AI (Grad-CAM++, Guided Backpropagation, Occlusion Sensitivity) for model interpretability, bias diagnosis, and clinically trustworthy predictions.

# 🩻 Federated Learning with Explainable AI (XAI) for Bone Fracture Classification

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![Federated Learning](https://img.shields.io/badge/Paradigm-FederatedLearning-success)
![XAI](https://img.shields.io/badge/AI-ExplainableAI-purple)
![Status](https://img.shields.io/badge/Project-Academic-brightgreen)

---

## 📌 Project Overview

This project presents a **privacy-preserving Federated Learning (FL) framework** for **bone fracture detection using X-ray images**, enhanced with **Explainable AI (XAI)** techniques to improve interpretability and clinical trust.

A **DenseNet121 deep learning model** was trained under:

✔ Centralized (baseline) setup  
✔ Federated Learning setup across **3 simulated hospital clients**

To ensure transparency and reliability, the system integrates:

- 🔥 Grad-CAM++
- 🧠 Guided Backpropagation
- 🧩 Occlusion Sensitivity Mapping

These XAI techniques visually explain model decisions by highlighting clinically relevant fracture regions.

---

## 🎯 Objectives

- Develop a **Federated Learning system** for medical image classification
- Compare **centralized vs federated performance**
- Improve baseline DenseNet121 using **custom architectural enhancements**
- Apply **Explainable AI (XAI)** for interpretability
- Analyze **Dependent vs Independent Federated Learning**

---

## 🩻 Dataset Details

**Task:** Binary Bone Fracture Classification  
**Classes:** Fracture / Non-Fracture  

**Total Images:** 10,580 X-ray images  

| Split | Samples |
|------|---------|
| Training | 9,246 |
| Validation | 828 |
| Testing | 506 |

**Federated Distribution (Simulated Hospitals):**

| Client | Samples | Proportion |
|--------|---------|------------|
| Client 1 | 3,061 | 33.11% |
| Client 2 | 4,674 | 50.55% |
| Client 3 | 1,511 | 16.34% |

✔ Non-IID distribution simulated  
✔ Images resized to **224×224**  
✔ Normalization + Data Augmentation applied

---

## 🧠 Model Architectures

### ✅ Baseline DenseNet121

- ImageNet pretrained
- GlobalAveragePooling
- Dense (512, ReLU)
- Dropout (0.4)
- Sigmoid Output

**Baseline Accuracy:** **88.49%**

---

### 🚀 Optimized DenseNet121 + Custom Layers

Enhancements:

✔ Additional Dense Layers (256 → 128)  
✔ Batch Normalization  
✔ Dropout (0.3–0.4)  
✔ Residual Skip Connections  
✔ Swish + ReLU Activations  

**Optimized Accuracy:** **94%**

---

## 🌐 Federated Learning Setup

| Parameter | Value |
|----------|-------|
| Clients | 3 |
| Federated Rounds | 3 |
| Local Epochs | 2 |
| Batch Size | 32 |
| Optimizer | Adam |
| Learning Rate | 1e-4 |
| Aggregation | **FedAvg (Weighted)** |

---

## 🔁 Federated Training Strategies

### 🔹 Independent Federated Learning
- Random initialization
- Clients train from scratch

**Accuracy:** **93.48%**

---

### 🔹 Dependent Federated Learning
- Initialized with optimized baseline weights

**Accuracy:** **🏆 95% (Best Performance)**

---

## 🔍 Explainable AI (XAI) Integration

To improve **clinical interpretability and trust**:

### 🔥 Grad-CAM++
Highlights discriminative fracture regions

### 🧠 Guided Backpropagation
Pixel-level gradient visualization

### 🧩 Occlusion Sensitivity
Measures prediction sensitivity to masked regions

✔ Confirms focus on fracture zones  
✔ Detects spurious correlations  
✔ Validates medical relevance

---

## 📊 Results Summary

| Model Configuration | Accuracy |
|---------------------|----------|
| Baseline DenseNet121 (Centralized) | 88.49% |
| DenseNet121 (Federated) | 86.00% |
| Optimized DenseNet121 (Centralized) | 94.00% |
| Federated Independent (Optimized) | 93.48% |
| **Federated Dependent (Optimized)** | **🏆 95.00%** |

---

## 📉 Training Stability

The optimized federated model demonstrated:

✔ Stable convergence  
✔ Reduced training/validation loss  
✔ Improved generalization  

---

## 🧰 Technologies & Tools

- TensorFlow / Keras
- TensorFlow Federated (TFF)
- NumPy
- Matplotlib
- PIL / OpenCV
- Google Colab / Kaggle

---

## 💡 Key Contributions

✅ Federated Learning framework for medical imaging  
✅ Optimized DenseNet121 architecture  
✅ Comparative FL strategies (Dependent vs Independent)  
✅ Integration of Explainable AI (XAI)  
✅ Bias detection & interpretability validation  
✅ Reproducible deep learning pipeline  

---

## 🚀 Future Enhancements

- 🔐 Secure Aggregation
- 🛡 Differential Privacy
- 🧠 Vision Transformers (ViT)
- 🌍 Larger client simulations
- 💻 Real cross-device Federated Learning
- 📏 Quantitative XAI evaluation metrics

---

## 👥 Team Members

**Srushti Dayanand Dangi**  
B.Tech (Hons), RV University  

**Chaitanya A S**  
B.Tech (Hons), RV University  

**Gauravik S S**  
B.Tech (Hons), RV University  

**Gopika**  
B.Tech (Hons), RV University  

---

## 📄 License

This repository is developed for **academic and educational purposes**.

---

## ⭐ If you found this project interesting

Give it a ⭐ on GitHub!
