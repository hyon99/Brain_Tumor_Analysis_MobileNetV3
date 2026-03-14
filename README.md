# Brain Tumor MRI Classification using MobileNetV3Large

## Overview

This project implements a **deep learning–based brain tumor classification system** using MRI images. The model uses **transfer learning with MobileNetV3Large** to classify MRI scans into **four tumor categories**.

The system is trained on a publicly available MRI dataset and uses **TensorFlow/Keras**, **mixed precision training**, and **data augmentation** to improve training efficiency and model performance.

The goal of the project is to build an **efficient and accurate CNN-based classifier** for detecting brain tumor types from MRI images.

## Dataset

Dataset used: **Brain Tumor MRI Dataset**

Classes included:

* Glioma
* Meningioma
* Pituitary
* No Tumor

Dataset source:
https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

Dataset structure:

```
brain-tumor-mri-dataset/
│
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── pituitary/
│   └── notumor/
│
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── pituitary/
    └── notumor/
```

---

## Model Architecture

The model uses **MobileNetV3Large as a feature extractor** with a custom classification head.

Architecture pipeline:

```
Input Image (224×224×3)
        ↓
Data Augmentation
        ↓
MobileNetV3 Preprocessing
        ↓
MobileNetV3Large (Pretrained on ImageNet, Frozen)
        ↓
Global Average Pooling
        ↓
Batch Normalization
        ↓
Dense Layer (256 units, ReLU)
        ↓
Dropout (0.1)
        ↓
Dense Output Layer (4 classes, Softmax)
```

---

## Key Features

* Transfer Learning using **MobileNetV3Large**
* **Mixed Precision Training (FP16)** for faster computation
* **Data Augmentation** for improved generalization
* Automatic **convolution layer analysis table**
* Efficient training pipeline using **tf.data**

---

## Data Augmentation

The following augmentation techniques are applied during training:

* Random Horizontal Flip
* Random Rotation (0.05)
* Random Zoom (0.1)
* Random Contrast (0.1)

These help prevent overfitting and improve model robustness.

---

## Training Configuration

| Parameter     | Value                                            |
| ------------- | ------------------------------------------------ |
| Image Size    | 224 × 224                                        |
| Batch Size    | 32                                               |
| Epochs        | 40                                               |
| Optimizer     | Adam                                             |
| Learning Rate | 1e-4                                             |
| Loss Function | Categorical Crossentropy (label smoothing = 0.1) |
| Classes       | 4                                                |

---

## Installation

Install required dependencies:

```
pip install tensorflow opendatasets matplotlib pandas
```

---

## Model Evaluation

After training, the model accuracy on Validation Data is ~93%.

## Technologies Used

* Python
* TensorFlow / Keras
* MobileNetV3Large
* OpenDatasets
* Matplotlib
* Pandas

---

## Possible Improvements

Future enhancements may include:

* Fine-tuning deeper layers of MobileNetV3
* Using attention mechanisms
* Hyperparameter tuning
* Model deployment with Flask or FastAPI
* Grad-CAM visualization for model interpretability

---

## Author

Sudipon Makal

---

## License

This project is open-source and available under the **MIT License**.
