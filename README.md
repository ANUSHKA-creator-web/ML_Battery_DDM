# 🔋 Battery Capacity Degradation Prediction using Machine Learning

## 📌 Project Overview
This project focuses on **predicting the capacity degradation of Li-ion batteries** over charge-discharge cycles using multiple machine learning models. Battery degradation is a critical factor in Electric Vehicle (EV) performance and lifespan, and accurate prediction enables better **battery health monitoring, predictive maintenance, and lifecycle management**.

The dataset consists of **battery cycle life data** where the battery capacity decreases with each cycle. Multiple machine learning regression models are trained and compared against true battery capacity degradation curves.

---

## ⚙️ Models Implemented
The following regression models were used:
- **K-Nearest Neighbors (KNN)**
- **Random Forest Regressor**
- **Gradient Boosting Regressor**
- **Support Vector Regressor (SVR)**
- **Ridge Regression**

---

## 📊 Results & Analysis

### 1. **Predicted vs True Capacity**
![Battery Prediction](B_2.png)

- The **black line** represents the **true battery capacity**.
- Colored dots represent predictions from different models.
- Observations:
  - **SVR** and **Ridge Regression** tend to capture smooth degradation but with some bias.
  - **Random Forest** and **Gradient Boosting** follow true capacity closely, though with slight overfitting on noise.
  - **KNN** predictions are more scattered and sensitive to local fluctuations.

---

### 2. **Smoothed Model Comparison**
![Smoothed Comparison](B_1.png)

- Curves represent **average smoothed predictions** vs. true capacity.
- Observations:
  - **Gradient Boosting** and **Random Forest** achieve the closest match to true degradation trends.
  - **SVR** shows a slightly higher prediction at early cycles but aligns well later.
  - **Ridge Regression** underestimates capacity at later cycles.
  - **KNN** is less stable compared to ensemble methods.

---

## ✅ Key Insights
- Ensemble models (**Random Forest, Gradient Boosting**) provided the most accurate predictions overall.
- **SVR** captured non-linear degradation patterns but with small systematic deviations.
- **Ridge Regression** is more stable but less accurate for long-term degradation.
- **KNN** is not suitable for long-term trend prediction due to its local dependency.

---

## 🚀 How to Run
1. Clone the repository / download files.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook Battery_ML.ipynb
   ```

---

## 📈 Future Work
- Integrating **Deep Learning models (LSTMs, RNNs, Transformers)** for time-series degradation prediction.
- Applying **transfer learning** to generalize across different battery chemistries.
- Building a **Digital Twin** of the battery for real-time health estimation.
