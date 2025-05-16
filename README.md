#  Brain Tumor Detection with CNN

This is a personal project where I trained a Convolutional Neural Network (CNN) to detect brain tumors from MRI scans. It’s a binary classification model that predicts whether a tumor is present or not in the given image.

##  Dataset
The dataset comes from [Kaggle](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection) and contains MRI images divided into two folders:
- `yes/` – images with brain tumors
- `no/` – images without tumors

I've placed these inside a `data/` folder for training.

##  Model Details
I used TensorFlow and Keras to build the CNN. The architecture includes:
- Conv2D layers with ReLU activation
- Batch Normalization
- MaxPooling
- Flatten + Dense layer for binary classification

The input size for images is standardized to `(240, 240, 3)` and pixel values are normalized between 0 and 1.

##  Performance
After training the model for multiple epochs, I reached the following results:
- **Validation Accuracy:** 91%
- **Test Accuracy:** 89%
- **F1 Score (Test):** 0.88

##  Visualizations
I’ve also included:
- Plots for training/validation accuracy and loss
- Sample MRI images with tumor and no-tumor labels
- F1 score and confusion matrix

##  Getting Started
If you want to run this locally:
1. Clone the repo:
   ```bash
   git clone https://github.com/Indhusrikrishnaraj/brain-tumor-detection-cnn.git
   cd brain-tumor-detection-cnn


