# Single Layer Perceptron – MNIST Binary Classification

## Overview

This project implements a **single-layer perceptron from scratch** and applies it to binary classification tasks using the MNIST handwritten digits dataset.

---

## Dataset

- MNIST handwritten digits
- Image size: 28 × 28
- Images flattened into 784-dimensional vectors
- Labels converted to {+1, -1}

---

## Model

### Prediction Rule

y_hat = sign(w^T x + b)

Where:
- w = weight vector
- b = bias
- x = input vector

---

### Update Rule (Perceptron Learning Rule)

If a sample is misclassified:

w ← w + η y_i x_i  
b ← b + η y_i  

Where:
- η = learning rate
- y_i ∈ {+1, -1}

Training stops when:
- Maximum iterations reached, or
- Classification error falls below threshold

---

## Evaluation

Classification Error = (Number of wrong predictions) / (Total samples)

Accuracy = 1 − Classification Error

---

## Visualisation of Learned Feature

The learned weight vector w is reshaped to 28 × 28 and displayed as an image.

Interpretation:
- Positive weights highlight pixels characteristic of class +1
- Negative weights highlight pixels characteristic of class −1
- The image resembles a contrast between the two digit patterns

---

## Requirements

- Python 3.9+
- NumPy
- Matplotlib