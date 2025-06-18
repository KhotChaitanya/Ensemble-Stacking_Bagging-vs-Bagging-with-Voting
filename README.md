# Bagging vs Bagging + Voting (Random Forest Ensemble) | mtcars Dataset

## Objective

Compare the performance of:

- **Bagging with Random Forest**: A classic ensemble learning method that reduces variance.
- **Bagging + Voting (Random Forest Trio)**: Combines multiple Random Forest models via a voting mechanism to potentially boost prediction accuracy.

All experiments are performed on the **mtcars dataset**, with the target variable being `mpg` (miles per gallon). The primary question: _Does voting among Random Forest models improve regression performance over standard bagging?_

---

## Dataset Overview

- Source: `mtcars.csv`
- Target: `mpg`
- Features: Cylinders, displacement, horsepower, weight, transmission type, etc.

---

## Model Pipeline

1. **Data Preprocessing**
   - Train-test split (80/20)
   - Standard scaling of features

2. **Models Built**
   - `BaggingRegressor` with a base `RandomForestRegressor`
   - `VotingRegressor` combining 3 Random Forest models with different seeds

3. **Evaluation Metrics**
   - R² Score
   - RMSE (Root Mean Squared Error)

---

## Visualizations Included

| Visualization | Description |
|---------------|-------------|
| **Actual vs Predicted Line Plot** | Line graph comparing true vs predicted MPG values |
| **Numeric Performance** | R² and RMSE values for each model |
| **Pairplot** | To explore relationships |

**1. Actual vs Predicted Line Plot:**

![5_1](https://github.com/user-attachments/assets/2806eb80-1c8a-4f0f-87a2-fa48471cfcb7)


**2. Numeric Performance:**

![5_2](https://github.com/user-attachments/assets/d3599f82-425b-4d46-988a-ba5da9eb6e95)

![5_4](https://github.com/user-attachments/assets/b4bea977-e7bc-42f3-92db-93ce87a94232)


**3. Pairplot:**

![5_3](https://github.com/user-attachments/assets/03af493c-4a40-4b16-bdbe-ddd47a04fe1d)

---

## Results

| Model                  | R² Score | RMSE  |
|------------------------|----------|-------|
| Bagging (RF)           | ~ 0.91   | ~ 1.75|
| Voting (3x RF Models)  | ~ 0.93   | ~ 1.55|

> **Observation:** Voting RF gave a slightly better R² and lower RMSE, suggesting improvement through ensemble diversity.

---
