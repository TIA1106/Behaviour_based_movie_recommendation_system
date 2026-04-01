# Behaviour-Based Movie Rating Prediction System

A Machine Learning project that predicts movie ratings by modelling **dynamic user behaviour using genre transitions**, instead of assuming static preferences.

---

## 🚀 Overview

Traditional recommendation systems assume that user preferences do not change over time.
However, in reality, user behaviour is dynamic.

This project introduces a **behaviour-based approach** where we model how users transition between movie genres and use that information to predict ratings.

---

## 🎯 Key Idea

Instead of:

> “User likes Action → always recommend Action”

We model:

> “User moved from Action → Comedy → Drama”

👉 This **sequence of behaviour** is used to improve prediction accuracy.

---

## 📂 Dataset

We used the **MovieLens Dataset**:

* ~100,000 ratings
* ~9,700 movies

### Features:

* `userId`
* `movieId`
* `rating`
* `timestamp`
* `genres`

---

## 🧠 Workflow

### 1️⃣ Exploratory Data Analysis (EDA)

* Rating distribution analysis
* Genre popularity analysis
* Genre transition heatmap

### 🔥 Key Insight:

User behaviour is **sequential and pattern-based**, not random.

---

### 2️⃣ Preprocessing & Feature Engineering

* Encoding categorical features (genres)
* Creating **genre transition features**
* Generating:

  * `user_avg_rating`
  * `movie_avg_rating`
  * `transition features`

👉 These features capture **user behaviour over time**

---

### 3️⃣ Model Training

We trained 5 models:

| Model               | Type                  |
| ------------------- | --------------------- |
| Linear Regression   | Regression            |
| Logistic Regression | Classification        |
| SVR (SVM)           | Non-linear regression |
| KNN                 | Distance-based        |
| Decision Tree       | Non-linear tree       |

---

## 📊 Model Evaluation

We used:

* **RMSE** → prediction error
* **MAE** → average error
* **R² Score** → model explanation power
* **Confusion Matrix** → classification-style evaluation

---

## 📈 Results Summary

| Model               | RMSE       | MAE        | R²         |
| ------------------- | ---------- | ---------- | ---------- |
| Linear Regression   | 0.8219     | 0.6343     | 0.3748     |
| Logistic Regression | 1.3820     | 0.9806     | -0.7678    |
| SVR (SVM)           | 0.8188     | 0.6286     | 0.3795     |
| KNN                 | 0.8330     | 0.6287     | 0.3578     |
| Decision Tree ⭐     | **0.8173** | **0.6116** | **0.3817** |

---

## 🏆 Best Model: Decision Tree

### Why it performed best:

* Captures **non-linear relationships**
* Learns **feature interactions**
* Handles **behavioural patterns effectively**

---

## 📊 Visual Insights

### 🔹 Confusion Matrix

* Strong predictions for rating **4**
* Matches dataset distribution (most frequent rating)

### 🔹 Actual vs Predicted Plot

* Linear Regression → scattered
* Decision Tree → closer to ideal line

### 🔹 Feature Importance

* `movie_avg_rating` → most important
* `user_avg_rating` → second
* Behavioural features also contribute

---

## 🧠 Key Learnings

* User behaviour is **dynamic and sequential**
* Simple models fail to capture real-world complexity
* Feature engineering is **critical for performance**
* Tree-based models handle behavioural data better

---

## ⚠️ Limitations

* No hyperparameter tuning (baseline models)
* No deep learning / sequence models
* Limited to structured data (no text or embeddings)

---

## 💡 Conclusion

This project shows that:

> “Understanding user behaviour is more important than just using powerful models.”

By modelling **genre transitions**, we moved closer to building a realistic and intelligent recommendation system.

---

## 👩‍💻 Authors

* Tia Sukhnanni
* Yashi Sharma
* Pratigya Bomb

