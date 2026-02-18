# Federated-Learning-XAI-Bone-Fracture-Classification
Privacy-preserving Federated Learning framework for Bone Fracture Classification using DenseNet121, enhanced with Explainable AI (Grad-CAM++, Guided Backpropagation, Occlusion Sensitivity) for model interpretability, bias diagnosis, and clinically trustworthy predictions.

# 🩻 Federated Learning with Explainable AI (XAI) for Bone Fracture Classification

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![Federated Learning](https://img.shields.io/badge/Paradigm-FederatedLearning-success)
![Explainable AI](https://img.shields.io/badge/AI-Explainable-purple)
![Status](https://img.shields.io/badge/Project-Academic-brightgreen)

---

## 🩻 Project Overview

This project implements a **privacy-preserving Federated Learning (FL) framework** for **bone fracture classification using X-ray images**, enhanced with **Explainable AI (XAI)** techniques to improve model transparency and clinical trust.

A **DenseNet121 deep learning model** was trained under:

✔ Centralized (baseline) setup  
✔ Federated Learning setup across **three simulated hospital clients**

To ensure interpretability, multiple XAI techniques were integrated:

- 🔥 Grad-CAM++
- 🧠 Guided Backpropagation
- 🧩 Occlusion Sensitivity Mapping

These methods visually highlight image regions influencing the model’s predictions, validating that decisions are based on clinically relevant fracture features.

---

## 🎯 Objectives

- Develop a **Federated Learning-based medical imaging classifier**
- Compare **centralized vs federated training performance**
- Improve DenseNet121 accuracy via **architectural enhancements**
- Integrate **Explainable AI (XAI)** for interpretability
- Analyze **Dependent vs Independent Federated Learning strategies**

---

## ⚙️ Methodology

### 1️⃣ Dataset

**Dataset:** Bone Fracture Binary Classification  
**Classes:** Fracture / Non-Fracture  
**Splits:** Train / Validation / Test  

**Federated Distribution (Simulated Hospitals):**

| Client | Samples | Proportion |
|--------|---------|------------|
| Client 1 | 3,061 | 33.11% |
| Client 2 | 4,674 | 50.55% |
| Client 3 | 1,511 | 16.34% |

✔ Non-IID data distribution simulated  
✔ Images resized to **224 × 224**  
✔ Normalization + Data Augmentation applied  

---

### 2️⃣ Model Architectures

#### ✅ A. Baseline DenseNet121

- ImageNet pretrained
- GlobalAveragePooling
- Dense(128, ReLU)
- Sigmoid Output

**Baseline Accuracy:** **88.49%**

---

#### 🚀 B. Optimized DenseNet121 + Custom Layers

Enhancements:

✔ Multi-layer Dense Blocks  
✔ Batch Normalization  
✔ Dropout Regularization  
✔ Residual Skip Connections  
✔ Swish + ReLU Activations  
✔ Fine-tuning of final layers  

**Optimized Accuracy:** **94%**

---

### 3️⃣ Federated Learning Setup

| Parameter | Value |
|----------|-------|
| Clients | 3 |
| Federated Rounds | 3 |
| Local Epochs per Round | 2 |
| Aggregation | **Weighted FedAvg** |
| Optimizer | Adam |
| Learning Rate | 1e-4 |

---

### 4️⃣ Federated Training Strategies

#### 🔹 Independent Federated Learning

- Random initialization
- Clients train without baseline knowledge

**Accuracy:** **93.48%**

---

#### 🔹 Dependent Federated Learning

- Global model initialized with optimized baseline weights

**Accuracy:** **🏆 95% (Best Performance)**

---

### 5️⃣ Explainable AI (XAI) Integration

To ensure **interpretability and clinical reliability**:

#### 🔥 Grad-CAM++
Highlights discriminative fracture regions

#### 🧠 Guided Backpropagation
Visualizes pixel-level gradient influence

#### 🧩 Occlusion Sensitivity
Measures prediction sensitivity to masked regions

✔ Validates focus on fracture zones  
✔ Detects model bias  
✔ Improves clinical trust  

---

## 📊 Results Summary

| Model Configuration | Accuracy (%) |
|---------------------|-------------|
| DenseNet121 Baseline (Centralized) | 88.49 |
| DenseNet121 Federated | 86.00 |
| DenseNet121 + Custom Layers (Centralized) | 94.00 |
| Federated Independent (Optimized) | 93.48 |
| **Federated Dependent (Optimized)** | **🏆 95.00** |


---

✅ **Key Finding:**  
Dependent Federated Learning with optimized initialization achieved the **highest accuracy (95%)**, demonstrating superior convergence and knowledge aggregation.

---

## 💡 Key Contributions

✅ Privacy-preserving Federated Learning framework  
✅ Optimized DenseNet121 architecture (+6% improvement)  
✅ Comparative study of FL strategies  
✅ Integration of Explainable AI (XAI)  
✅ Bias diagnosis & interpretability validation  
✅ Reproducible end-to-end pipeline  

---

## 🧰 Technologies Used

- TensorFlow / Keras
- TensorFlow Federated (TFF)
- NumPy
- PIL / OpenCV
- Matplotlib
- Google Colab / Kaggle

---

## 📈 Future Enhancements

- 🔐 Secure Aggregation
- 🛡 Differential Privacy
- 🧠 Vision Transformers (ViT)
- 🌍 Larger client simulations
- 💻 Real cross-device Federated Learning
- 📏 Quantitative XAI evaluation metrics

---

## 👥 Team Members

**Srushti Dayanand Dangi**  
B.Tech (Hons), 3rd Year – RV University, Bangalore  

**Chaitanya A S**  
B.Tech (Hons), 3rd Year – RV University, Bangalore  

**Gauravik S S**  
B.Tech (Hons), 3rd Year – RV University, Bangalore  

**Gopika**  
B.Tech (Hons), 3rd Year – RV University, Bangalore  

---

## 📄 License

This repository is developed for **academic and educational purposes**.

---

## ⭐ Support

If you found this project interesting, consider giving it a ⭐ on GitHub!

