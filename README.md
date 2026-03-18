# House Price Prediction Project

## 📌 Project Overview

This project focuses on building a **Machine Learning Regression Model** to predict house prices based on various features such as area, number of bedrooms, bathrooms, and other attributes.

---

## 🎯 Objective

To develop a model that can accurately predict house prices using:

* Data preprocessing
* Feature engineering
* Model training & evaluation

---

## 📊 Dataset

The dataset contains housing-related features such as:

* Bedrooms
* Bathrooms
* Square feet (living area, lot area)
* Floors
* Condition
* Year built

Target variable:

* **Price**

---

## ⚙️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib

---

## 🔍 Steps Performed

### 1. Data Preprocessing

* Removed unnecessary columns (date, street, city, etc.)
* Handled missing values
* Converted data into suitable format

### 2. Feature Engineering

* Applied **log transformation** to price
* Performed feature scaling using StandardScaler

### 3. Model Training

Three models were trained:

* Linear Regression
* Random Forest Regressor
* Gradient Boosting Regressor

### 4. Model Evaluation

Models were evaluated using:

* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)

### 5. Residual Analysis

* Checked distribution of prediction errors

---

## 📈 Results

* Ensemble models like **Random Forest** and **Gradient Boosting** performed better than Linear Regression.
* The model was able to capture complex relationships in the data.

---

## 💾 Model Saving

The best model is saved using Joblib:

```python
import joblib
joblib.dump(model, "house_price_model.pkl")
```

---

## 🔮 Prediction Example

```python
import joblib
import numpy as np

model = joblib.load("house_price_model.pkl")

sample = X_test[0].reshape(1, -1)
prediction = model.predict(sample)

print("Predicted Price:", np.exp(prediction))
```

---

## 📂 Project Structure

```
house-price-prediction/
│──house_price_data.csv
|── house_price.ipynb
│── house_price_model.pkl
│── README.md
```

---

## 👩‍💻 Author

**Siddhi Khandave**
BSc Data Science

---

## 🚀 Conclusion

This project demonstrates how machine learning techniques can be used to predict house prices effectively. Proper data preprocessing, feature engineering, and model selection significantly improve performance.

---
