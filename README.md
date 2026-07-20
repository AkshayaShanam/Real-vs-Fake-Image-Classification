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
