# UTS Data Mining - Neural Network vs SVM

## Deskripsi

Project UTS mata kuliah Data Mining yang membandingkan performa Neural Network dan Support Vector Machine (SVM) pada dataset MNIST dan FashionMNIST.

## Dataset

- MNIST
- FashionMNIST

## Model yang Digunakan

### Neural Network

- NN-1: 784-128-10
- NN-2: 784-256-Dropout-128-10

### Support Vector Machine

- Linear Kernel
- Polynomial Kernel
- RBF Kernel
- Sigmoid Kernel

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Environment

- Python 3.11
- PyTorch CUDA 12.6
- NVIDIA RTX 3050 Laptop GPU

## Hasil Utama

### MNIST

Best Model: Neural Network (NN-2)
F1-score: 0.9808

### FashionMNIST

Best Model: Neural Network (NN-1)
F1-score: 0.8802

## Author

Ida Bagus Gede Dhananjaya
