# 🌿 Plant Disease Detection using Deep Learning (CNN with PyTorch)

> A deep learning-based image classification system that identifies plant diseases from leaf images using a custom-built Convolutional Neural Network (CNN) implemented in PyTorch.

---

## 🚀 Project Highlights

- 🧠 Built a **CNN from scratch (no pretrained model)**
- 📊 Achieved supervised multi-class image classification on real agricultural data
- ⚙️ Implemented full ML pipeline: data loading → preprocessing → training → evaluation
- 🔥 GPU-ready training using CUDA
- 📦 Custom Dataset class built using PyTorch
- 📉 Model evaluated using accuracy and loss metrics

---

## 🎯 Problem Statement

Agricultural productivity is heavily affected by plant diseases, which often go undetected until significant damage occurs. Manual identification is slow, error-prone, and not scalable.

This project aims to automate plant disease detection using deep learning to enable fast and accurate classification of plant leaf conditions.

---

## 📂 Dataset

**PlantVillage Dataset**

🔗 https://www.kaggle.com/datasets/mohitsingh1804/plantvillage

### Dataset Overview:
- Images of plant leaves across multiple species
- Includes both healthy and diseased samples
- Structured into:
  - `train/`
  - `val/`
- Each class represents a specific plant disease or healthy condition

---

## 🧠 Model Architecture

A custom Convolutional Neural Network was designed from scratch:

### 🔹 Feature Extractor
- 4 Convolutional Blocks:
  - Conv2D → ReLU → BatchNorm → MaxPooling
- Feature depth progression:
  - 3 → 32 → 64 → 128 → 256

### 🔹 Classifier Head
- Flatten layer
- Fully connected layers:
  - 256 → 256 → 64 → num_classes
- ReLU activations
- Dropout (0.5) for regularization

---

## ⚙️ Training Pipeline

### Hyperparameters:
- Optimizer: **Adam**
- Loss Function: **CrossEntropyLoss**
- Learning Rate: `0.001`
- Batch Size: `32`
- Epochs: `5`
- Image Size: `128 × 128`

### Preprocessing:
- Image resizing
- Tensor conversion
- Normalization (mean = 0.5, std = 0.5)

---

## 📊 Performance Tracking

The model was evaluated using:

- Training Loss
- Training Accuracy
- Validation Loss
- Validation Accuracy

> The training loop includes real-time accuracy computation for both training and validation sets.

---

## 🛠️ Technical Implementation

### Key Components Built From Scratch:

- Custom PyTorch `Dataset` class
- DataLoader for batch processing
- Manual training loop
- Validation loop with `torch.no_grad()`
- GPU/CPU device handling

### Core Stack:
- Python 🐍
- PyTorch 🔥
- Torchvision
- PIL (Pillow)
- KaggleHub
- NumPy

---

## 📈 Key Learnings

This project helped strengthen my understanding of:

### 🧠 Deep Learning Fundamentals
- CNN architecture design
- Feature extraction through convolution layers
- Importance of normalization, pooling, and dropout

### ⚙️ PyTorch Engineering
- Writing custom Dataset classes
- Building training pipelines manually
- Debugging tensor shapes and model flow
- Efficient GPU utilization

### 🔬 Machine Learning Workflow
- Data preprocessing strategies for image data
- Train/validation pipeline design
- Model evaluation techniques
- Overfitting control via dropout

---

## 🔮 Future Improvements

This project can be extended into a production-level system:

### 🚀 Model Enhancements
- Replace CNN with pretrained architectures:
  - ResNet
  - EfficientNet
  - MobileNet
- Add advanced data augmentation:
  - rotation
  - flipping
  - color jitter

### 📊 Training Improvements
- Train for more epochs
- Add learning rate scheduler
- Implement early stopping
- Handle class imbalance

### 🌐 Deployment Ideas
- Web app using **Flask / FastAPI**
- Frontend interface for real-time predictions
- Mobile deployment using **TorchScript / ONNX**

---

## 🧾 Project Summary

This project demonstrates a complete end-to-end deep learning pipeline for plant disease classification using a custom CNN built from scratch. It highlights strong fundamentals in computer vision, PyTorch, and model training workflows.

It serves as a strong foundation for building real-world agricultural AI solutions.

---

## 👨‍💻 Author

Built as a personal machine learning project to strengthen deep learning and PyTorch skills.

---

## ⭐ If You Like This Project

Consider giving it a ⭐ on GitHub if you find it useful or interesting.
