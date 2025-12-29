# City-Based House Rent Prediction: Web Scraping and Deep Learning Regression Model

## Project Overview
This project aims to **predict rental prices** in a specific city in Turkey. The workflow includes:

1. **Data Collection via Web Scraping:**  
   Rental listings are collected from popular real estate websites such as Zingat, Hepsiemlak, and Emlakjet. The dataset includes features like:
   - Neighborhood (Semt)  
   - Number of rooms  
   - Property size  
   - Floor information  
   - Other relevant property attributes  

2. **Data Cleaning and Preprocessing:**  
   - Missing values are handled and outliers are removed.  
   - Features are encoded numerically for machine learning compatibility.  
   - Feature engineering is applied to enhance model performance.

3. **Modeling:**  
   - Traditional machine learning models: Linear Regression, Random Forest, Gradient Boosting, Extra Trees, KNN, XGB, etc.  
   - Deep Learning model using TensorFlow/Keras.

4. **Evaluation Metrics:**  
   - **R² (Coefficient of Determination)**  
   - **RMSE (Root Mean Squared Error)**  
   - **MAE (Mean Absolute Error)**

## Model Performance Comparison

| Model                 | R² Score | RMSE            | MAE           |
|-----------------------|----------|----------------|---------------|
| Extra Tree Regressor   | 0.866    | 1.0567e+07     | 3.4807e+06    |
| KNeighborsRegressor    | 0.805    | 1.2732e+07     | 6.6180e+06    |
| Gradient Boosting      | 0.800    | 1.2913e+07     | 3.7278e+06    |
| Decision Tree          | 0.792    | 1.3149e+07     | 4.2733e+06    |
| XGBRegressor           | 0.767    | 1.3916e+07     | 3.7953e+06    |
| Linear Regression      | 0.700    | 1.5811e+07     | 5.2174e+06    |
| Lasso                  | 0.700    | 1.5811e+07     | 5.2174e+06    |
| Ridge                  | 0.640    | 1.7301e+07     | 5.3541e+06    |
| SGD                    | 0.560    | 1.9138e+07     | 5.9482e+06    |
| AdaBoost               | 0.412    | 2.2119e+07     | 5.4536e+06    |
| ElasticNet             | 0.065    | 2.7891e+07     | 6.9526e+06    |
| SVR                    | -0.041   | 2.9434e+07     | 7.2997e+06    |
| MLP Regressor          | -0.155   | 3.0998e+07     | 1.1341e+07    |

## Key Insights
- **Extra Tree Regressor** achieved the highest performance (R² ≈ 0.85), making it the most effective model for rent prediction.  
- Gradient Boosting and KNN models also performed well, while linear models (Linear, Ridge, Lasso) had moderate performance.  
- SVR and MLP models failed to capture the underlying patterns, resulting in negative R² scores.  
- The deep learning (Keras) model achieved R² ≈ 0.75, outperforming simple linear models but underperforming compared to tree-based ensemble methods.  

## Conclusion
Tree-based models such as **Extra Trees** and **Gradient Boosting** are highly effective for predicting rental prices due to the **non-linear relationships** in property features. While deep learning models can capture some complexity, traditional ensemble methods remain superior for this type of structured tabular data.
