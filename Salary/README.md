# Salary Prediction using Simple Linear Regression

## 📌 Overview
This project applies a **Simple Linear Regression** machine learning model to predict an employee's salary based on their years of experience. It includes comprehensive Exploratory Data Analysis (EDA), statistical evaluation, and data visualization to understand the relationship between experience and income.

## 📊 Dataset
The project uses `Salary_dataset.csv`, which contains two primary columns:
* **`YearsExperience`**: The independent variable (X) representing the number of years an individual has worked.
* **`Salary`**: The dependent variable (y) representing the annual salary in dollars.

## 🛠️ Technologies & Libraries Used
This project is built using Python. The following libraries are required:
* `pandas` - For data manipulation and analysis
* `scikit-learn` - For building and evaluating the Machine Learning model
* `matplotlib` & `seaborn` - For advanced statistical visualizations

## 🚀 How to Run
1. Clone the repository and ensure Python is installed.
2. Install the required dependencies:
   `pip install pandas scikit-learn matplotlib seaborn`
3. Run the Jupyter Notebook cells or execute the Python script:
   `python salary_prediction.py`

## 📈 Model Performance & Results
* **Base Salary (Intercept):** $24,380.20
* **Annual Increase (Slope):** $9,423.82 
* **R-squared (Accuracy):** `0.9024` (The model explains over 90% of the variance in the data).
