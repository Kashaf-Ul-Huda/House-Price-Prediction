# House Price Prediction

## Objective
Predict median house prices based on property features. The project highlights regression modeling, feature engineering, preprocessing, and Gradio deployment.

## Dataset
- **Source:** California Housing Dataset (Handson-ML2)
  - URL: [https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv](https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv)
- **Description:** Contains 8 numeric features, 1 categorical (`ocean_proximity`), and target variable `median_house_value`.

## Methodology
1. **Load Dataset**
   - Read CSV using pandas.
   - Checked `head()`, `info()`, `isnull()`.

2. **Data Preprocessing**
   - Filled missing values in `total_bedrooms` with median.
   - One-hot encoded `ocean_proximity`.
   - Scaled features if needed.

3. **Train-Test Split**
   - 80% training, 20% testing.

4. **Modeling**
   - Linear Regression
   - Gradient Boosting Regressor (preferred for better accuracy)
   - Trained on numeric and encoded features.

5. **Evaluation**
   - Metrics: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE)
   - Visualization: Predicted vs Actual prices scatter plot

6. **Gradio Deployment**
   - Inputs: Numeric property features + one-hot encoded ocean proximity features
   - Output: Predicted median house value
   - Interactive interface allows testing any property combination.

## Results
- Gradient Boosting performed better than Linear Regression.
- MAE and RMSE values were within acceptable ranges.
- Gradio interface provides easy interactive prediction.

## References
- Dataset: California Housing Dataset
- Python Libraries: pandas, scikit-learn, numpy, gradio
