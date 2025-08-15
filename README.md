# 🍽️ Restaurant Rating Prediction

This project predicts restaurant **Aggregate Ratings** using a cleaned and encoded dataset, trained with a **Decision Tree Regressor**. It also visualizes prediction accuracy and the most influential features.

---

## 📌 Project Overview
The aim is to estimate a restaurant's rating based on its details such as cuisine, location, price range, and other features. The project follows a complete ML workflow — data cleaning, preprocessing, model training, evaluation, and visualization.

---

## ⚙️ Workflow

1. **Data Loading**
   - Load dataset (`.csv` file) using `pandas`.
   - Store restaurant names separately for displaying predictions.

2. **Data Cleaning**
   - Remove rows where `Aggregate rating` is missing.
   - Drop unnecessary columns:  
     `Restaurant ID`, `Address`, `Locality Verbose`, `Locality`, `Votes`, `Rating color`, `Rating text`.
   - Fill missing numeric values with **median** and categorical values with **mode**.

3. **Data Preprocessing**
   - Encode categorical columns using **Label Encoding**.
   - Separate **features (X)** and **target (y)**.

4. **Model Training**
   - Split data into train/test sets.
   - Train a **DecisionTreeRegressor** with `max_depth=8` and `random_state=42`.

5. **Model Evaluation**
   - Predict ratings for test data.
   - Calculate:
     - **RMSE** (Root Mean Squared Error)
     - **R² Score**
   - Compare actual vs predicted ratings.

6. **Visualization**
   - **Scatter Plot** → Shows how close predictions are to actual ratings.
   - **Bar Chart** → Displays the most important features influencing ratings.

---

## 📊 Results
- **Metrics:**
  - RMSE: *(depends on dataset)*
  - R² Score: *(depends on dataset)*
- **Sample Output Table:**
  | Restaurant Name | Actual Rating | Predicted Rating |
  |-----------------|--------------|------------------|
  | Example Name    | 4.1          | 4.0              |
  | Example Name 2  | 3.5          | 3.6              |

---

## 🛠️ Tech Stack
- **Python**
- **pandas**, **numpy** → Data handling
- **scikit-learn** → Machine learning
- **matplotlib** → Visualizations

---

## 📂 File Structure

```
restaurant-rating-prediction/
├── data/
│   └── Dataset.csv
├── src/
│   └── restaurant_rating_prediction.py
├── images/
│   ├── scatter.png
│   └── feature_importance.png
└── README.md
```

