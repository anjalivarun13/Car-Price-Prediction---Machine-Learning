# 🚗 Car Price Prediction Model

This project predicts the price of used cars using **Machine Learning (Linear Regression)** and includes a user-friendly **Flask web application** for real-time predictions.

The model is saved and loaded using **pickle**.

---

## 🖼️ Website Preview

### **Before**
![Website Before](images/before.png)

### **After**
![Website After](images/after.png)

*(Replace the above paths with your actual screenshot locations.)*

---

## 📊 Dataset Overview

### **Columns in Dataset**
- `name`
- `company`
- `year`
- `Price`
- `kms_driven`
- `fuel_type`

---

## 🧹 Data Cleaning & Preprocessing

The dataset had several inconsistencies. Below are the preprocessing steps:

### ✔ Car Name Standardization
- Car names were messy and sometimes contained long descriptions like  
  *“Maruti Ertiga showroom condition with”* or *“Well maintained Tata Sumo”*.  
- Standardized by keeping only the **first 3 words**.

### ✔ Company Column Cleaning
- Many values were not real car companies (e.g., *“Used”*, *“URJENT”*).  
- Filtered and kept only genuine automobile manufacturers.

### ✔ Year Column
- Contained non-year values and stored as `object`.  
- Cleaned and converted to **integer**.

### ✔ Price Column
- Included values like `"Ask for Price"` and had commas.  
- Removed invalid entries, stripped commas, converted to numeric.

### ✔ Kilometers Driven
- Values like `"45000 kms"` were cleaned by extracting only the numeric part.

### ✔ Fuel Type
- Had missing values and misplacements (e.g., `"Petrol"` in wrong rows).  
- Cleaned and corrected.

---

## 🧠 Machine Learning Model

- **Model Used:** Linear Regression  
- **R² Score:** **0.89**  
- Model stored using **pickle**.

---

## 🖥️ Project Structure

├── static/
├── templates/
│ ├── index.html
├── model/
│ ├── car_price_model.pkl
├── data.csv
├── app.py
├── README.md
└── requirements.txt

---

## 🚀 Flask Web Application

The Flask app provides an interactive UI for predicting car prices.

### How It Works:
1. User enters car details  
2. Flask processes the form  
3. Pickle model predicts price  
4. Output is displayed on the webpage  

### ▶ Run the Application

python app.py

Open browser and go to:

http://127.0.0.1:5000

---

## 📦 Installation

1. Clone the repository:

---

## 📦 Installation

1. Clone the repository:

git clone https://github.com/your-username/car-price-prediction.git
cd car-price-prediction

2. Install dependencies:

pip install -r requirements.txt

3. Launch Flask app:

python application.py

---

## 🧪 Example Prediction Input

Company: Maruti
Car Name: Maruti Suzuki Swift
Year: 2019
Kms Driven: 100
Fuel Type: Petrol

**Output:**

Predicted Price: ₹507857.73 (approx.)

---
