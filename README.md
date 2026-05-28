<div align="center">

# Neural Network vs Support Vector Machine

### Analisis Komparatif pada Dataset MNIST dan FashionMNIST

<p align="center">
Implementasi dan Perbandingan Model Machine Learning menggunakan PyTorch dan Scikit-learn
</p>

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-CUDA%2012.6-red?style=for-the-badge&logo=pytorch)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-SVM-orange?style=for-the-badge&logo=scikitlearn)
![Status](https://img.shields.io/badge/Project-Selesai-success?style=for-the-badge)

</div>

---

# Gambaran Umum Proyek

Proyek ini dikembangkan sebagai tugas mata kuliah **Data Mining** dengan tujuan membandingkan performa algoritma **Neural Network** dan **Support Vector Machine (SVM)** pada tugas klasifikasi citra menggunakan dataset **MNIST** dan **FashionMNIST**.

Implementasi difokuskan pada evaluasi performa klasifikasi menggunakan berbagai metrik evaluasi machine learning serta analisis terhadap kekuatan dan kelemahan masing-masing model dan konfigurasi kernel.

Proyek ini memanfaatkan:

- PyTorch dengan akselerasi CUDA
- Scikit-learn SVM
- Workflow modular berbasis Jupyter Notebook
- Visualisasi menggunakan Matplotlib
- Analisis Confusion Matrix

---

# Dataset

## MNIST

- Dataset digit tulisan tangan
- 10 kelas (0–9)
- Citra grayscale berukuran 28×28

## FashionMNIST

- Dataset citra fashion
- 10 kategori pakaian
- Citra grayscale berukuran 28×28

---

# Model yang Digunakan

## Neural Network

| Model | Arsitektur                          |
| ----- | ----------------------------------- |
| NN-1  | 784 → 128 → 10                      |
| NN-2  | 784 → 256 → Dropout(0.3) → 128 → 10 |

### Konfigurasi Neural Network

- Activation Function: ReLU
- Optimizer: Adam
- Loss Function: CrossEntropyLoss
- Framework: PyTorch CUDA

---

## Support Vector Machine (SVM)

Kernel yang digunakan:

- Linear
- Polynomial
- RBF
- Sigmoid

### Konfigurasi SVM

- Normalisasi menggunakan StandardScaler
- Implementasi menggunakan Scikit-learn SVC

---

# Metrik Evaluasi

Model dievaluasi menggunakan:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

# Hasil Terbaik

| Dataset      | Model Terbaik         | F1-score |
| ------------ | --------------------- | -------- |
| MNIST        | Neural Network (NN-2) | 0.9808   |
| FashionMNIST | Neural Network (NN-1) | 0.8802   |

> Kernel terbaik pada SVM: **RBF Kernel**

---

# Perbandingan Model

## Grafik Perbandingan F1-score

![Comparison Chart](results/comparison_chart.png)

---

# Analisis Confusion Matrix

## FashionMNIST - Neural Network Terbaik (NN-1)

![FashionMNIST NN](results/confusion_matrix/fashionmnist_best_neural_network_cm.png)

---

## FashionMNIST - Performa SVM Terendah (Sigmoid)

![FashionMNIST SVM Sigmoid](results/confusion_matrix/fashionmnist_svm_sigmoid_cm.png)

---

## MNIST - Neural Network Terbaik (NN-2)

![MNIST NN](results/confusion_matrix/mnist_best_neural_network_cm.png)

---

## MNIST - Kernel SVM Terbaik (RBF)

![MNIST SVM RBF](results/confusion_matrix/mnist_svm_rbf_cm.png)

---

## MNIST - Performa SVM Terendah (Sigmoid)

![MNIST SVM Sigmoid](results/confusion_matrix/mnist_svm_sigmoid_cm.png)

---

# Ringkasan Analisis

Berdasarkan hasil eksperimen yang dilakukan:

- Neural Network memperoleh performa terbaik pada kedua dataset.
- Model NN-2 menghasilkan performa tertinggi pada MNIST dengan F1-score sebesar 0.9808.
- Model NN-1 menghasilkan performa terbaik pada FashionMNIST dengan F1-score sebesar 0.8802.
- Pada kelompok SVM, kernel RBF secara konsisten mengungguli kernel Linear, Polynomial, dan Sigmoid.
- Kernel Sigmoid menghasilkan performa klasifikasi paling rendah, terutama pada FashionMNIST.
- Dataset FashionMNIST memiliki tingkat kesulitan klasifikasi yang lebih tinggi karena kemiripan visual antar kategori pakaian.

---

# Detail Teknis

<details>
<summary>Detail Training Neural Network</summary>

### Hyperparameter

- Epoch: 10
- Batch Size: 64
- Learning Rate: 0.001

### Framework

- PyTorch
- CUDA 12.6
- GPU Acceleration Enabled

</details>

<details>
<summary>Detail Kernel SVM</summary>

### Kernel yang Digunakan

- Linear
- Polynomial (degree=3)
- RBF
- Sigmoid

### Preprocessing

- Normalisasi menggunakan StandardScaler
- Flatten citra menjadi 784 fitur

</details>

<details>
<summary>Spesifikasi Perangkat</summary>

### Sistem

- AMD Ryzen 7 6800H
- NVIDIA GeForce RTX 3050 Laptop GPU
- RAM 16 GB

</details>

---

# Struktur Proyek

```bash
UTS_Data_Mining/
│
├── models/
│
├── notebooks/
│   ├── 01_setup_and_dataset.ipynb
│   ├── 02_train_neural_network.ipynb
│   ├── 03_train_svm.ipynb
│   └── 04_evaluation_and_comparison.ipynb
│
├── results/
│   ├── comparison_chart.png
│   ├── nn_results.csv
│   ├── svm_results.csv
│   ├── metrics_results.csv
│   └── confusion_matrix/
│
├── README.md
├── requirements.txt
└── .gitignore
```
