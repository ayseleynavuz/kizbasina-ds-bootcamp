# House Prices - Advanced Regression Techniques

This project aims to predict house prices using various regression techniques based on multiple features provided in the dataset. The project follows a complete machine learning pipeline, from data preprocessing and EDA to model training, evaluation, and tuning.

## 📁 Project Structure

- `data/` – Contains the training and test datasets.
- `notebooks/` – Includes the Jupyter notebook with the complete analysis.
- `README.md` – Project overview and instructions.

---

## 📊 Dataset

The dataset used is from the **Kaggle House Prices - Advanced Regression Techniques** competition:

- **Train Set:** 1,460 rows × 81 columns  
- **Test Set:** 1,459 rows × 80 columns  
- Target variable: `SalePrice`

[🔗 Dataset on Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

---

## 🔍 Project Goals

- Understand the data and its structure
- Handle missing values
- Feature engineering and encoding
- Train and evaluate multiple regression models
- Tune model hyperparameters
- Interpret model results

---

## 📌 Steps Performed

### 1. Exploratory Data Analysis (EDA)
- Visualized `SalePrice` distribution  
- Analyzed missing values  
- Checked outliers  
- Correlation analysis

### 2. Data Preprocessing
- Dropped columns with more than 20% missing values  
- Imputed numerical columns using mean  
- Imputed categorical columns using a constant placeholder (`"Missing"`)  
- One-hot encoded all categorical variables  
- Aligned train and test datasets  

### 3. Outlier Removal
- Removed extreme outliers in `GrLivArea` vs `SalePrice` to improve model accuracy

### 4. Modeling
- **Baseline models:**  
  - Decision Tree Regressor  
  - Random Forest Regressor

- **Evaluation Metrics:**  
  - RMSE (Root Mean Squared Error)  
  - RMSLE (Root Mean Squared Log Error)  
  - R² Score

- **Hyperparameter Tuning:**  
  - Performed `GridSearchCV` for the Random Forest model  
  - Best parameters: `n_estimators=100`, `max_depth=20`, `max_features='sqrt'`

### 5. Model Performance

| Model               | RMSE      | RMSLE   | R² Score |
|--------------------|-----------|---------|----------|
| Decision Tree       | ~31000    | ~0.19   | ~0.68    |
| Random Forest       | ~24000    | ~0.15   | ~0.82    |
| Random Forest (Tuned) | **20292.68** | **0.1337** | **0.8705** |

### 6. Feature Importance

![Feature Importance](feature_importance.png)

---

## 🛠 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 📌 Future Improvements

- Try other models: XGBoost, Lasso, Ridge  
- Perform feature selection  
- Fine-tune feature engineering steps  
- Cross-validation on full dataset

---

## 💡 Learnings

- Hands-on experience with a full ML pipeline  
- Data cleaning and imputation strategies  
- Model tuning using grid search  
- Evaluation using multiple metrics

---

## 🙋‍♀️ Author

- Name: *ALEYNA YAVUZ*  
- LinkedIn: https://www.linkedin.com/in/ayseleynavuz/
- Kaggle: https://www.kaggle.com/aleynayavuz

---

## 🏁 License

This project is for educational purposes only. Based on the [Kaggle House Prices Challenge](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques).
