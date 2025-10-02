# 🔥 Calories Burnt Prediction using Machine Learning

## 📌 Project Overview
This project predicts the **calories burnt during exercise** based on personal and activity features such as gender, age, height, weight, duration, heart rate, and body temperature.  
The aim is to build an accurate and user-friendly solution that can be used in **fitness apps, wearable devices, and healthcare systems**.

---

## 📂 Dataset
- **Calories.csv** → Contains User_ID and Calories burnt.  
- **Exercise.csv** → Contains User_ID and features such as Age, Gender, Height, Weight, Duration, Heart Rate, Body Temperature.  
- Datasets were merged on `User_ID` to form a single dataset with **15,000+ records**.

---

## 🛠️ Tech Stack
- **Programming Language:** Python  
- **Libraries Used:** Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost, Pickle, Tkinter  

---

## 🔎 Exploratory Data Analysis (EDA)
- Checked dataset info: no missing values, no duplicates.  
- Visualized numerical distributions (Age, Height, Weight, Duration, etc.).  
- Encoded categorical feature `Gender`.  
- Target variable: **Calories**  

---

## ⚙️ Data Preprocessing
- Removed `User_ID` (not useful for prediction).  
- Applied **ColumnTransformer**:  
  - `OrdinalEncoder` → Encode Gender (Male/Female).  
  - `StandardScaler` → Normalize numerical features.  
- Built a **Pipeline** to automate preprocessing + model training.

---

## 🤖 Models Used
1. **Linear Regression**  
   - Simple baseline model.  
   - R² Score: ~0.96  

2. **Random Forest Regressor**  
   - Ensemble of decision trees.  
   - R² Score: ~0.998  

3. **XGBoost Regressor** ✅ (Best Model)  
   - Sequential boosting with regularization.  
   - R² Score: ~0.999  
   - MAE: ~1.49  

---

## 📊 Results
| Model              | R² Score | MAE   |
|--------------------|----------|-------|
| Linear Regression  | 0.967    | Higher error |
| Random Forest      | 0.998    | ~1.68 |
| XGBoost Regressor  | 0.999    | ~1.49 |

✅ **XGBoost was selected as the final model** due to its superior accuracy and performance.

---

## 🖥️ Deployment
- Trained pipeline was saved using **Pickle** (`pipeline.pkl`).  
- Developed a **Tkinter GUI Application** where users can:  
  - Input their details (age, weight, height, etc.).  
  - Get instant calorie predictions.  
  - View results in a simple and user-friendly interface.

---

## 🚀 How to Run
1. Clone the repository  
   ```bash
   git clone https://github.com/your-username/calories-burnt-prediction.git
   cd calories-burnt-prediction
