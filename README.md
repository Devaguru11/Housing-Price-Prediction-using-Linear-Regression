# 🏠 Housing Price Prediction using Linear Regression

This project predicts the sale prices of homes using data from the [Kaggle House Prices: Advanced Regression Techniques competition](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques).  
We implemented a simple and interpretable **Linear Regression** model with proper data preprocessing, feature engineering, and pipeline construction.

---

## 📌 Problem Statement

Predict the final selling price of residential homes based on features like area, location, construction year, and more.  
The goal is to minimize prediction error on unseen test data.

---

## 🔧 Technologies Used

- **Python**
- **pandas** – data handling  
- **numpy** – numerical operations  
- **scikit-learn** – machine learning (Linear Regression, pipelines, metrics)  
- **matplotlib, seaborn** – visualizations

---

## 📁 Dataset

- `train.csv` – includes 81 features and `SalePrice` as target
- `test.csv` – includes the same features, but without `SalePrice`
> Download both from Kaggle:  
> 🔗 [Kaggle Competition Link](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

---

## 🧪 Workflow Summary

1. Load and combine train/test datasets  
2. Handle missing values using domain knowledge:
   - Fill `"None"` for missing categorical features like `GarageType`, `Basement`
   - Fill **mode** for remaining categorical columns
   - Fill **median** for numeric columns
3. Convert `MSSubClass` to categorical  
4. Apply **one-hot encoding**  
5. **Log transform** the target (`SalePrice`) to reduce skewness  
6. Use `Pipeline` with:
   - `StandardScaler()` to normalize features  
   - `LinearRegression()` to train the model
7. Split data for training and validation
8. Evaluate with **RMSE**
9. Generate `submission.csv` for Kaggle

---

## 📊 Output

- **Validation RMSE**: ~0.13 (log scale)  
- **Submission file**: `submission.csv`  
- **Kaggle leaderboard**: You can upload and view your public score

---

## 📈 Visualizations

- SalePrice distribution (before and after log transform)
- Predicted vs Actual SalePrice (scatter plot)

---

## ✅ How to Run

1. Clone the repo:
```bash
git clone https://github.com/your-username/housing-price-prediction.git
cd housing-price-prediction
