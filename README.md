# 🏠 House Price Multimodal Predictor

A machine learning project to predict house prices by combining structured tabular data with image data of houses, using CNN feature extraction and regression modeling.

---

## 🎯 **Objective of the Task**

The goal of this project is to build a **multimodal machine learning pipeline** that predicts housing prices by leveraging:
- Structured tabular data (e.g., bedrooms, bathrooms, city info, square footage)
- Visual information extracted from house images

This demonstrates the power of **multimodal learning**, where combining different data modalities can improve prediction performance compared to using a single data type.

---

## 🧰 **Methodology / Approach**

- 📦 **Data**:  
  - Tabular data from `House_prediction.csv`  
  - House images stored in `House_images` folder

- 🧠 **Image feature extraction**:
  - Used **pretrained ResNet50** from PyTorch to extract deep features (2048-dimensional vectors) from images
  - Removed the final classification layer to use the CNN as a feature extractor

- ➕ **Feature fusion**:
  - Standardized tabular features (`bed`, `bath`, `sqft`, etc.)
  - Concatenated image features with tabular features into a single combined feature vector

- 📊 **Modeling**:
  - Trained regression models (Linear Regression)
  - Split data into training and test sets to evaluate performance

- 📈 **Evaluation metrics**:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)

---

## 📊 **Key Results / Observations**

| Metric | Score (example run) |
|-------|--------------------:|
| MAE   | ~223,000           |
| RMSE  | ~301,000           |

- The model was able to learn meaningful patterns from both images and structured data
- Using only tabular data or only images produced higher errors, showing that multimodal fusion helps improve prediction accuracy
- Feature engineering and using stronger regressors (e.g., Random Forest, XGBoost) could further improve performance

---
<img width="151" height="36" alt="image" src="https://github.com/user-attachments/assets/6b134521-24ec-4847-b576-85c74062c06b" />


## ✨ **Skills Gained**
- Multimodal machine learning
- Convolutional Neural Networks (CNNs)
- Feature fusion (image + tabular data)
- Regression modeling & evaluation

---
