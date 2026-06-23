# MNIST Object Detection using VGG16 Transfer Learning

## Overview

This project implements a multi-task deep learning model for object localization and digit classification using TensorFlow and Keras. The model is built on top of a pretrained VGG16 backbone and is trained on a custom object detection dataset generated from the MNIST handwritten digit dataset.

Instead of performing only digit classification, each MNIST digit is randomly placed on a larger 64×64 canvas. The model learns two tasks simultaneously:

* Digit Classification (0–9)
* Bounding Box Regression (Object Localization)

This project demonstrates the fundamentals of transfer learning, multi-task learning, and object detection.

---

## Features

* Custom object detection dataset generation
* Transfer Learning using VGG16 pretrained on ImageNet
* Multi-output neural network architecture
* Digit classification head
* Bounding box regression head
* Early Stopping and Learning Rate Scheduling
* TensorFlow/Keras implementation

---

## Dataset

The project uses the MNIST handwritten digit dataset.

### Preprocessing

* MNIST digits are placed at random locations on a 64×64 blank canvas.
* Bounding box coordinates are generated automatically.
* Images are converted to RGB format to match VGG16 input requirements.
* Bounding boxes are normalized before training.

---

## Model Architecture

### Backbone

* VGG16 (Pretrained on ImageNet)
* Top classification layers removed
* Last few layers fine-tuned

### Outputs

#### Classification Head

Predicts:

* Digits from 0–9

#### Localization Head

Predicts:

* xmin
* ymin
* xmax
* ymax

---

## Training Configuration

* Optimizer: Adam
* Classification Loss: Sparse Categorical Crossentropy
* Bounding Box Loss: Mean Squared Error (MSE)
* Metrics:

  * Classification Accuracy
  * Bounding Box MAE
* EarlyStopping
* ReduceLROnPlateau

---

## Results

The model is capable of:

* Detecting the location of handwritten digits
* Predicting accurate bounding boxes
* Classifying detected digits simultaneously

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* OpenCV
* Matplotlib


## Future Improvements

* Support multiple objects per image
* Implement IoU-based evaluation
* Add data augmentation
* Train on larger datasets
* Implement YOLO and DETR architectures
* Improve localization accuracy

---

## Learning Outcomes

Through this project, the following concepts are explored:

* Transfer Learning
* Object Localization
* Multi-Task Learning
* Bounding Box Regression
* Computer Vision Pipelines
* TensorFlow Model Development

---

## Author

Shubham Verma

B.Tech Computer Science and Engineering

University College of Engineering and Technology, Bikaner
