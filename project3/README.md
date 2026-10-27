# Energy Efficiency Prediction

This project uses a multiple linear regression model to predict building
heating load from building characteristics in the ENB2012 energy efficiency
dataset. It is a practice exercise in data exploration, train/test splitting,
regression, and model evaluation.

## Project files

- `energy_effciency_prediction.ipynb` — explores the dataset, trains the
  regression model, evaluates predictions, and plots feature comparisons.
- `ENB2012_data.xlsx` — the Excel dataset used by the notebook.

## Dataset and prediction target

The notebook assigns descriptive names to the dataset's ten columns: eight
building features (including relative compactness, surface and wall area,
orientation, and glazing measurements), plus `Heating Load` and `Cooling Load`.
It uses the eight building features to predict `Heating Load`. `Cooling Load`
is not modeled in this notebook.

## Requirements

Install Python and the libraries used by the notebook:

```powershell
python -m pip install pandas numpy scikit-learn matplotlib seaborn openpyxl jupyter
```

`openpyxl` enables pandas to read the Excel dataset.

## Run the notebook

In PowerShell, move to the project folder and start Jupyter:

```powershell
cd "D:\pip\refernce\ml\linear regression\project3"
jupyter notebook
```

Open `energy_effciency_prediction.ipynb` and run the cells in order. The
notebook loads `ENB2012_data.xlsx` using a relative path, so start Jupyter from
this project folder. In VS Code, open this folder, select a Python kernel with
the required packages installed, and run the notebook cells in order.

## Modeling workflow

The notebook:

1. Loads the Excel dataset with pandas, assigns descriptive column names, and
   inspects the data, missing values, duplicates, and correlations.
2. Uses the eight building characteristics as input features and `Heating Load`
   as the prediction target.
3. Splits the rows into training and test sets with an 80/20 split and
   `random_state=42`.
4. Fits a scikit-learn `LinearRegression` model on the training data.
5. Reports training MSE, RMSE, MAE, and R², then reports test R² and plots
   actual and predicted heating loads against each feature.

## Note

The final plotting cell refers to `sns` but the notebook does not import
Seaborn. To run that cell, add `import seaborn as sns` to the notebook's imports;
otherwise, the preceding modeling and evaluation cells can be run without it.

This is an educational baseline model. Its results depend on the supplied data
and should not be treated as guaranteed real-world predictions.
