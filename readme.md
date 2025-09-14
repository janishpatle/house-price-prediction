# 🏡 California Housing Price Prediction

This project predicts **median house values** in California districts based on features such as income, number of rooms, population, and location using machine learning regression techniques.  
It is implemented in Python using **scikit-learn** and trained on the **California Housing Prices dataset**.

---

## 📊 Dataset
- **Source**: `/kaggle/input/california-housing-prices/housing.csv`  
- **Size**: ~20,640 samples, 10 features  
- **Features**:  
  - `longitude` – geographic coordinate  
  - `latitude` – geographic coordinate  
  - `housing_median_age` – median age of houses  
  - `total_rooms` – total number of rooms per district  
  - `total_bedrooms` – total number of bedrooms per district  
  - `population` – population of district  
  - `households` – number of households  
  - `median_income` – median income of district  
  - `ocean_proximity` – categorical feature  
- **Target Variable**: `median_house_value`  

---

## 🔧 Workflow
1. **Data Preprocessing**
   - Handle missing values with `SimpleImputer`  
   - Encode categorical variable (`ocean_proximity`) with `OneHotEncoder`  
   - Scale numerical features with `StandardScaler`  

2. **Feature Engineering**
   - Created new features:  
     - `rooms_per_household`  
     - `bedrooms_ratio`  
     - `population_per_household`  
   - Log-transform skewed features  

3. **Model Training**
   - Linear Regression  
   - Decision Tree Regressor  
   - Random Forest Regressor  
   - Hyperparameter tuning with `GridSearchCV`  

4. **Evaluation**
   - Metrics: RMSE, R² score  
   - Cross-validation used for robust evaluation  

---

## 📈 Results
- **Best Model**: Random Forest Regressor (after GridSearchCV tuning)  
- **RMSE**: ~50,000 (on test set)  
- **R² Score**: ~0.8  

*(Values may vary depending on preprocessing and hyperparameters.)*  

---

## ▶️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/california-housing-prediction.git
cd california-housing-prediction
