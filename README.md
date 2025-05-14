# Pneumonia Detection Using Deep Neural Networks

This project focuses on using deep learning models to diagnose pneumonia from chest X-ray (CXR) images, with a dataset collected from the Guangzhou Women and Children Medical Center.

## 📌 Project Summary

We applied and compared four deep learning models to classify CXR images as either **Normal** or **Pneumonia**:

- **DenseNet201**
- **EfficientNetB0**
- **ResNet-18**
- **Custom CNN**

Data augmentation and preprocessing were critical to improving performance, especially in handling class imbalance.

## 📁 Dataset

- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets)
- **Total Images**: 5863 CXR images
- **Age Range**: Children aged 1–5
- **Structure**:
  - `train/` — Normal (0), Pneumonia (1)
  - `val/` — Normal (0), Pneumonia (1)
  - `test/` — Normal (0), Pneumonia (1)

## 🧪 Preprocessing

- Convert images to grayscale (optional)
- Resize to 196×196 or 224×224
- Normalize pixel values to [0,1]
- Apply data augmentation:
  - Rotation
  - Zoom
  - Shifting
  - Horizontal flipping (when appropriate)

## 🧠 Models

### DenseNet201
- Pretrained on ImageNet
- Fine-tuned with custom layers
- Achieved **88%** accuracy after augmentation

### EfficientNetB0
- Achieved best performance: **95.94%** accuracy
- High recall for pneumonia class: **0.99**

### ResNet-18
- Accuracy dropped to **50%**
- Struggled with noisy pneumonia images

### Custom CNN
- Accuracy: **91%**
- F1-Score for pneumonia: **93%**

## 📊 Results Summary

| Model         | Accuracy | Precision | Recall | F1-Score |
|---------------|----------|-----------|--------|----------|
| DenseNet201   | 88%      | High      | Balanced | High     |
| EfficientNetB0| 95.94%   | 0.92+     | 0.99 (PNEU) | Excellent |
| ResNet-18     | 50%      | Low       | Low    | Low      |
| Custom CNN    | 91%      | 92%       | 93%    | 93%      |

## 🔬 Conclusion

Deep learning models—especially EfficientNetB0—can be highly effective for automated pneumonia diagnosis using chest X-rays. Future improvements include better noise handling, expanding datasets, and integrating explainability tools such as Grad-CAM.


