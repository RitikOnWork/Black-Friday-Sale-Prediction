# 🛍️ Black Friday Sales Prediction

An end-to-end Machine Learning project to predict customer purchase amounts during Black Friday sales based on customer demographics and product details. By predicting purchase behaviors, businesses can optimize pricing strategies, improve inventory management, and design personalized marketing campaigns to maximize revenue.

---

## 📋 Project Overview

During Black Friday, retail stores offer massive discounts, leading to a surge in traffic and transaction volume. This project analyzes a dataset containing historical transaction records from a retail store to build a predictive model. 

* **Objective:** Predict the continuous target variable `Purchase` (the transaction amount).
* **Core Algorithm:** **Random Forest Regressor** (Ensemble Learning).
* **Key Steps:** Exploratory Data Analysis (EDA), Missing Value Imputation, Categorical Feature Encoding, Model Training, and Evaluation.

---

## 📊 Dataset Description

The project uses the [BlackFridaySales.csv](file:///e:/Slash%20Mark%20IT%20Solutions%20%28OPC%29%20Pvt.%20Ltd/Black%20Friday%20Sale%20Prediction/BlackFridaySales.csv) dataset, which contains **550,068 observations** and **12 attributes**:

| Feature Name | Data Type | Description |
| :--- | :--- | :--- |
| `User_ID` | Integer | Unique identifier for each customer |
| `Product_ID` | Object (String) | Unique identifier for each product |
| `Gender` | Object (String) | Gender of the customer (`M` / `F`) |
| `Age` | Object (String) | Age group intervals (e.g., `0-17`, `18-25`, `26-35`, `36-45`, `46-50`, `51-55`, `55+`) |
| `Occupation` | Integer | Masked occupation code of the customer (0 to 20) |
| `City_Category` | Object (String) | Category of the city where the customer resides (`A`, `B`, `C`) |
| `Stay_In_Current_City_Years` | Object (String) | Duration of stay in current city (e.g., `0`, `1`, `2`, `3`, `4+`) |
| `Marital_Status` | Integer | Marital status of the customer (`0` = Unmarried, `1` = Married) |
| `Product_Category_1` | Integer | Primary category of the product |
| `Product_Category_2` | Float | Secondary category of the product (contains missing values) |
| `Product_Category_3` | Float | Tertiary category of the product (contains missing values) |
| **`Purchase`** (Target) | Integer | Purchase amount in currency units |

---

## 🛠️ Technology Stack

* **Programming Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Machine Learning Framework:** `scikit-learn`

---

## ⚙️ Data Preprocessing & Modeling Workflow

1. **Handling Missing Values:**
   * Missing values in `Product_Category_2` and `Product_Category_3` indicate that the product does not belong to a secondary/tertiary category. These were handled appropriately during preprocessing.
2. **Feature Encoding:**
   * Categorical features like `Gender`, `Age`, `City_Category`, and `Stay_In_Current_City_Years` were converted into numeric values using label encoding (`LabelEncoder`).
3. **Data Splitting:**
   * The processed dataset was split into training and testing sets (typically 80/20 split) to validate model performance.
4. **Model Architecture:**
   * Trained a **Random Forest Regressor** with `n_estimators=200` to learn robust decision paths across the dataset.

---

## 📈 Model Performance & Evaluation

The trained Random Forest Regressor model yielded the following evaluation metrics on the test dataset:

* **Mean Absolute Error (MAE):** `2,225.55`
* **Mean Squared Error (MSE):** `9,359,895.61`
* **Root Mean Squared Error (RMSE):** `3,059.39`
* **R² (Coefficient of Determination) Score:** `0.6275` (~62.7% variance explained)

> [!NOTE]
> Random Forest Regressor was selected for its capability to handle complex non-linear relationships and interactions among categorical and numerical variables without requiring feature scaling.

---

## 🚀 How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/RitikOnWork/Black-Friday-Sale-Prediction.git
cd Black-Friday-Sale-Prediction
```

### 2. Install Required Dependencies
Ensure you have Python installed, then install the packages:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Open the Jupyter Notebook
Run Jupyter Notebook or JupyterLab to inspect the EDA and run the model pipeline:
```bash
jupyter notebook Black_Friday_Sale_Predictiontled.ipynb
```

---

## 📂 Repository Structure

* [Black_Friday_Sale_Predictiontled.ipynb](file:///e:/Slash%20Mark%20IT%20Solutions%20%28OPC%29%20Pvt.%20Ltd/Black%20Friday%20Sale%20Prediction/Black_Friday_Sale_Predictiontled.ipynb) - Core Jupyter Notebook with data processing, visualization, modeling, and evaluation.
* [BlackFridaySales.csv](file:///e:/Slash%20Mark%20IT%20Solutions%20%28OPC%29%20Pvt.%20Ltd/Black%20Friday%20Sale%20Prediction/BlackFridaySales.csv) - Raw dataset.
* [.gitignore](file:///e:/Slash%20Mark%20IT%20Solutions%20%28OPC%29%20Pvt.%20Ltd/Black%20Friday%20Sale%20Prediction/.gitignore) - Specifies untracked files to ignore.
* [README.md](file:///e:/Slash%20Mark%20IT%20Solutions%20%28OPC%29%20Pvt.%20Ltd/Black%20Friday%20Sale%20Prediction/README.md) - Project documentation.
