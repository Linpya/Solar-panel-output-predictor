# ☀️ Solar Output Prediction using Regression Models

This repository contains an end-to-end workflow for predicting solar output (in kWh) based on environmental conditions using multiple regression models. The pipeline includes data preprocessing, exploratory data analysis (EDA), model training (with and without scaling), evaluation, and visualization.

---

## 📁 Dataset

We use the publicly available [Solar Panels Output Dataset on Kaggle](https://www.kaggle.com/datasets/js0805/solar-panels-output-dataset), which includes daily weather and solar generation data.

**Features:**

- `Date`: Timestamp (daily resolution)
- `Temperature_C`: Ambient temperature in °C
- `Irradiance_W/m2`: Solar irradiance in W/m²
- `WindSpeed_m/s`: Wind speed in m/s
- `Humidity_%`: Relative humidity in %
- `SolarOutput_kWh`: Target variable – solar energy output in kWh

> All data is from the year **2024**.

---

## 📊 Project Workflow

1. **Data Preprocessing**
   - Convert `Date` to datetime format
   - Extract useful features: `month` and `day`
   - Reorder and drop unnecessary columns

2. **Exploratory Data Analysis**
   - Univariate and bivariate visualizations using seaborn and matplotlib
   - Relationship plots (pairplots, lmplots, displots)
   - Monthly and daily solar output trends

3. **Model Training & Evaluation**
   - Train/test split
   - Trained 9 models:
     - Linear Regression
     - Ridge Regression
     - Lasso Regression
     - Decision Tree
     - Random Forest
     - Gradient Boosting
     - Support Vector Regression (SVR)
     - K-Nearest Neighbors
     - Neural Network (MLP)
   - R² score evaluation
   - With and without feature scaling (`StandardScaler`)

4. **Model Interpretation**
   - Feature importance visualization using Lasso coefficients

---

## 📦 Requirements

Install the dependencies using:

```bash
pip install -r requirements.txt
````

### Required packages

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

---

## 🧪 How to Run

Run the full pipeline by executing:

```bash
python main.py
```

This will:

* Load and preprocess data
* Run EDA
* Train models
* Display R² scores
* Plot feature importances

---

## 📈 Sample Output

```text
Scaled Results:
         Model   R2 Score
0  RandomForest   0.94
1  GradientBoost 0.92
2  Ridge         0.89
...
```

---

## 📂 File Structure

```
├── solar_output.csv         # Dataset
├── main.py                  # Main code file with pipeline
├── README.md                # Project README
└── requirements.txt         # Python dependencies
```

---

## 📌 To-Do

* [ ] Add cross-validation scores
* [ ] Add MAE, RMSE evaluation
* [ ] Hyperparameter tuning
* [ ] Streamlit dashboard for real-time predictions



## 📄 License

This project is open-source under the [MIT License](LICENSE).

