# 🧠 Real vs AI-Generated Fake Image Classification

### Detecting Synthetic Images Using Deep Learning and MobileNetV3Small

**Python** • **TensorFlow** • **Keras** • **MobileNetV3Small** • **Transfer Learning** • **CNN** • **Scikit-learn**

---

## 📖 About the Project

The rapid development of Artificial Intelligence has made it possible to generate highly realistic images using AI models. These AI-generated images can sometimes be difficult to distinguish from real images through manual inspection.

This project presents a Deep Learning-based image classification system that classifies images into two categories:

- 🖼️ **REAL**
- 🤖 **AI-GENERATED FAKE**

The project uses **MobileNetV3Small**, a lightweight and efficient Convolutional Neural Network (CNN), combined with **Transfer Learning** using ImageNet-pretrained weights.

The model learns visual patterns such as:

- Edges
- Colors
- Textures
- Shapes
- Artificial patterns
- Pixel-level visual characteristics

These learned features are used to classify images as either Real or AI-Generated Fake.

---

## 🎯 Problem Statement

With the increasing use of Generative AI, AI-generated images are becoming increasingly realistic and difficult to identify manually.

Traditional visual inspection may not always be reliable. Therefore, an automated system is required to analyze visual patterns and classify images as either real or AI-generated.

This project addresses this problem using a lightweight Deep Learning model based on **MobileNetV3Small**.

---

## 📊 Dataset

This project uses the CIFAKE dataset, which contains approximately 120,000 images belonging to two classes:

- 🖼️ REAL
- 🤖 AI-GENERATED FAKE

```text
          CIFAKE Dataset
          │
          ├── REAL
          └── AI-GENERATED FAKE
```
The images are resized to:
- 32 × 32 pixels
- 3 RGB channels

---

## ✨ Features

### 🖼️ Image Classification

The model classifies images into:

- ✅ REAL
- 🤖 AI-GENERATED FAKE

### 🧠 Deep Learning Model

- MobileNetV3Small CNN architecture
- ImageNet-pretrained weights
- Transfer Learning
- Custom classification head
- Binary image classification

### ⚡ Lightweight Architecture

- Fewer parameters compared to large CNN models
- Lower computational cost
- Faster training and inference
- Suitable for resource-constrained environments

### 📊 Model Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────────────┐
                    │        CIFAKE Dataset       │
                    │    Real + AI-Generated      │
                    │           Images            │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │       Image Preprocessing   │
                    │                             │
                    │   Resize Images to 32 × 32  │
                    │   MobileNetV3 Preprocessing │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │      MobileNetV3Small       │
                    │    ImageNet Pretrained CNN  │
                    │       Feature Extraction    │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │       Custom Classifier     │
                    │                             │
                    │   Batch Normalization       │
                    │   Dense Layer - 256 Neurons │
                    │   Dropout - 40%              │
                    │   Dense Layer - 64 Neurons  │
                    │   Sigmoid Output            │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │       Final Prediction      │
                    │                             │
                    │   REAL / AI-GENERATED FAKE  │
                    └─────────────────────────────┘
```
---
### 🧠 Model Architecture

The project uses MobileNetV3Small as the backbone feature extractor.

```text
Input Image
     │
     ▼
32 × 32 × 3 Image
     │
     ▼
MobileNetV3Small (ImageNet Pretrained Weights)
     │
     ▼
Feature Extraction
     │
     ▼
Global Max Pooling
     │
     ▼
Batch Normalization
     │
     ▼
Dense Layer — 256 Neurons + ReLU
     │
     ▼
Dropout — 40%
     │
     ▼
Dense Layer — 64 Neurons + ReLU
     │
     ▼
Output Layer — 1 Neuron + Sigmoid
     │
     ▼
REAL / FAKE
```
---

### 🔄 Transfer Learning

Pretrained ImageNet weights are used to initialize MobileNetV3Small, allowing the model to leverage previously learned visual features and fine-tune them for the real-vs-fake classification task.

---

### 📂 Project Structure

```text
Real-vs-Fake-Image-Classification/
│
├── Project Code/
│   │
│   ├── Batch-128/
│   │
│   ├── Batch-16/
│   │
│   ├── Batch-32/
│   │
│   ├── Batch-64/
│   │
│   └── Batch Sizes
│
└── README.md
```
---

### 🛠️ Tech Stack

- Programming Language : Python
- Deep Learning : TensorFlow, Keras, MobileNetV3Small, Convolutional Neural Networks (CNN), Transfer Learning
- Data Processing :NumPy, Visualization, Matplotlib, Seaborn
- Model Evaluation : Scikit-learn
- Development Environment : Kaggle Notebook, Jupyter Notebook
- Version Control : Git, GitHub
---

### 📚 Learning Outcomes

This project strengthened practical knowledge in:

- Deep Learning
- Convolutional Neural Networks
- Transfer Learning
- MobileNetV3 Architecture
- Image Classification
- TensorFlow and Keras
- Model Fine-Tuning
- Regularization
- Hyperparameter Selection
- Early Stopping
- Model Evaluation
- Confusion Matrix Analysis
- Precision and Recall
- F1-Score

---

