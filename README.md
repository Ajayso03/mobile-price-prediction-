# 📱 Mobile Phone Price Prediction  

## 📌 Project Overview  
This project builds a **machine learning model** that predicts the **price range** of a mobile phone based on its specifications. The model classifies phones into **four categories**:  

- `0` → Low cost  
- `1` → Medium cost  
- `2` → High cost  
- `3` → Very high cost  

The system uses data about phone hardware features (RAM, battery, camera, etc.) to make predictions.  

---

## 📊 Dataset  
The dataset contains specifications of mobile phones and their corresponding price ranges.  

**Features included:**  
- `battery_power`: Battery capacity in mAh  
- `blue`: Has Bluetooth or not  
- `clock_speed`: Processor speed (GHz)  
- `dual_sim`: Dual SIM support  
- `fc`: Front camera megapixels  
- `four_g`: 4G support  
- `int_memory`: Internal memory in GB  
- `m_deep`: Mobile depth in cm  
- `mobile_wt`: Weight in gm  
- `n_cores`: Number of processor cores  
- `pc`: Primary camera megapixels  
- `px_height`: Pixel resolution height  
- `px_width`: Pixel resolution width  
- `ram`: RAM in MB  
- `sc_h`: Screen height in cm  
- `sc_w`: Screen width in cm  
- `talk_time`: Battery backup (hours)  
- `three_g`: 3G support  
- `touch_screen`: Touchscreen support  
- `wifi`: WiFi support  
- **Target:** `price_range` (0 = low, 1 = medium, 2 = high, 3 = very high)  

---

## ⚙️ Technologies Used  
- **Python** (Data preprocessing & modeling)  
- **Pandas & NumPy** (Data analysis)  
- **Matplotlib & Seaborn** (Visualization)  
- **Scikit-learn** (Model building and evaluation)  
- **Joblib** (Model saving & loading)  
- **Streamlit** (for deployment UI, optional)  

---

## 🚀 Project Workflow  
1. **Data Preprocessing**  
   - Handle dataset, check for missing values, normalize/scale features if required.  
   - Split data into training & testing sets.  

2. **Exploratory Data Analysis (EDA)**  
   - Distribution of features  
   - Correlation with price range  
   - Feature importance analysis  

3. **Model Building**  
   - Used **classification algorithms** (RandomForestClassifier, etc.)  
   - Evaluated accuracy, precision, recall, F1-score.  
   - Selected the best-performing model.  

4. **Model Saving**  
   - Trained model exported using `joblib`.  

5. **Deployment (Optional)**  
   - Streamlit-based UI to input phone specifications and predict price range.  

---

## 📂 Project Structure  
```
📦 Mobile_Price_Prediction
 ┣ 📜 dataset.csv              # Dataset used
 ┣ 📜 mobile_price_prediction_clean.ipynb   # Jupyter Notebook (EDA + model training)
 ┣ 📜 mobile_price_model.joblib # Trained ML model
 ┣ 📜 Predict Mobile Phone Pricing.pdf  # Project report
 ┣ 📜 Book1.csv.xlsx            # Supporting file
 ┣ 📜 README.md                 # Project documentation
```

---

## ▶️ How to Run the Project  

### 🔹 Run Jupyter Notebook  
```bash
jupyter notebook mobile_price_prediction_clean.ipynb
```

### 🔹 Run with Saved Model  
```python
import joblib
import pandas as pd

# Load model
model = joblib.load("mobile_price_model.joblib")

# Example input (must match dataset features)
sample = [[842,1,2.2,1,1,0,20,0.7,188,4,13,800,1200,1500,12,7,19,1,1,1]]
prediction = model.predict(sample)
print("Predicted Price Range:", prediction)
```

### 🔹 Run Streamlit App (if included)  
```bash
streamlit run app.py
```

---

## 📈 Results  
- The best-performing model achieved **high accuracy** in classifying phones into their respective price ranges.  
- **RAM, pixel resolution, and battery power** were among the most important features.  

---

## 🤝 Contribution  
Feel free to fork the repo, open issues, and submit pull requests to improve the project.  

---

## 📜 License  
This project is licensed under the **MIT License**.  
