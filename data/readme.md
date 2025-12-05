# Sample Landslide Monitoring Dataset (`sample.csv`)

This dataset contains multivariate time-series sensor readings collected from a landslide-prone monitoring site.  
Each row represents the most recent sensor measurements at a particular time.  
The target column represents the **movement class** at the next timestep (t+1).

The dataset is used in the deep learning models included in this repository:
- MLP (ANN)
- 1D-CNN
- CNN + LSTM
- Simple LSTM
- Bidirectional LSTM

---

## 📌 File: `sample.csv`

### **Shape**
Each row contains:
- **13 input sensor features + 3 lagged time steps (t-1, t-2, t-3)**
- **1 target movement class**

Total columns: **53**

---

## 🔢 **Column Descriptions**

Below is the typical meaning of each feature present in the dataset:

| Column Name | Description |
|-------------|-------------|
| `rainfall` | Rainfall intensity (mm/hr) measured by rain gauge sensors |
| `soil_moisture` | Soil water content; higher values indicate saturation risk |
| `pore_pressure` | Subsurface pore water pressure (kPa); contributes to slope instability |
| `acceleration` | IMU-based ground vibration or acceleration readings |
| `displacement` | Cumulative ground movement from extensometers or tiltmeters |
| `tilt_angle` | Change in slope angle (degrees) |
| `temperature` | Ambient or subsurface temperature |
| `humidity` | Atmospheric humidity percentage |
| `geophone` | Vibrational energy detected in the soil (proxy for micro-movements) |
| `strain` | Deformation of slope mass or supporting structures |
| `water_level` | Groundwater/table level relative to sensors |
| `pressure` | Atmospheric or sensor housing pressure |
| `lag_feature` | Any additional engineered feature (moving averages, gradients, etc.) |
| `movement_class` | {0 = Stable, 1 = Moderate movement, 2 = Critical movement} |
| **`movement_class_t+1`** | Target label: {0 = Stable, 1 = Moderate movement, 2 = Critical movement} |

> *Note:* Column names may vary based on the preprocessing file. Update the names above if your dataset uses specific labels.

---

## 🎯 **Target Column**
`movement_class_t+1`  
- `0` → No movement / Stable  
- `1` → Moderate movement  
- `2` → Critical movement / High-risk event  

This is integer-encoded and used for multi-class classification using **softmax**.

---

## 📘 Usage in Deep Learning Models

All models treat each row (or timestep window) as one input sample.  
For sequential models (LSTM, CNN-LSTM), the dataset is reshaped into: (batch_size, time_steps, num_features), ex: (32, 4, 13)
For MLP & 1D CNN, the dataset is reshaped into: (batch_size, 13)

