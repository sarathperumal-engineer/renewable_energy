# Renewable Energy Delta Prediction

This project demonstrates a machine learning pipeline for predicting the energy delta (Wh) based on various environmental and operational features using a RandomForestRegressor.

## Table of Contents

- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Prediction](#prediction)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)

## Dataset

The dataset is loaded from a CSV file (`Renewable.csv`). It contains features related to environmental and operational data, with the target variable being `Energy delta[Wh]`.

## Data Preprocessing

1. **Handling Missing Values**:
    - The script counts and drops rows with missing values.

2. **Feature Selection**:
    - Features used for training are all columns except `Time` and `Energy delta[Wh]`.
    - The target variable is `Energy delta[Wh]`.

3. **Data Splitting**:
    - The data is split into training and testing sets with an 80-20 ratio.

4. **Feature Scaling**:
    - Numerical features are scaled using `StandardScaler`.

## Model Training

The `RandomForestRegressor` is used for training the model with the following configuration:
- `n_estimators`: 100
- `random_state`: 42

## Model Evaluation

The model is evaluated using Mean Absolute Error (MAE) on the test dataset.

## Prediction

The model can be used to predict the energy delta for new input data. An example input is provided in the script.

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/renewable-energy-prediction.git
    ```

2. Change to the project directory:
    ```bash
    cd renewable-energy-prediction
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the script:
    ```bash
    python prediction.py
    ```

## Dependencies

- pandas
- scikit-learn
- numpy

You can install these dependencies using:
```bash
pip install pandas scikit-learn numpy
