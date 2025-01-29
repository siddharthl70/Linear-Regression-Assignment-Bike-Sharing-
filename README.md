# Bike Demand Prediction Using Multiple Linear Regression

## Overview
This project aims to predict the demand for shared bikes using a multiple linear regression model. The dataset contains daily records of bike rentals and various influencing factors such as weather conditions, seasonality, and other environmental factors. By analyzing these factors, the model provides insights that can help optimize bike-sharing services.

## Dataset
The dataset used for this analysis is `day.csv`, which includes:

- **cnt**: Total bike rentals (Target Variable)
- **season**: Season of the year (`spring`, `summer`, `fall`, `winter`)
- **yr**: Year (`0` for 2018, `1` for 2019)
- **mnth**: Month of the year (`1` to `12`)
- **holiday**: Whether the day is a holiday (`0`: No, `1`: Yes)
- **weekday**: Day of the week (`0`: Sunday - `6`: Saturday)
- **workingday**: Whether the day is a working day (`0`: No, `1`: Yes)
- **weathersit**: Weather condition (`Clear`, `Mist + Cloudy`, `Light Snow/Rain`, `Heavy Rain`)
- **temp**: Normalized temperature in Celsius
- **hum**: Normalized humidity level
- **windspeed**: Normalized wind speed
- **casual**: Count of casual users
- **registered**: Count of registered users

## Steps Involved
### 1. Data Understanding & Preparation
- Load and inspect the dataset.
- Handle missing values and outliers if any.
- Convert categorical variables into appropriate formats.
- Create dummy variables for categorical data.
- Remove irrelevant features that do not contribute significantly to the prediction.

### 2. Exploratory Data Analysis (EDA)
- Visualize distributions of numerical features using histograms.
- Analyze correlations between features using heatmaps.
- Compare bike demand across different seasons and weather conditions.

### 3. Model Building
- Split the data into training (`80%`) and testing (`20%`) sets.
- Train a multiple linear regression model using `scikit-learn`.
- Select the most significant features by analyzing **p-values** and **Variance Inflation Factor (VIF)**.

### 4. Model Evaluation
- Evaluate performance using the following metrics:
  - **R-squared (R²)**: Measures the proportion of variance explained by the model.
  - **Adjusted R-squared**: Accounts for the number of predictors in the model.
  - **Mean Absolute Error (MAE)**: Measures the average absolute errors.
  - **Mean Squared Error (MSE)**: Computes the average squared difference.
  - **Root Mean Squared Error (RMSE)**: Square root of MSE, giving better interpretability.
- Perform residual analysis to validate linear regression assumptions.

### 5. Residual Analysis
- Plot residual distributions to check normality.
- Check for homoscedasticity by plotting residuals vs. predicted values.
- Use the **Durbin-Watson test** to detect autocorrelation in residuals.

## Installation & Requirements
To run this project, ensure you have the following libraries installed:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib
```

## Running the Project
1. Clone this repository using:
   ```bash
   git clone <repo-url>
   ```
2. Navigate to the project folder:
   ```bash
   cd bike-demand-prediction
   ```
3. Open the Jupyter Notebook `bike_demand_prediction.ipynb`.
4. Run all the cells to train and evaluate the model.

## Results & Insights
- The trained model provides insights into how different features impact bike demand.
- **Key Findings:**
  - Temperature and seasonality significantly impact demand.
  - Holidays and working days show variations in bike usage patterns.
  - Weather conditions such as heavy rain reduce demand significantly.
- The model achieves an **R² score** of ~0.8, indicating a good fit.
- Residual analysis confirms that the linear regression assumptions hold.

## Future Improvements
- Try **polynomial regression** to capture non-linear relationships.
- Include additional external data like **special events** or **traffic patterns**.
- Apply **feature engineering** to create interaction terms.
- Experiment with other machine learning models like **decision trees** or **random forests**.

## Author
**Siddharth Laskar**
- LinkedIn: (https://www.linkedin.com/in/siddharthlaskar/)
- GitHub: (https://github.com/siddharthl70/Linear-Regression-Assignment-Bike-Sharing-)

## License
This project is open-source and available under the **MIT License**. Feel free to modify and use it as needed.

