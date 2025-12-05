# Deep Models for Landslide Prediction

This repository contains deep learning models developed for predicting landslide movements using multi-sensor time-series data collected from real-world landslide monitoring stations (Mandi, Himachal Pradesh, India).

## 📘 Included Notebooks

### 1. Landslide_Movements_Prediction_using_LSTM_models.ipynb
Implements:
- Simple LSTM
- CNN-LSTM
- BiLSTM
- Thresholding
- Metrics computation
- Confusion matrices

### 2. Landslide_Prediction_for_MLP_CNN.ipynb
Implements:
- MLP (ANN)
- 1D-CNN
- CNN-LSTM comparison
- Evaluation on holdout dataset
- Results

## 📂 Structure
- `notebooks/` – all Jupyter notebooks
- `models/` – saved model weights (optional)
- `plots/` – training graphs, confusion matrices
- `data/` – sample datasets (if permitted to upload)

## 🧠 Goal
Develop standard models for land movement prediction at t+1 based on multi-sensor monitoring data.

## 🔬 Techniques
- LSTM, BiLSTM, CNN, MLP
- EarlyStopping, ModelCheckpoint
- Custom thresholding

