# Backpack Price Prediction

This project aims to predict backpack prices using various features, including brand, weight capacity, material, and more. The process begins by loading and merging training datasets, followed by cleaning the data (handling missing values, removing duplicates, and dropping unnecessary columns). 

## Data Preprocessing
- **Missing Values**: `Weight Capacity (kg)` is filled with the median, and other missing values are replaced with "Unknown."
- **Data Cleaning**: Removed the `id` column and duplicates.

## Exploratory Data Analysis (EDA)
EDA is performed to understand the data better. Key metrics for the target variable, `Price`, are calculated, such as the mean, median, and price range. The relationship between brands and average price is also analyzed. Visualizations are generated using `matplotlib` and `seaborn`.

## Model Training
Initially, `sklearn`'s Decision Tree Regressor was used, but the results were poor and CPU usage was high. The project then switched to more advanced models: `XGBoost`, `LightGBM`, and `CatBoost`. After tuning hyperparameters with Optuna, the `LightGBM` model showed the best results.

### Model Metrics:
- **RMSE**: 38.87
- **MSE**: 1511.09
- **MAE**: 33.62
- **R²**: 0.0022

## Next Steps
While the model shows improvements, its performance is still suboptimal, with a low R² value. Future work will focus on additional feature engineering, optimization, and experimenting with different models to enhance performance.

## Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/Klaraaorban/Backpack-price-prediction
cd Backpack-price-prediction
pip install -r requirements.txt
