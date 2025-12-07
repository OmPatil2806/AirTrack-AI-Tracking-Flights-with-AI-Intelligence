# AirTrack AI – Predicting US Flight Delays with Machine Learning

AirTrack AI is a comprehensive machine learning project designed to predict flight delays in the US. Using historical flight data, the project leverages advanced ML models including *XGBoost, **LightGBM, and **CatBoost* to provide actionable insights for airlines, airports, and passengers.

---

## 🚀 Project Overview

Flight delays cause operational challenges, financial losses, and customer dissatisfaction. Predicting delays before they occur allows airlines to:

- Optimize scheduling
- Improve passenger experience
- Minimize operational costs

This project builds an end-to-end ML pipeline to forecast delays based on historical flight, weather, and airport data.

---

## 📂 Dataset

- *Source:* US Flight Delays dataset (2024)  
- *Size:* ~7M rows, 35+ columns  

*Key Features:*

- *Flight schedule:* year, month, day_of_month, day_of_week, fl_date  
- *Airline info:* op_unique_carrier, op_carrier_fl_num  
- *Airport info:* origin, origin_city_name, origin_state_nm, dest, dest_city_name, dest_state_nm  
- *Flight times:* dep_time, arr_time, crs_dep_time, crs_arr_time, taxi_out, taxi_in, air_time  
- *Delays & cancellations:* dep_delay, arr_delay, cancelled, cancellation_code  
- *Distance & other features:* distance, carrier_delay, weather_delay, NAS_delay, security_delay, late_aircraft_delay

---

## 🛠 Project Pipeline

### Data Exploration
- Inspect dataset shape, types, and summary statistics
- Analyze target variable (Delayed) distribution
- Visualize delays by airline, airport, and month

### Data Preprocessing
- Handle missing values
- Remove duplicates and outliers
- Convert data types and create new features (e.g., hour, day, month, delay flags)
- Encode categorical variables and scale numeric features

### Train–Test Split
- Stratified 80:20 split for train and test sets

### Handle Imbalanced Data
- Use *SMOTE* to balance delayed vs on-time flights in the training set

### Model Training
- *XGBoost:* Tune n_estimators, learning_rate, max_depth, subsample, colsample_bytree  
- *LightGBM:* Tune num_iterations, learning_rate, num_leaves, max_depth  
- *CatBoost:* Tune iterations, learning_rate, depth, l2_leaf_reg  
- Track validation metrics and use early stopping

### Model Evaluation
- Metrics: Accuracy, Precision, Recall, F1-score, ROC–AUC
- Confusion matrix visualization
- Compare all models to select the best performer

---

## 📊 Results

| Model     | Accuracy | Precision | Recall  | F1-score |
|----------|---------|-----------|--------|----------|
| XGBoost  | 0.9989  | 0.9961    | 0.9992 | 0.9977   |
| LightGBM | 0.9993  | 0.9976    | 0.9993 | 0.9985   |
| CatBoost | TBD     | TBD       | TBD    | TBD      |

*Best Performing Model:* LightGBM (highest accuracy and F1-score)  

Confusion matrices show high prediction performance for delayed and on-time flights.

---

## 📈 Key Features
- Flight schedule details
- Airline and airport information
- Distance categories and congestion features
- Delay flags for weather, carrier, NAS, security, and late aircraft

---

## 🔧 Technologies Used
- *Languages:* Python  
- *Libraries:* pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn, XGBoost, LightGBM, CatBoost  
- *Environment:* Jupyter Notebook  

---

## 💡 Business Impact
- Predicting flight delays improves airline operational efficiency
- Enhances passenger experience by anticipating delays
- Reduces financial losses due to delayed flights
- Identifies key factors contributing to flight delays

## 👤 Author

*Om Patil*  
📧 Data Science & Machine Learning Enthusiast  
🔗 [Connect with me on LinkedIn](https://www.linkedin.com/in/om-patil-039863369/)  
👨‍💻 [GitHub Profile](https://github.com/OmPatil2806)
