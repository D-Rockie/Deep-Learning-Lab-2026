# Implementation of Convolutional Neural Networks (CNNs)

A TensorFlow/Keras implementation of a Convolutional Neural Network for multi-class image classification on the CIFAR-10 dataset, covering the convolution operation, output dimension calculation, feature map visualization, pooling comparison, and full CNN training/evaluation.

## Features

- CIFAR-10 data loading, sample visualization, and class distribution analysis
- Convolution implemented and compared across kernel sizes (3×3, 5×5, 7×7)
- Hyperparameter study: stride (1 vs 2) and padding (same vs valid), with output dimension calculations
- Feature map visualization after the first convolutional layer
- Max Pooling vs Average Pooling comparison
- Full CNN: Conv → ReLU → MaxPool → Conv → ReLU → MaxPool → Flatten → Dense → Softmax
- Model evaluation (Accuracy, Precision, Recall, F1-score, Confusion Matrix, Classification Report)
- Numerical exercises: output size calculation, parameter counting, ReLU vs Sigmoid comparison

## Tech Stack

- Python
- TensorFlow / Keras
- Scikit-learn
- NumPy
- Matplotlib

## Dataset

- CIFAR-10
- Training images: 50,000
- Testing images: 10,000
- Classes: 10 (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
- Image size: 32 × 32 × 3
- Class distribution is balanced (5,000 training images per class)

## Model Configuration

- Architecture: Conv → ReLU → MaxPool → Conv → ReLU → MaxPool → Flatten → Dense → Softmax
- Optimizer: Adam
- Epochs: 20
- Batch Size: 32
- Trainable Parameters: 136,874

## Results

| Metric | Value |
|---|---|
| Training Accuracy | 0.9523 |
| Testing Accuracy | 0.7003 |
| Precision | 0.6987 |
| Recall | 0.7003 |
| F1-score | 0.6980 |
| Parameters | 136,874 |

### Pooling Comparison (Max vs Average)

| Pooling | Test Accuracy | Training Accuracy | Notes |
|---|---|---|---|
| Max Pooling | 0.6522 | 0.9523 | Larger train–val gap, heavier overfitting |
| Average Pooling | 0.6810 | — | Generalized slightly better on this dataset |

### Filter Count Comparison (16 vs 64 filters)

| Filters | Parameters | Test Accuracy | Time/Epoch |
|---|---|---|---|
| 16 | 136,874 | 0.6522 | ~45–47 s |
| 64 | 301,578 | 0.6895 | ~130–140 s |

Increasing filters roughly tripled per-epoch training time for a ~3.7 point accuracy gain — the standard accuracy-vs-compute trade-off in CNN design.

## Numerical Exercises

1. **Output size, 64×64 input, 5×5 kernel, stride 2, padding 2:** `(64 − 5 + 2×2)/2 + 1 = 32.5` → floored to **32×32**
2. **Parameters, 64 filters of 3×3 on RGB input:** `(3×3×3 + 1) × 64 = 1,792`
3. **ReLU vs Sigmoid:** ReLU (`max(0, x)`) is cheap to compute and avoids vanishing gradients (constant gradient of 1 for positive inputs), but can suffer from "dying ReLU" (neurons permanently inactive). Sigmoid squashes outputs to (0, 1), saturates for large |x| causing vanishing gradients in deep networks, and is more expensive due to the exponential term. ReLU is preferred in hidden layers; sigmoid is typically reserved for binary classifier output layers.
