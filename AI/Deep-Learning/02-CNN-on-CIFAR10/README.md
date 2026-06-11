# CIFAR-10 Image Classification using CNN

## Objective

Build a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify images from the CIFAR-10 dataset and compare its performance with a traditional Artificial Neural Network (ANN).

## Dataset

- CIFAR-10
- 50,000 training images
- 10,000 testing images
- Image size: 32 × 32 × 3 (RGB)
- 10 classes

## Model Architecture

```
Input (32×32×3)
      ↓
Conv2D (32, 3×3) + ReLU
      ↓
MaxPooling (2×2)
      ↓
Conv2D (32, 3×3) + ReLU
      ↓
MaxPooling (2×2)
      ↓
Flatten
      ↓
Dense (64, ReLU)
      ↓
Dense (10, Softmax)
```

## Results

| Model | Accuracy |
|-------|---------:|
| ANN | 49.63% |
| CNN | 68.21% |

## Concepts Learned

- CNN vs ANN
- Convolution Layer (Conv2D)
- Filters (Kernels)
- Feature Maps
- Max Pooling
- Flatten Layer
- ReLU Activation
- Softmax Activation
- Model Evaluation
- Classification Report
- Confusion Matrix

## Key Takeaways

- CNNs preserve spatial information, unlike ANNs.
- Convolution layers learn image features such as edges and textures.
- Pooling reduces computation while retaining important information.
- CNN achieved significantly better accuracy than ANN on CIFAR-10.

## Tech Stack

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn