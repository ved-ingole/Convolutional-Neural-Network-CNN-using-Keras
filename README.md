# 🧠 CNN using TensorFlow/Keras - Handwritten Digit Classification

## PERSONAL DEEP LEARNING PROJECT

|               |                                                      |
| ------------- | ---------------------------------------------------- |
| **Author**    | Ved Ingole                                           |
| **Domain**    | Deep Learning / Computer Vision                      |
| **Framework** | TensorFlow & Keras                                   |
| **Project**   | Handwritten Digit Classification using CNN           |

---

# 📂 Dataset

* **Dataset Name:** MNIST Handwritten Digits Dataset
* **Source:** TensorFlow / Keras Datasets
* **Loaded Using:** `keras.datasets.mnist.load_data()`
* **Training Images:** 60,000
* **Testing Images:** 10,000
* **Image Size:** 28 × 28 Pixels (Grayscale)
* **Classes:** 10 (Digits 0–9)
* **Task Type:** Multi-Class Image Classification

---

# 🎯 Project Objectives

1. Load the MNIST handwritten digit dataset
2. Preprocess image data for CNN input
3. Build a Convolutional Neural Network (CNN)
4. Train the CNN model using TensorFlow/Keras
5. Evaluate model performance on unseen test data
6. Visualize training and validation performance
7. Save the trained model for future predictions

---

# 🔁 Project Pipeline

## Step 1: Import Required Libraries

Imported all required libraries for deep learning and visualization.

Libraries Used:

* TensorFlow
* Keras
* Matplotlib

Purpose:

* Build CNN architecture
* Train and evaluate the model
* Plot training performance

---

## Step 2: Load Dataset

Loaded the MNIST handwritten digit dataset using TensorFlow/Keras.

Dataset contains:

* 60,000 Training Images
* 10,000 Testing Images
* Labels from digits **0–9**

---

## Step 3: Data Preprocessing

Prepared the dataset before training.

### Normalization

Converted pixel values from:

* 0–255 → 0–1

This improves convergence during model training.

### Reshaping Images

Converted images into CNN input format:

* (28, 28, 1)

Where:

* Height = 28
* Width = 28
* Channels = 1 (Grayscale)

### One-Hot Encoding

Converted digit labels into categorical vectors using:

* `keras.utils.to_categorical()`

Purpose:

* Required for multi-class classification using Softmax output.

---

## Step 4: Build CNN Model

Designed a Sequential Convolutional Neural Network.

### Input Layer

Input Shape:

* 28 × 28 × 1

### First Convolution Block

* Conv2D
* 32 Filters
* Kernel Size = 3 × 3
* ReLU Activation
* MaxPooling2D (2 × 2)

Purpose:

* Extract basic image features such as edges and curves.

### Second Convolution Block

* Conv2D
* 64 Filters
* Kernel Size = 3 × 3
* ReLU Activation
* MaxPooling2D (2 × 2)

Purpose:

* Learn complex patterns and shapes from images.

### Flatten Layer

Converts feature maps into a one-dimensional vector.

### Dropout Layer

* Dropout Rate = 0.5

Purpose:

* Reduce overfitting
* Improve model generalization

### Dense Layer

* 128 Neurons
* ReLU Activation

### Output Layer

* 10 Neurons
* Softmax Activation

Outputs probability scores for digits **0–9**.

---

## Step 5: Compile Model

Compiled the CNN model using:

### Optimizer

* Adam

### Loss Function

* Categorical Crossentropy

### Evaluation Metric

* Accuracy

---

## Step 6: Train Model

Model trained using:

* Epochs = 10
* Batch Size = 128
* Validation Split = 10%

Training history stored for visualization.

---

## Step 7: Model Evaluation

Evaluated the trained model using the testing dataset.

Performance metrics:

* Test Accuracy
* Test Loss

Evaluation performed on unseen handwritten digit images.

---

## Step 8: Visualization

Generated training graphs.

### Accuracy Graph

Visualized:

* Training Accuracy
* Validation Accuracy

### Loss Graph

Visualized:

* Training Loss
* Validation Loss

Output File:

```text
training_history.png
```

Purpose:

* Analyze model learning
* Detect overfitting or underfitting
* Compare training and validation performance

---

## Step 9: Save Trained Model

Saved the trained CNN model for future predictions.

Output File:

```text
mnist_cnn_model.keras
```

The saved model can later be loaded without retraining.

---

# 📊 Key Findings

| Analysis | Observation |
|----------|-------------|
| Dataset | MNIST Handwritten Digits |
| Model Used | Convolutional Neural Network (CNN) |
| Framework | TensorFlow / Keras |
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Activation Functions | ReLU & Softmax |
| Output Classes | 10 Digits (0–9) |
| Model Performance | High Accuracy on Test Dataset |

---

# 🛠️ Tools & Libraries

| Tool | Purpose |
|------|---------|
| Python | Programming Language |
| TensorFlow | Deep Learning Framework |
| Keras | Neural Network API |
| NumPy | Numerical Operations |
| Matplotlib | Visualization |

---

# 📁 Files

| File | Description |
|------|-------------|
| `cnn_mnist.py` | Main Python Script |
| `mnist_cnn_model.keras` | Saved CNN Model |
| `training_history.png` | Training Accuracy & Loss Graph |
| `README.md` | Project Documentation |

---

# 📈 Visualizations Included

* Training Accuracy Graph
* Validation Accuracy Graph
* Training Loss Graph
* Validation Loss Graph

---

# 📚 Dataset Citation

LeCun, Y., Cortes, C., & Burges, C. J. C. **MNIST Handwritten Digit Database**, available through TensorFlow/Keras Datasets.

---

# 👨‍💻 Author

**Ved Ingole**

---

# ✅ Conclusion

This project demonstrates the implementation of a **Convolutional Neural Network (CNN)** using **TensorFlow and Keras** for handwritten digit recognition on the **MNIST dataset**. The workflow includes data preprocessing, CNN model design, compilation, training, evaluation, visualization of training performance, and model saving. The project provides practical experience in applying deep learning techniques to computer vision tasks and serves as a strong foundation for building more advanced image classification models.
