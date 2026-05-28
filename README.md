# UTS Data Mining - Neural Network vs SVM

## Comparative Analysis of Neural Network and Support Vector Machine on MNIST and FashionMNIST Datasets

Project UTS mata kuliah Data Mining yang bertujuan membandingkan performa algoritma Neural Network dan Support Vector Machine (SVM) pada klasifikasi citra menggunakan dataset MNIST dan FashionMNIST.

---

# Dataset

Dataset yang digunakan:

- MNIST
  - Dataset digit tulisan tangan
  - 10 kelas
  - Grayscale 28×28

- FashionMNIST
  - Dataset citra fashion
  - 10 kelas
  - Grayscale 28×28

---

# Model yang Digunakan

## Neural Network

| Model | Arsitektur                  |
| ----- | --------------------------- |
| NN-1  | 784-128-10                  |
| NN-2  | 784-256-Dropout(0.3)-128-10 |

Activation Function:

- ReLU

Optimizer:

- Adam

Loss Function:

- CrossEntropyLoss

---

## Support Vector Machine (SVM)

Kernel yang digunakan:

- Linear
- Polynomial
- RBF
- Sigmoid

---

# Evaluation Metrics

Evaluasi model menggunakan:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

# Hasil Utama

| Dataset      | Best Model            | F1-score |
| ------------ | --------------------- | -------- |
| MNIST        | Neural Network (NN-2) | 0.9808   |
| FashionMNIST | Neural Network (NN-1) | 0.8802   |

Kernel terbaik pada SVM:

- RBF Kernel

---

# Perbandingan F1-score Model

![Comparison Chart](results/comparison_chart.png)

---

# Struktur Project

```bash
UTS_Data_Mining/
│
├── notebooks/
├── results/
├── models/
├── README.md
└── requirements.txt
```

---

# Environment

- Python 3.11
- PyTorch CUDA 12.6
- NVIDIA GeForce RTX 3050 Laptop GPU
- VS Code

---

# Cara Menjalankan Project

## Clone repository

```bash
git clone https://github.com/Arachnoida/UTS-Data-Mining.git
```

## Install dependencies

```bash
pip install -r requirements.txt
```

## Jalankan notebook

Gunakan Jupyter Notebook atau VS Code untuk menjalankan notebook pada folder:

```bash
notebooks/
```

---

# Author

Ida Bagus Gede Dhananjaya |
Universitas Udayana
