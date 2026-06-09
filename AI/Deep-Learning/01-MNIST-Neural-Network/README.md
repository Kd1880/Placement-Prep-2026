# MNIST Handwritten Digit Classification

## Objective

Build my first Artificial Neural Network (ANN) using TensorFlow/Keras to classify handwritten digits (0–9) from the MNIST dataset.

---

## Dataset

* **Training Images:** 60,000
* **Testing Images:** 10,000
* **Image Size:** 28 × 28 pixels (grayscale)

Each image contains pixel values ranging from **0 to 255**, where:

* **0** = Black
* **255** = White

---

## Data Preparation

### Normalization

```python
X_train = X_train / 255
X_test = X_test / 255
```

**Why?**

* Converts pixel values from **0–255** to **0–1**
* Makes training faster
* Improves model convergence
* Prevents large input values from affecting learning

---

## Model Architecture

```
Input (28×28 Image)
        │
        ▼
Flatten Layer
(28×28 → 784)
        │
        ▼
Dense Layer
100 Neurons
Activation: ReLU
        │
        ▼
Output Layer
10 Neurons
Activation: Softmax
```

---

## Concepts Learned

### 1. Why do we have X and Y?

* **X** → Input data (images)
* **Y** → Correct labels (digits)

Example:

```
X_train[0] → Image of digit 5

Y_train[0] → 5
```

The model learns the relationship between the image and its correct label.

---

### 2. Training vs Testing Data

Training data is used to learn patterns.

Testing data is kept separate and is only used to evaluate how well the model performs on unseen images.

---

### 3. Flatten Layer

Original image:

```
28 × 28
```

After Flatten:

```
784
```

The neural network accepts a 1D vector, so Flatten converts the 2D image into a single list of 784 pixel values.

---

### 4. Dense Layer

A Dense layer means every neuron is connected to every neuron in the previous layer.

Example:

```
784 Inputs
      │
      ▼
100 Hidden Neurons
```

Each neuron learns different features from the image.

---

### 5. ReLU Activation

```
f(x) = max(0, x)
```

If the value is negative:

```
0
```

If positive:

```
same value
```

ReLU introduces non-linearity and helps deep networks learn complex patterns efficiently.

---

### 6. Softmax Activation

The output layer has **10 neurons**, one for each digit (0–9).

Softmax converts the outputs into probabilities.

Example:

```
0 : 0.01
1 : 0.02
2 : 0.90
3 : 0.01
...
```

The highest probability is chosen as the prediction.

---

### 7. Loss Function

```
Sparse Categorical Crossentropy
```

Measures how wrong the predictions are.

Lower loss indicates better predictions.

---

### 8. Optimizer

```
Adam
```

The optimizer updates the model's weights after every batch to minimize the loss.

---

### 9. Epoch

One complete pass through the entire training dataset.

Example:

```
epochs = 5
```

means the model sees all 60,000 images five times.

---

### 10. Accuracy

Accuracy represents the percentage of correct predictions.

Final training accuracy:

**98.44%**

---

## Problems I Faced

* TensorFlow installation
* Multiple Python versions
* Jupyter kernel mismatch
* TensorBoard installation
* Git Bash path issues
* Conda environment configuration

**Resolution:** Successfully configured a dedicated TensorFlow environment using Anaconda.

---

## Key Takeaways

* Always normalize image data.
* Use **ReLU** for hidden layers.
* Use **Softmax** for multi-class classification.
* Keep training and testing data separate.
* Flatten converts images into vectors.
* Adam is a powerful optimizer for beginners.
* TensorFlow + Keras makes building neural networks straightforward.

---

## Next Topics

* Hidden Layers
* Overfitting
* Dropout
* TensorBoard
* Convolutional Neural Networks (CNNs)
