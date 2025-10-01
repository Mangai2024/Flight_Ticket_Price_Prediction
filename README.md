# Flight_Ticket_Price_Prediction
📌 **Project Overview**

This project predicts flight ticket prices based on features such as airline, source city, destination city, departure time, arrival time, class, duration, stops, and days left before travel.
The goal is to build a machine learning model that can accurately estimate ticket prices and assist in better pricing strategies.

📊 **Dataset**

Rows: ~300,000

Columns: 12

Features include:

airline, source_city, destination_city, departure_time, arrival_time, stops, class

duration, days_left

Target variable: price

Unnecessary columns like Unnamed: 0 and flight were dropped during preprocessing.

⚙️ Steps Followed

Data Understanding → Checked shape, columns, and missing values.

Preprocessing → Dropped irrelevant columns, handled categorical variables with One-Hot Encoding.

Train-Test Split → Divided dataset into training (80%) and testing (20%).

Model Training → Tried Linear Regression, Random Forest, and XGBoost.

Hyperparameter Tuning → Applied RandomizedSearch on XGBoost to improve performance.

Evaluation → Compared models using MAE, RMSE, and R².

📈****** **Model Performance******
Before Tuning

Random Forest → R² ≈ 0.74

XGBoost → R² ≈ 0.77

**After Hyperparameter Tuning**

XGBoost (Tuned) → R² ≈ **0.98 🎯
**
💾 Model Saving

The best-performing model (tuned XGBoost) was saved as a .pkl file using joblib for deployment.

import joblib
joblib.dump(best_xgb, "xgboost_flight_model.pkl")

🚀 Future Improvements

Use feature engineering (e.g., interaction terms between features).

Apply cross-validation for more robust evaluation.

Deploy as a web app using Streamlit or FastAPI.

🏆 Key Takeaway

This project demonstrates the complete ML pipeline — from data preprocessing to model building, tuning, and saving the model for deployment.
