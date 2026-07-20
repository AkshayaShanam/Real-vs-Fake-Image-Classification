🧠 Real vs AI-Generated Fake Image Classification

Detecting Synthetic Images Using Deep Learning and MobileNetV3Small

Python • TensorFlow • Keras • MobileNetV3Small • Transfer Learning • CNN • Scikit-learn

📖 About the Project

The rapid development of Artificial Intelligence has made it possible to generate highly realistic images using AI models. These AI-generated images can sometimes be difficult to distinguish from real images and may be used to spread misinformation or misleading visual content.

This project presents a Deep Learning-based image classification system that classifies images into two categories:

🖼️ REAL
🤖 AI-GENERATED FAKE

The project uses MobileNetV3Small, a lightweight and efficient Convolutional Neural Network (CNN), combined with Transfer Learning using ImageNet-pretrained weights.

The model learns visual patterns such as:

Edges
Colors
Textures
Shapes
Artificial patterns
Pixel-level visual characteristics

and uses these features to classify an image as Real or AI-Generated Fake.

🎯 Problem Statement

With the increasing use of Generative AI, AI-generated images are becoming more realistic and difficult to identify manually.

Traditional visual inspection may not always be reliable. Therefore, there is a need for an automated system that can analyze image patterns and classify images as real or AI-generated.

This project addresses this problem using a lightweight deep learning model based on MobileNetV3Small.

✨ Features
🖼️ Image Classification
Classifies images as:
✅ REAL
🤖 AI-GENERATED FAKE
🧠 Deep Learning Model
Uses MobileNetV3Small CNN architecture
Uses ImageNet-pretrained weights
Performs transfer learning
Supports fine-tuning
⚡ Lightweight Architecture
Fewer parameters compared to large CNN models
Lower computational cost
Faster training and inference
Suitable for resource-constrained environments

🏗️ System Architecture
                    ┌─────────────────────────────┐
                    │        CIFAKE Dataset       │
                    │    Real + AI-Generated      │
                    │           Images            │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │       Image Preprocessing   │
                    │     Resize Images to 32x32  │
                    │    MobileNetV3 Preprocessing│
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
                    │ Batch Normalization         │
                    │ Dense Layer - 256 Neurons   │
                    │ Dropout - 40%                │
                    │ Dense Layer - 64 Neurons    │
                    │ Sigmoid Output              │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────────┐
                    │       Final Prediction      │
                    │                             │
                    │     REAL / AI-GENERATED     │
                    │           FAKE              │
                    └─────────────────────────────┘
🧠 Model Architecture

The project uses MobileNetV3Small as the backbone feature extractor.

Input Image
    │
    ▼
32 × 32 × 3 Image
    │
    ▼
MobileNetV3Small
(ImageNet Pretrained Weights)
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
Dense Layer
256 Neurons + ReLU
    │
    ▼
Dropout
40%
    │
    ▼
Dense Layer
64 Neurons + ReLU
    │
    ▼
Output Layer
1 Neuron + Sigmoid
    │
    ▼
REAL / FAKE
🔄 Transfer Learning

📊 Dataset

This project uses the CIFAKE dataset of 1,20,000 images, which contains two categories of images:

CIFAKE Dataset
      │
      ├── REAL
      │
      └── AI-GENERATED FAKE

The images are resized to:

32 × 32 pixels

with:

3 RGB channels

📈 Evaluation Metrics

The model is evaluated using multiple metrics.

🎯 Accuracy

Measures the overall percentage of correct predictions.

🎯 Precision

Measures how many images predicted as a particular class were actually correct.

🎯 Recall

Measures how many actual images of a class were correctly detected.

🎯 F1-Score

Provides a balance between precision and recall.

🎯 Confusion Matrix

Shows:

True Positives
True Negatives
False Positives
False Negatives

📂 Project Structure

🛠️ Tech Stack
Programming Language
Python
Deep Learning
TensorFlow
Keras
MobileNetV3Small
CNN
Transfer Learning
Data Processing
NumPy
Visualization
Matplotlib
Seaborn
Evaluation
Scikit-learn
Development Environment
Kaggle Notebook
Jupyter Notebook
Version Control
Git
GitHub
🚀 Getting Started
Clone Repository
git clone https://github.com/AkshayaShanam/Real-vs-Fake-Image-Classification.git
cd Real-vs-Fake-Image-Classification
Install Dependencies
pip install -r requirements.txt
📦 Requirements

Create a requirements.txt file containing:

numpy
matplotlib
tensorflow
seaborn
scikit-learn
ipython
🗃️ Dataset Setup

The CIFAKE dataset is not included in this repository because of its large size.

Download the dataset separately and update the dataset path in the notebook.

For Kaggle:

dataset_dir = "/kaggle/input/cifake-real-and-ai-generated-synthetic-images/"

For local execution:

dataset_dir = "path/to/cifake/dataset/"

The expected dataset structure is:

CIFAKE/

├── train/
│   ├── FAKE/
│   └── REAL/
│
└── test/
    ├── FAKE/
    └── REAL/

🔄 Project Workflow
1. Load the CIFAKE Dataset
        ↓
2. Resize Images to 32 × 32
        ↓
3. Load MobileNetV3Small
        ↓
4. Load ImageNet Pretrained Weights
        ↓
5. Extract Visual Features
        ↓
6. Add Custom Classification Layers
        ↓
7. Apply Transfer Learning
        ↓
8. Train the Model
        ↓
9. Apply Early Stopping
        ↓
10. Generate Predictions
        ↓
11. Calculate Evaluation Metrics
        ↓
12. Classify Image as REAL or FAKE

📚 Learning Outcomes

This project strengthened practical knowledge in:

Deep Learning
Convolutional Neural Networks
Transfer Learning
MobileNetV3 Architecture
Image Classification
TensorFlow and Keras
Model Fine-Tuning
Regularization
Hyperparameter Selection
Early Stopping
Model Evaluation
Confusion Matrix Analysis
Precision and Recall
F1-Score
Python
Git and GitHub
Kaggle GPU Environment

👩‍💻 Author

Shanam Akshaya

🎓 B.Tech – Computer Science & Engineering (Data Science)

📧 Email: 23211a67b1@bvrit.ac.in

🔗 GitHub: AkshayaShanam

🔗 LinkedIn: Akshaya Shanam

⭐ If you found this project helpful, please consider giving it a Star!

Thank you for visiting Real vs AI-Generated Fake Image Classification! 🤖🧠
