# Implementation of a Multi-Layer Perceptron

A TensorFlow/Keras implementation of a Multi-Layer Perceptron (MLP) for multi-class image classification on the Fashion-MNIST dataset. Also includes an MLP solution to the XOR gate problem, which a single layer perceptron cannot solve.

## Features

- Fashion-MNIST data preprocessing
- MLP model implementation
- Hyperparameter tuning
- Model evaluation (Accuracy, Precision, Recall, F1-score)
- Training and evaluation visualizations
- XOR gate solved using an MLP with a hidden layer, demonstrating non-linear decision boundaries that a single layer perceptron cannot produce

## Tech Stack

- Python
- TensorFlow / Keras
- Scikit-learn
- SciKeras
- NumPy
- Matplotlib

## Results

### Best Hyperparameters

| Hyperparameter | Value |
|---|---|
| Hidden Layers | 3 |
| Hidden Neurons | 128 |
| Learning Rate | 0.001 |
| Batch Size | 32 |
| Optimizer | RMSProp |
| Activation Function | Tanh |
| Epochs | 30 |
| Dropout | 0.2 |
| Cross-validation Accuracy | 0.8643 (86.43%) |
| Testing Accuracy | 0.8803 (88.03%) |

### Performance Comparison

| Metric | Baseline | Optimized |
|---|---|---|
| Accuracy | 0.8849 | 0.8803 |
| Precision | 0.8871 | 0.8813 |
| Recall | 0.8849 | 0.8803 |
| F1-score | 0.8855 | 0.8805 |
| Training Time | 110.57 s | 169.59 s |

### Baseline Per-Class Report (test set)

| Class | Precision | Recall | F1-score | Support |
|---|---|---|---|---|
| T-shirt/top | 0.87 | 0.79 | 0.83 | 1000 |
| Trouser | 0.99 | 0.96 | 0.98 | 1000 |
| Pullover | 0.81 | 0.80 | 0.80 | 1000 |
| Dress | 0.85 | 0.92 | 0.88 | 1000 |
| Coat | 0.81 | 0.81 | 0.81 | 1000 |
| Sandal | 0.97 | 0.96 | 0.97 | 1000 |
| Shirt | 0.70 | 0.75 | 0.72 | 1000 |
| Sneaker | 0.94 | 0.95 | 0.95 | 1000 |
| Bag | 0.98 | 0.96 | 0.97 | 1000 |
| Ankle boot | 0.95 | 0.95 | 0.95 | 1000 |
| **Macro avg** | 0.89 | 0.88 | 0.89 | 10000 |
| **Weighted avg** | 0.89 | 0.88 | 0.89 | 10000 |

loit.
