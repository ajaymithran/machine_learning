# Car Fuel Efficiency Prediction

+-------------------------------+
| CAR FUEL EFFICIENCY PREDICTION |
+-------------------------------+

This project trains a linear regression model to predict fuel efficiency in kilometers per liter using car feature data.

## Project overview

- Notebook: `car_fuel_efficency_prediction.ipynb`
- Dataset: `car_fuel_efficiency_practice.csv`
- Task: estimate `FuelEfficiencyKmPerL` from the available car attributes

## Features used

The notebook builds a model using the dataset columns except for the target column:

- Engine size
- Horsepower
- Weight
- Transmission
- Fuel type
- Other numeric vehicle features in the CSV

## Requirements

Install the project dependencies with:

```powershell
python -m pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

## Run the notebook

Open the notebook in VS Code or Jupyter Notebook and run the cells from top to bottom.

```powershell
cd "D:\linear regression\project2"
jupyter notebook
```

## Model workflow

1. Load the dataset with pandas.
2. Split the data into training and testing sets.
3. Train a `LinearRegression` model.
4. Evaluate the model using MAE, MSE, RMSE, and R².
5. Compare predicted and actual fuel efficiency values.

## Model performance

The trained model performed well on both training and test data:

- Training R²: about 0.969
- Test R²: about 0.944
- Training RMSE: about 0.513
- Test RMSE: about 0.497

These results show the model captures the main pattern in the dataset and generalizes reasonably well.

## Notes

This notebook is intended for learning and practice in machine learning, especially linear regression and model evaluation.
