Real Estate Housing Price Prediction
California Housing Dataset — OLS, Ridge & Lasso Regression
Project Overview
This project predicts median house values using the California Housing dataset. It compares three regression models: Ordinary Least Squares (OLS) Linear Regression, Ridge Regression, and Lasso Regression.

The project uses Python and Scikit-Learn to preprocess the data, create interaction features, tune regularization parameters, evaluate model performance, and visualize prediction errors.
Project Objectives
- Load and explore the California Housing dataset.
- Check and handle missing values using median imputation.
- Create pairwise interaction features.
- Split the data into 80% training data and 20% testing data.
- Standardize features using StandardScaler.
- Train OLS, Ridge, and Lasso regression models.
- Tune Ridge and Lasso alpha values using GridSearchCV.
- Compare models using RMSE, MAE, and R².
- Visualize feature correlations, actual versus predicted values, and residual errors.
Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
Dataset
The project uses Scikit-Learn's California Housing dataset. It contains housing-related features such as median income, house age, average rooms, population, and geographic coordinates.

The target variable is median house value. In this dataset, target values are expressed in units of $100,000.

The dataset may be downloaded automatically by Scikit-Learn when the program is run for the first time, so an internet connection may be required.
Models
1. OLS Linear Regression — baseline linear regression model.
2. Ridge Regression (L2) — adds L2 regularization to help control large coefficients and multicollinearity.
3. Lasso Regression (L1) — adds L1 regularization and can reduce some coefficients to zero.
Ridge and Lasso parameters are selected using five-fold cross-validation with GridSearchCV.
Evaluation Metrics
- RMSE (Root Mean Squared Error): Measures the typical prediction error, penalizing larger errors more strongly.
- MAE (Mean Absolute Error): Measures the average absolute difference between actual and predicted values.
- R² (Coefficient of Determination): Measures how much variation in the target is explained by the model.
Lower RMSE and MAE are better. A higher R² is generally better.
Generated Outputs
When the code runs successfully, it creates a california_housing_output folder containing:
- 01_correlation_heatmap.png — feature correlation heatmap.
- 02_model_metrics_comparison.png — RMSE, MAE, and R² comparison.
- 03_actual_vs_predicted.png — actual and predicted values for each model.
- 04_residual_distributions.png — residual error distributions.
- 05_residuals_vs_predicted.png — residuals plotted against predicted values.
- model_metrics.csv — evaluation metrics for all models.
Installation
Install the required Python packages:
pip install numpy pandas matplotlib seaborn scikit-learn
How to Run
Download or clone this repository, open a terminal in the project folder, and run:
python california_housing_regression.py
Alternatively, open California_Housing_Regression.ipynb in Jupyter Notebook or Google Colab and run the notebook cells.
Project Files
- california_housing_regression.py — complete Python script.
- California_Housing_Regression.ipynb — Jupyter Notebook version.
- README.md — project documentation.
Notes
- The train/test split uses a fixed random seed so the results are reproducible.
- Preprocessing is performed in a Scikit-Learn pipeline to help avoid data leakage.
- Results can vary if the dataset, random seed, feature engineering, or model settings are changed.
Author
M Jawad Mazhar
