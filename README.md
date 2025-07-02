
---

## Dataset Description

**E_Commerce.csv** contains online retail transactions with features such as:

- **OrderID**: Unique identifier for each purchase  
- **CustomerID**: Anonymized customer identifier  
- **OrderDate**: Date and time of the order  
- **ProductCategory**: Categorical label for the item purchased  
- **UnitPrice**: Price per unit (in local currency)  
- **Quantity**: Number of units sold  
- **Revenue**: Total order value (UnitPrice × Quantity)  

---

## Technologies & Libraries

- **Python 3.x**  
  - `pandas`, `numpy` for data manipulation  
  - `matplotlib`, `seaborn` for EDA and plotting  
  - `scikit‑learn` for feature engineering, modeling, and evaluation  
- **Jupyter Notebook**  
- **Power BI** for interactive dashboards  

---

## Key Steps & Findings

1. **Data Cleaning & Preprocessing**  
   - Converted `OrderDate` to `datetime`, extracted **day**, **month**, and **hour**  
   - Handled missing values via imputation or row removal  
   - Dropped duplicate transactions  

2. **Exploratory Data Analysis**  
   - Distribution of `Revenue`, `UnitPrice`, and `Quantity`  
   - Top‑selling product categories and monthly sales trends  
   - Correlation heatmap to identify relationships between features  

3. **Feature Engineering**  
   - Created `OrderHour`, `OrderMonth`, and `DayOfWeek` from `OrderDate`  
   - One‑hot encoded `ProductCategory`  
   - Standardized numeric features (`UnitPrice`, `Quantity`, etc.)  

4. **Model Building & Evaluation**  
   - Trained four regressors:
     - **Linear Regression**  
     - **Decision Tree Regressor**  
     - **Random Forest Regressor**  
     - **K‑Nearest Neighbors Regressor**  
   - Evaluated using **R²** and **RMSE**  

5. **Hyperparameter Tuning**  
   - Performed `GridSearchCV` on **Random Forest**  
   - Selected best parameters for `n_estimators` and `max_depth`  


7. **Conclusions & Recommendations**  
   - **Key Drivers of Revenue**: Unit price, quantity sold, and order timing  
   - **Best Model**: Random Forest Regressor (R² ≈ 0.5, RMSE ≈ 25)  
   - **Business Insights**:
     - Peak sales occur during weekends and holiday months  
     - Certain product categories consistently outperform others  
   - **Next Steps**: Incorporate customer demographics, marketing campaign data, and deploy model via Streamlit for real‑time revenue forecasting  

---

## How to Run

1. **Clone** the repository:
   ```bash
   git clone https://github.com/yourusername/Capstone‑ECommerce‑Project.git
   cd Capstone‑ECommerce‑Project
