# House Price Prediction

## Project Overview
This project predicts house prices based on various features such as the number of bedrooms, proximity to the ocean, and more. Different regression models are evaluated and optimized using Grid Search to achieve the best prediction accuracy.

## Key Features
- **Data Preprocessing**: Missing values in the `total_bedrooms` feature are filled with the most frequent value (mode). The `ocean_proximity` feature is encoded into numerical values.
- **Model Selection**: Several regression models are trained, including Linear Regression, Ridge, Lasso, Random Forest, Gradient Boosting, KNeighbors, and Decision Tree.
- **Grid Search**: Used to optimize hyperparameters for each model by searching through predefined parameter grids. This ensures the best-performing model is selected.
- **Model Evaluation**: Each model's performance is evaluated using Mean Squared Error (MSE) and R-squared (R²) metrics.

## How it Works
1. **Data Preprocessing**: Missing values are handled, and categorical data is encoded.
2. **Model Training**: Multiple regression models are trained using Grid Search for hyperparameter tuning.
3. **Model Evaluation**: The best model is selected based on R² and MSE scores.

## Results
The best hyperparameters for each model are identified, and their performance is displayed using R² and MSE. This approach ensures that the model performs optimally.
