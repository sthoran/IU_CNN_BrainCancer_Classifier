# Brain MRI Classification with CNN and Dilated CNN

This project implements and compares **Convolutional Neural Networks (CNN)** and **Dilated CNNs** for the classification of brain MRI scans into four categories: **Glioma**, **No Tumor**, **Meningioma**, and **Pituitary Tumor**. The aim is to assess the effectiveness of dilated convolutions in handling complex datasets, including those with added noise.

---

## Project Overview

Brain MRI classification is a critical task in medical imaging. While traditional CNNs have proven effective, **Dilated CNNs** offer an advantage by expanding the receptive field, allowing the model to capture spatial dependencies without increasing the computational load. This project evaluates the robustness of both models in standard and noisy environments.

---

## Dataset

The dataset contains 7023 MRI images categorized into four classes:
1. **Glioma**
2. **No Tumor**
3. **Meningioma**
4. **Pituitary Tumor**

Each image is labeled and preprocessed for training, validation, and testing.

---

## Model Architectures

### CNN
The CNN model uses standard convolutional layers to extract spatial features from the input images. It follows a traditional architecture of:
- **Convolutional Layers**
- **Max Pooling Layers**
- **Fully Connected Layers**

### Dilated CNN
The Dilated CNN replaces standard convolutional layers with **dilated convolutions**, which allow for a larger receptive field without increasing parameters. This architecture is particularly suited for noisy or complex datasets.

---

## Performance Evaluation

Performance was assessed using the following metrics:
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

Models were tested on both:
1. **Clean Data**: Original dataset without noise.
2. **Noisy Data**: Dataset with added noise to evaluate model robustness.

---

## Results

### On Clean Data:
| Model        | Class        | Precision | Recall | F1-Score |
|--------------|--------------|-----------|--------|----------|
| **CNN**      | Glioma       | 0.96      | 0.93   | 0.94     |
|              | No Tumor     | 0.89      | 0.93   | 0.91     |
|              | Meningioma   | 0.99      | 0.97   | 0.98     |
|              | Pituitary    | 0.98      | 0.98   | 0.98     |
| **Dilated CNN** | Glioma    | 0.96      | 0.93   | 0.94     |
|              | No Tumor     | 0.89      | 0.93   | 0.91     |
|              | Meningioma   | 0.99      | 0.97   | 0.98     |
|              | Pituitary    | 0.98      | 0.98   | 0.98     |

### On Noisy Data:
| Model        | Class        | Precision | Recall | F1-Score |
|--------------|--------------|-----------|--------|----------|
| **CNN**      | Glioma       | 0.90      | 0.82   | 0.86     |
|              | No Tumor     | 0.76      | 0.69   | 0.73     |
|              | Meningioma   | 0.93      | 0.99   | 0.96     |
|              | Pituitary    | 0.85      | 0.92   | 0.89     |
| **Dilated CNN** | Glioma    | 0.99      | 0.83   | 0.88     |
|              | No Tumor     | 0.77      | 0.66   | 0.71     |
|              | Meningioma   | 0.91      | 0.99   | 0.95     |
|              | Pituitary    | 0.85      | 0.94   | 0.89     |

---

## Requirements

To run this project, you will need:
- Python 3.8 or higher
- TensorFlow 2.x
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook (optional)

Install dependencies using:
```bash
pip install -r requirements.txt
