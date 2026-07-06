# Brain Tumor MRI Classification using MobileNetV3Large

A proof-of-concept deep learning project exploring the use of transfer learning for multiclass brain MRI image classification. This repository demonstrates a possible workflow using TensorFlow and MobileNetV3Large and is intended for educational and research purposes only.

> **Note**
> This project is an experimental concept and is **not** a production-ready medical application. It has not been clinically validated and should not be used for diagnosis or patient care.

---

## Overview

This project investigates whether transfer learning can be used to distinguish between four categories of brain MRI images:

- Glioma
- Meningioma
- Pituitary Tumor
- No Tumor

The primary objective is to explore model development, training, and evaluation using modern computer vision techniques.

---

## Features

- MobileNetV3Large transfer learning
- TensorFlow/Keras implementation
- Image preprocessing and augmentation
- Model training and evaluation pipeline
- Confusion matrix visualization
- Google Colab compatible

---

## Dataset

```
brain-tumor-mri-dataset/
│
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── notumor/
│   └── pituitary/
│
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── notumor/
    └── pituitary/
```

Classes:

- Glioma
- Meningioma
- No Tumor
- Pituitary

---

## Model Architecture

- **Base Model:** MobileNetV3Large (ImageNet pretrained)
- Input Size: **224 × 224 × 3**
- Global Average Pooling
- Dense Classification Layer
- Softmax Output (4 Classes)

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- OpenCV
- Scikit-learn
- Google Colab

---

## Workflow

1. Load MRI dataset
2. Preprocess and augment images
3. Build MobileNetV3Large transfer learning model
4. Train and validate the model
5. Evaluate model performance
6. Visualize results using standard classification metrics

---

## Repository Structure

```
├── BRAIN_TUMOUR_PRED_MOBNETV3.ipynb
├── dataset/
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Future Work

- Experiment with additional CNN architectures
- Integrate explainability methods such as Grad-CAM
- Compare multiple transfer learning models
- Optimize training through fine-tuning and hyperparameter tuning
- Investigate deployment as a research demonstration

---

## Disclaimer

This repository is a **research and learning project** intended to demonstrate deep learning techniques for image classification.

It is **not** a medical device, **not** a diagnostic tool, and **not** suitable for clinical use. Any results produced by this model should not be interpreted as medical advice or used to make healthcare decisions.

---

## License

This project is licensed under the MIT License.
