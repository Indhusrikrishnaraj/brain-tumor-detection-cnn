#  Brain Tumor Classification with EfficientNetB3

This project uses transfer learning with **EfficientNetB3** and TensorFlow to classify brain MRI images into four categories:

- Glioma
- Meningioma
- Pituitary tumor
- No tumor

It’s designed for high performance on limited medical data, using advanced training techniques, callbacks, and evaluation metrics.

---

##  Dataset

The dataset is from [Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset).

###  Folder Structure

Before training, organize your dataset like this:

```
brain_tumor/
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── pituitary/
│   └── notumor/
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── pituitary/
    └── notumor/
```

Each folder should contain the respective MRI images.

---

##  Model Overview

- Base model: **EfficientNetB3** (pretrained on ImageNet)
- Classification head: BatchNormalization → Dense → Dropout → Dense (Softmax)
- Optimizer: `Adamax`
- Loss: `categorical_crossentropy`
- Includes a **custom training callback** with learning rate scheduling and early stopping logic

---

##  How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/brain-tumor-detection-efficientnet.git
   cd brain-tumor-detection-efficientnet
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Make sure the dataset is placed inside the `brain_tumor/` directory as shown above.

4. Launch the notebook:
   ```bash
   jupyter notebook notebooks/brain_tumor_detection_efficientnet.ipynb
   ```

---

##  Results

| Metric        | Accuracy |
|---------------|----------|
| Train         | 100%     |
| Validation    | 98.7%    |
| Test          | 98.6%    |

- ✅ Confusion matrix
- ✅ Classification report
- ✅ Accuracy/loss visualizations
- ✅ F1-score per class

---

##  Tech Stack

- TensorFlow / Keras
- EfficientNetB3
- ImageDataGenerator
- Scikit-learn
- Matplotlib, Seaborn
- OpenCV, Pandas, NumPy

---

##  Why EfficientNetB3?

EfficientNetB3 is part of Google’s EfficientNet family of models. It provides a strong balance of speed and accuracy, making it a great fit for medical imaging with limited data.

- Pretrained on ImageNet
- Efficient for GPU or CPU inference
- Achieves high accuracy with fewer parameters

---

##  License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.





