# 👁️ Glaucoma Classification Using CNN and Feature Extraction
This project implements a Convolutional Neural Network (CNN) model to classify fundus images into **Glaucomatous (RG)** and **Normal (NRG)** classes. The model uses **feature extraction techniques** to enhance classification performance.

# 📁 Dataset Structure
The dataset used in this project contains two categories:
glaucoma_data/
├── train/
│ ├── NRG/ # Normal retinal images
│ └── RG/ # Glaucoma retinal images


---

## 🧠 Model Overview

- **Framework**: TensorFlow/Keras
- **Model Type**: CNN with Global Average Pooling
- **Preprocessing**:
  - Image resizing (e.g., 150x150)
  - Normalization
  - Label encoding (NRG = 0, RG = 1)
- **Split**: Train/Test (e.g., 80/20)
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy

---

## 🧪 Results

| Metric           | Value    |
|------------------|----------|
| Test Accuracy    | ~65%     |
| Loss             | ~0.63    |

> 🔍 *Note: With additional tuning or data augmentation, accuracy can be further improved.*

---

## 📝 How to Run

1. Upload your dataset zip in Google Colab.
2. Extract and preprocess the images.
3. Train the model:
   ```python
   history = model.fit(X_train, y_train, epochs=50, validation_data=(X_test, y_test))
