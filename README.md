# CIFAR-100 CNN vs ResNet50

An image classification project using the **CIFAR-100 dataset**, comparing a custom **CNN built from scratch** with **ResNet50 using Transfer Learning**.

The project demonstrates how pretrained deep learning models can improve image classification performance compared with training a CNN architecture from scratch.

## 📌 Project Overview

The goal of this project is to build and evaluate two different image classification approaches:

1. **Custom CNN** — a convolutional neural network designed and trained from scratch.
2. **ResNet50** — a pretrained deep learning model used through transfer learning.

Both approaches are evaluated using training, validation, and test performance.

## 📊 Dataset

The project uses the **CIFAR-100 dataset**, which contains:

* **50,000 training images**
* **10,000 test images**
* **100 classes**
* RGB images with dimensions **32 × 32 × 3**

The dataset is loaded directly using TensorFlow/Keras.

## 🧠 Models

### 1. CNN From Scratch

A custom convolutional neural network is developed using Keras layers such as:

* Conv2D
* BatchNormalization
* MaxPooling
* Dropout
* Flatten
* Dense
* ReLU
* Softmax

The model is trained from randomly initialized weights.

### 2. ResNet50 Transfer Learning

The second approach uses **ResNet50**, a deep residual neural network pretrained on a large image dataset.

Transfer learning allows the model to reuse features learned from the pretrained network and adapt them to the CIFAR-100 classification task.

## ⚙️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* ResNet50
* Transfer Learning
* Convolutional Neural Networks (CNN)

## 🔄 Workflow

```text
CIFAR-100 Dataset
       ↓
Data Loading
       ↓
Data Preprocessing
       ↓
 ┌───────────────┬──────────────────┐
 │               │                  │
 ▼               ▼                  │
CNN From      ResNet50              │
Scratch       Transfer Learning     │
 │               │                  │
 └───────────────┴──────────────────┘
                 ↓
          Model Evaluation
                 ↓
       Performance Comparison
```

## 📈 Model Comparison

| Metric              | CNN From Scratch |   ResNet50 |
| ------------------- | ---------------: | ---------: |
| Train Accuracy      |           50.74% |     56.34% |
| Validation Accuracy |           42.22% |     57.76% |
| Test Accuracy       |           42.96% |     57.07% |
| Test Loss           |           2.2278 |     1.6633 |
| Training Time       |          638 sec |   1000 sec |
| Parameters          |        1,112,935 | 23,862,548 |

## 🏆 Results

**ResNet50 performed better overall** than the CNN built from scratch.

ResNet50 achieved higher training, validation, and test accuracy, while also obtaining a lower test loss.

The main advantage comes from using a pretrained model that has already learned useful visual features. Instead of learning all image representations from the beginning, transfer learning allows ResNet50 to start from previously learned features and adapt them to the target classification task.

Although ResNet50 required more training time and had significantly more parameters, it achieved substantially better classification performance.

## 💡 Key Takeaways

* CNNs can be built from scratch for image classification.
* Deeper architectures can learn more complex visual representations.
* Transfer learning can significantly improve performance.
* Pretrained models reduce the need to learn useful low-level features from scratch.
* ResNet50 achieved better generalization on the CIFAR-100 test set in this experiment.
* The trade-off is increased model size, number of parameters, and training time.

## 📁 Project Structure

```text
cifar100-cnn-vs-resnet50/
│
├── CIFAR100_CNN_vs_ResNet50.ipynb
├── README.md
└── requirements.txt
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/bassam519/cifar100-cnn-vs-resnet50.git
```

### 2. Install dependencies

```bash
pip install tensorflow numpy pandas matplotlib seaborn
```

### 3. Open the notebook

```bash
jupyter notebook CIFAR100_CNN_vs_ResNet50.ipynb
```

Run the notebook cells sequentially to reproduce the experiments.

## 👨‍💻 Author

**Bassam**

Aspiring ML Engineer | Data Science | Machine Learning | Data Analysis

GitHub: [bassam519](https://github.com/bassam519)

---

⭐ If you find this project useful, consider giving the repository a star!
