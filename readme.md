# Waste Classification (Tin vs Glass)

This project is a deep learning-based image classification system that automatically identifies waste items as **Tin** or **Glass** using a Convolutional Neural Network (CNN) built with TensorFlow/Keras. The goal is to support smarter waste segregation by using computer vision to distinguish between recyclable materials.

The model is trained on a Kaggle dataset containing images along with YOLO annotation files, which are processed and converted into a structured format for training and evaluation.

---

## Dataset

The dataset includes images with YOLO annotations, which were processed for model training.

## Example Images

| Dataset                        | Result                       | Training Graph             |
| ------------------------------ | ---------------------------- | -------------------------- |
| ![Dataset](images/dataset.png) | ![Result](images/result.png) | ![Graph](images/graph.png) |

---

## Workflow

- Dataset downloaded and prepared from Kaggle
- YOLO annotation files parsed into structured format
- Data visualized with bounding boxes
- CNN model built using TensorFlow/Keras
- Model trained and evaluated
- Performance checked using accuracy, loss, and confusion matrix
- Prediction function created for custom images

---

## Training Loss

Training loss is shown in the **graph.png** image (loss curve over epochs).

---

## Tech Stack

- Python
- TensorFlow / Keras
- Pandas
- OpenCV
- Matplotlib

---
