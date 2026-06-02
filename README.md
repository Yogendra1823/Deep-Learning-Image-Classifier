# Deep Learning Image Classification using Transfer Learning

## Overview

This project implements a high-performance image classification system using Transfer Learning and Deep Learning techniques. The model leverages MobileNetV2, a pretrained convolutional neural network trained on the ImageNet dataset, to accurately classify images of cats and dogs.

Developed as part of the **Interspark AI/ML Internship Program**, this project demonstrates practical applications of computer vision, transfer learning, data augmentation, model evaluation, and deployment-ready model generation.

---

## Project Objectives

* Build an image classification model using deep learning.
* Apply transfer learning using a pretrained CNN architecture.
* Improve model generalization through data augmentation.
* Evaluate model performance using standard metrics.
* Save and reuse the trained model for inference.
* Gain practical experience in modern computer vision workflows.

---

## Key Features

* Transfer Learning with MobileNetV2
* TensorFlow & Keras Deep Learning Framework
* Data Augmentation Pipeline
* Automated Dataset Loading using TensorFlow Datasets
* Training and Validation Performance Visualization
* Model Persistence using HDF5 Format
* Inference-Ready Saved Model
* GPU-Accelerated Training via Google Colab

---

## Dataset Information

**Dataset:** Cats vs Dogs

**Source:** TensorFlow Datasets (TFDS)

### Dataset Statistics

| Property     | Value                 |
| ------------ | --------------------- |
| Total Images | 23,262                |
| Classes      | 2                     |
| Labels       | Cat, Dog              |
| Dataset Type | Binary Classification |

The dataset consists of real-world images with varying backgrounds, lighting conditions, image sizes, and viewpoints, making it suitable for evaluating image classification models.

---

## Data Preprocessing

The following preprocessing steps were applied:

* Image resizing to 224×224 pixels
* Pixel normalization
* Dataset batching
* Dataset shuffling
* Train-validation splitting

### Data Augmentation

To improve model generalization and reduce overfitting:

* Random Horizontal Flip
* Random Rotation
* Random Zoom

---

## Model Architecture

### Base Model

MobileNetV2 (Pretrained on ImageNet)

### Classification Head

* GlobalAveragePooling2D
* Dropout Layer (Regularization)
* Dense Output Layer with Sigmoid Activation

### Transfer Learning Strategy

The pretrained MobileNetV2 feature extractor was frozen during training while a custom classification head was trained on the Cats vs Dogs dataset.

---

## Training Configuration

| Parameter     | Value               |
| ------------- | ------------------- |
| Optimizer     | Adam                |
| Loss Function | Binary Crossentropy |
| Batch Size    | 32                  |
| Epochs        | 5                   |
| Input Size    | 224 × 224           |
| Framework     | TensorFlow/Keras    |

---

## Results

### Model Performance

| Metric              | Score  |
| ------------------- | ------ |
| Training Accuracy   | 94.76% |
| Validation Accuracy | 98.28% |
| Validation Loss     | 0.0460 |

The model achieved excellent classification performance with strong generalization capabilities and minimal overfitting.

---

## Visualizations

The project includes:

* Dataset Preview
* Model Summary
* Training Accuracy Curve
* Training Loss Curve
* Evaluation Metrics
* Sample Predictions

All generated visualizations are available inside the `screenshots/` directory.

---

## Project Structure

```text
Deep-Learning-Image-Classifier/
│
├── screenshots/
│   ├── dataset_preview.png
│   ├── model_summary.png
│   ├── training_accuracy.png
│   ├── training_loss.png
│   └── evaluation_metrics.png
│
├── cats_dogs_classifier.h5
├── task2_deep_learning_image_classifier.ipynb
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone <repository-url>
cd Deep-Learning-Image-Classifier
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
task2_deep_learning_image_classifier.ipynb
```

Run all notebook cells sequentially.

---

## Model Inference

Load the saved model:

```python
from tensorflow.keras.models import load_model

model = load_model("cats_dogs_classifier.h5")
```

Use the model to predict new cat and dog images.

---

## Learning Outcomes

This project demonstrates practical understanding of:

* Deep Learning Fundamentals
* Convolutional Neural Networks (CNNs)
* Transfer Learning
* Computer Vision
* Data Augmentation
* Model Evaluation
* TensorFlow & Keras
* Model Deployment Preparation

---

## Future Improvements

* Fine-tuning MobileNetV2 layers
* Multi-class image classification
* Streamlit deployment
* TensorFlow Lite conversion
* Real-time webcam predictions
* Docker containerization
* Cloud deployment

---

## Internship Information

**Program:** Interspark AI/ML Internship Program

**Domain:** Artificial Intelligence & Machine Learning

---

## Author

**Yogendra**

B.Tech – Artificial Intelligence & Machine Learning

Narasimha Reddy Engineering College

---

## License

This project is developed for educational, research, and internship submission purposes.
