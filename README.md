# 🚦 Traffic Situation Prediction using Random Forest

This project uses machine learning to predict traffic situations (e.g., heavy, moderate, or light) based on vehicle counts and time-based features using a Random Forest Classifier.

---

## 📂 Dataset

The dataset used is `TrafficTwoMonth.csv`, which includes:
- Vehicle counts: `CarCount`, `BikeCount`, `BusCount`, `TruckCount`, `Total`
- Timestamps: `Date`, `Time`, `Day of the week`
- Label: `Traffic Situation` (categorical: e.g., Heavy, Medium, Light)

---

## 🧼 Data Preprocessing

1. Combined `Date` and `Time` into a full datetime object.
2. Extracted datetime features: `hour`, `day`, `month`, `weekday`.
3. Encoded:
   - `Traffic Situation` using `LabelEncoder` (target variable)
   - `Day of the week` to numerical values
4. Dropped any rows with invalid or missing datetime information.

---

## 🎯 Model

- **Model Used:** Random Forest Classifier
- **Hyperparameter Tuning:** GridSearchCV
  - `n_estimators`: [100, 200]
  - `max_depth`: [10, 20, None]
  - `min_samples_split`: [2, 5]
  - `min_samples_leaf`: [1, 2]
- **Evaluation Metrics:**
  - Accuracy
  - Weighted F1 Score
  - Confusion Matrix
  - Classification Report

---

## 📊 Visualizations

- **Class Distribution Plot:** Distribution of traffic situations in the dataset.
- **Confusion Matrix Heatmap:** Performance visualization of the model.
- **Feature Importances:** Importance of each feature in prediction.

---

## 🏁 Results

- Best model is saved as `best_random_forest_model.pkl` using `joblib`.
- Sample inference is demonstrated using a single row from the validation set.

---

