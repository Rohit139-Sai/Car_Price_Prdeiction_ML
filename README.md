# 🚗 Car Price Prediction using Machine Learning

This project was developed as part of **SystemTron ML Internship – Week 2 Task**.

It focuses on predicting the resale value of used cars using a machine learning model, based on features such as:
- Year of manufacture
- Kilometers driven
- Fuel type

The goal is to build a regression model that can estimate the car price accurately based on these inputs.

---

## ⚙️ Tech Stack

This project uses the following tools and technologies:

- **Python** – Programming language
- **Pandas** – Data manipulation and preprocessing
- **NumPy** – Numerical operations
- **Matplotlib** & **Seaborn** – Data visualization
- **Scikit-learn** – Machine learning algorithms and evaluation
- **Google Colab** – Development and execution environment
- **Pickle** – Saving and loading the trained model

---

## 📁 Dataset Overview

The dataset contains historical information about used cars listed for sale.  
It includes several features, out of which only the most relevant were selected for building the model.

### 📌 Columns Used:

| Column        | Description                          |
|---------------|--------------------------------------|
| `year`        | Year the car was purchased           |
| `kms_driven`  | Total distance driven (in kilometers)|
| `fuel_type`   | Type of fuel (Petrol, Diesel, CNG)   |
| `price`       | 💰 Target: Selling price of the car  |

---

🔴 **Dropped Columns:**
- `name`: Car model name (too many unique values)
- `company`: Brand of the car (not used in this model)

---

📌 **Label Encoding for `fuel_type`:**
- Petrol → 2  
- Diesel → 1  
- CNG → 0
  
---

## 🔍 Steps Followed in the Project

### 📥 1. Imported Required Libraries
- Imported Python libraries such as pandas, numpy, matplotlib, seaborn, scikit-learn, and pickle to handle data processing, visualization, machine learning, and model saving.

### 📂 2. Loaded the Dataset
- Loaded the car price dataset into a DataFrame using pandas.
- Viewed the dataset using `.head()`, `.info()`, and `.describe()` to understand its structure.

### 🧹 3. Cleaned the Dataset
- Removed unnecessary columns like `name` and `company` which were not useful for prediction.
- Cleaned string values in the `price` and `kms_driven` columns and converted them into numerical format.
- Converted `year` column to integer format.

### 🔁 4. Encoded Categorical Features
- Applied label encoding to convert the `fuel_type` column into numerical values so that machine learning models can understand them.

### 🧪 5. Split the Data
- Separated the dataset into features (`X`) and target (`y`), and then split it into training and testing sets using an 80/20 ratio.

### 🤖 6. Trained the Model
- Used the **Random Forest Regressor** algorithm to train the model on the training dataset.

### 📈 7. Evaluated the Model
- Evaluated the performance of the model using:
  - **R² Score**
  - **Mean Absolute Error (MAE)**
  - **Root Mean Squared Error (RMSE)**

### 💾 8. Saved the Model
- Saved the trained model using Python’s `pickle` library so that it can be reused later for predictions.

### 🔮 9. Made Predictions
- Tested the model by giving new inputs like year, kilometers driven, and fuel type to predict the price of a used car.

---

## 📊 Model Evaluation

After training the model using Random Forest Regressor, its performance was evaluated using the following metrics:

- **R² Score** – Measures how well the predicted prices fit the actual prices.  
- **Mean Absolute Error (MAE)** – Shows the average difference between predicted and actual prices.  
- **Root Mean Squared Error (RMSE)** – Penalizes large errors more than MAE; gives a better sense of overall model error.

The model showed good accuracy in predicting used car prices on the test dataset.

---
## 🔮 Sample Output

When providing new input (e.g., a 2019 Petrol car driven for 35,000 km), the model predicts an approximate resale price like:

The actual output may vary slightly based on input values and model tuning.

---
## 👤 Author

**Dasari Sai Ram**  
B.Tech in Civil Engineering  
SRKR Engineering College  
SystemTron ML Intern – Week 2 Task  
🔗 [www.systemtron.in](https://www.systemtron.in)

---

## 📌 Acknowledgement

This project was created as a part of the **SystemTron Machine Learning Internship – Week 2** assignment.

It helped me explore a complete regression workflow from data cleaning to model deployment.

---

## 📄 License

This project is open-source and intended for learning and demonstration purposes only.





