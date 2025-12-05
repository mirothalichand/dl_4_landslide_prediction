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
- `data/` – input data (multi-sensors data)


## 🧠 Goal
Develop standard models for land movement prediction at t+1 based on multi-sensor monitoring data.

## 🔬 Techniques
- LSTM, BiLSTM, CNN, MLP
- EarlyStopping, ModelCheckpoint
- Custom thresholding


---

## 🧪 Example Workflow

1. Load dataset using `pandas.read_csv()`
2. Drop missing values
3. Scale features using `StandardScaler`
4. Create `(X, y)` arrays using the provided DataEngine class
5. Split into:
   - Training set  
   - Validation set  
   - Holdout test set  
6. Train one or more models:
   - LSTM / BiLSTM  
   - CNN-LSTM  
   - MLP / CNN  
7. Evaluate model using accuracy, precision, recall, F1-score, confusion matrix
8. Apply thresholding for calibration if needed

---



