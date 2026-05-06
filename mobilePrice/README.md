# 📱 Mobile Phone Price Classification

## 📌 Project Overview

In the highly competitive mobile phone market, estimating the correct price of a new device is crucial. This project aims to solve this business problem by building a Machine Learning model that predicts the **price range** of mobile phones based on their hardware specifications (e.g., RAM, Battery Power, Screen Resolution).

Instead of predicting the exact price, the model classifies phones into four distinct tiers:

- `0` : Low Cost
- `1` : Medium Cost
- `2` : High Cost
- `3` : Premium

## 📊 Dataset Description

The project uses a dataset containing various mobile phone features.

- **Features:** 20 attributes including `ram`, `battery_power`, `px_height`, `px_width`, `clock_speed`, `dual_sim`, etc.
- **Target Variable:** `price_range`

## 🛠️ Data Preprocessing

- **Feature Scaling:** Applied `StandardScaler` to normalize the data. This step was critical because features like RAM (measured in thousands) and physical dimensions (measured in decimals) have vastly different scales, which heavily impacts distance-based algorithms.

## 🤖 Models Comparison: SVM vs. Random Forest

To find the most accurate predictor, two different classification models were trained and compared:

### 1. Support Vector Machine (SVM) - _Best Performer_

- **Kernel:** Linear
- **Accuracy:** **97%**
- **Why it worked best:** The relationship between core mobile specs (like RAM) and the price range is highly linear. SVM with a linear kernel excelled at drawing clear, straight decision boundaries between the different price tiers.
- **Note:** SVM is highly sensitive to feature scales, making the `StandardScaler` step essential for this 97% accuracy.

### 2. Random Forest Classifier

- **Accuracy:** **~89%**
- **Why we used it:** While slightly less accurate than SVM for this specific linear dataset, Random Forest is robust to outliers and does not require feature scaling. More importantly, it allowed us to easily extract **Feature Importance** to understand _how_ the market prices phones.

## 💡 Key Business Insights

By utilizing the Feature Importance from the Random Forest model, we extracted the following market insights:

1. **RAM is King:** The amount of RAM is by far the most dominant factor in deciding a phone's price tier.
2. **Battery & Display:** `battery_power` and screen resolution (`px_height` / `px_width`) are the next most valuable features to consumers.
3. **Standardized Features:** Features like 3G/4G capability, Bluetooth, or Dual SIM support have very little impact on price variations, as they are now considered standard across all tiers.

## 🚀 How to Run

1. Clone this repository.
2. Ensure you have `pandas`, `scikit-learn`, and `matplotlib` installed.
3. Run the Python scripts or Jupyter Notebook to train the models and generate predictions for the `test.csv` dataset.

---

**Author:** Fedaa Mohammad | AI & Systems Engineer
