# Single Layer Perceptron – MNIST Binary Classification

## Overview

This project implements a **single-layer perceptron from scratch** and applies it to binary classification tasks using the MNIST handwritten digits dataset.

The goal is to:
- Train a perceptron to distinguish between two selected digit classes
- Evaluate classification performance
- Visualise the learned weight vector
- Compare performance across different digit pairs

---

## Dataset

- **MNIST handwritten digits**
- Original image size: **28 × 28**
- Images are flattened into **784-dimensional vectors**
- Only two selected digit classes are used per experiment
- Labels are mapped to **{+1, -1}**

---

## Model

### Prediction Rule

\[
\hat{y} = \text{sign}(w^T x + b)
\]

Where:
- `w` = weight vector
- `b` = bias term
- `x` = input vector

---

### Update Rule (Perceptron Learning Rule)

If a sample is misclassified:

\[
w \leftarrow w + \eta y_i x_i
\]
\[
b \leftarrow b + \eta y_i
\]

Where:
- `η` = learning rate
- `y_i ∈ {+1, -1}`

Training stops when:
- Maximum number of iterations is reached, or
- Classification error falls below a threshold

---

## Training Procedure

1. Extract two digit classes from MNIST
2. Convert labels to `{+1, -1}`
3. Train perceptron using iterative updates
4. Record training error per iteration
5. Evaluate on test set

---

## Evaluation

- **Training Error**: Fraction of misclassified training samples per iteration
- **Test Error**: Fraction of misclassified test samples using learned parameters

Accuracy is computed as:

\[
\text{Accuracy} = 1 - \text{Classification Error}
\]

---

## Visualisation of Learned Feature

The learned weight vector `w` is reshaped to **28 × 28** and displayed as an image.

Interpretation:
- Positive weights highlight pixels characteristic of class `+1`
- Negative weights highlight pixels characteristic of class `-1`
- The image resembles a contrast between the two digit patterns

---

## Observations

- Some digit pairs are more linearly separable than others
- The perceptron converges when classes are approximately linearly separable
- Harder digit pairs result in higher classification error

---

## Requirements

- Python 3.9+
- NumPy
- Matplotlib

---

## How to Run

1. Load MNIST dataset
2. Select two digit classes
3. Run training (`optimize`)
4. Evaluate using `test`
5. Visualise learned weights

---

## Author

Single-layer perceptron implementation for binary digit classification.