# 🍔 Food Delivery Time Prediction and Analysis

## 📌 Project Overview

Food Delivery Time Prediction and Analysis is a data science and machine learning project that analyzes food delivery records and investigates whether information available at the time of ordering can be used to predict delivery duration.

The project covers data cleaning, exploratory data analysis, feature engineering, visualization, regression modeling, and model evaluation.

---

## 🎯 Objectives

- Analyze food delivery data and identify delivery-time patterns.
- Clean and preprocess order and delivery datasets.
- Perform Exploratory Data Analysis (EDA).
- Visualize important patterns and relationships in the data.
- Engineer features suitable for machine learning.
- Build a regression model to predict delivery duration.
- Compare the regression model against a baseline prediction.

---

## 📊 Dataset

The project uses the **Food Delivery Sample Database**, a synthetic dataset created for educational and analytical purposes.

The dataset contains multiple related CSV tables representing different components of a food delivery marketplace.

The main tables used for prediction are:

- `orders.csv`
- `deliveries.csv`

These tables are joined using the order identifier.

The analysis focuses on completed orders created during **2025**.

After preprocessing and filtering, the final analytical dataset contains **251 completed deliveries**.

---

## 🧹 Data Preprocessing

The preprocessing stage includes:

- Parsing date and time columns.
- Joining order and delivery information.
- Filtering completed deliveries.
- Selecting orders created during 2025.
- Calculating delivery duration in minutes.
- Checking missing values and duplicates.
- Removing invalid delivery durations.
- Creating time-based features.

---

## 📈 Exploratory Data Analysis

Several analyses and visualizations are performed, including:

- Distribution of delivery duration.
- Number of completed orders by month.
- Average delivery duration by month.
- Relationship between order hour and delivery duration.
- Correlation analysis between numerical features.

The completed deliveries have an average delivery duration of approximately **50.4 minutes**, with a median of approximately **49 minutes**.

---

## ⚙️ Feature Engineering

The following features are used for prediction:

- Order hour
- Month
- Weekday
- Delivery fee
- Total order amount

### Target Variable

**Delivery Duration (minutes)**

Delivery duration is calculated as:

`Delivery Time - Order Creation Time`

---

## 🤖 Machine Learning Model

The project uses **Linear Regression** to predict delivery duration.

A chronological train-test split is used:

- **Training:** January to August
- **Testing:** September to December

A mean prediction baseline is also created so that the performance of the regression model can be properly compared.

---

## 📊 Model Performance

| Model | MAE | RMSE |
|---|---:|---:|
| Mean Baseline | 13.07 min | 15.71 min |
| Linear Regression | 13.97 min | 16.74 min |

**Linear Regression R² Score:** `-0.135`

The Linear Regression model did not outperform the baseline model. This indicates that the available features do not contain enough predictive information to accurately estimate delivery duration.

---

## ⚠️ Limitations

The dataset does not contain several important real-world factors that can influence food delivery time, including:

- Delivery distance
- Traffic conditions
- Weather conditions
- Restaurant preparation time
- Courier availability
- Promised delivery time

The dataset is also synthetic, so the results should not be interpreted as the performance of a real food delivery platform.

---

## 🚀 Future Improvements

The project can be improved by:

- Using a larger real-world dataset.
- Adding delivery distance.
- Including traffic and weather information.
- Adding restaurant preparation time.
- Including courier-related information.
- Testing models such as Random Forest and Gradient Boosting.
- Performing hyperparameter tuning.
- Developing an interactive prediction application.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📁 Project Structure

```text
Food-Delivery-Time-Prediction-and-Analysis/
│
├── data/
│   ├── README.md
│   └── Dataset CSV files
│
├── images/
│   └── Project visualizations
│
├── notebooks/
│   └── food_delivery_analysis.ipynb
│
├── report/
│   └── Food_Delivery_Analysis_Report.pdf
│
├── .gitignore
├── README.md
└── requirements.txt
```

---


## 📄 Project Report

The complete project report containing the methodology, exploratory analysis, model development, results, limitations, and conclusions is available in the `report` folder.

---

## 👩‍💻 Authors

**Aaratrika Srivastava**  
**Saanvi Pirta**

---

## 📚 Dataset Source

**Food Delivery Sample Database – Database Sample**

The dataset is synthetic and intended for educational and practice purposes.
