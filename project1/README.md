# California Housing Price Prediction

This project uses a multiple linear regression model to estimate median house
values in California from housing, population, income, and geographic data. It
is a practice project for exploring a basic machine-learning workflow with
Python and scikit-learn.

## Project files

- `house_price_prediction.ipynb` — loads the data, explores it, trains the
  regression model, and evaluates predictions.
- `california_housing_train.csv` — the dataset used by the notebook.

## Dataset

The CSV contains these columns:

| Column | Description |
| --- | --- |
| `longitude`, `latitude` | Geographic coordinates |
| `housing_median_age` | Median age of housing in the area |
| `total_rooms`, `total_bedrooms` | Total rooms and bedrooms |
| `population` | Population |
| `households` | Number of households |
| `median_income` | Median income |
| `median_house_value` | Target value the model predicts |

The model uses all columns except `median_house_value` as input features and
predicts `median_house_value`.

## Requirements

Install Python, then install the libraries used by the notebook:

```powershell
python -m pip install pandas scikit-learn matplotlib jupyter
```

## Run the notebook

In PowerShell, move to the project folder and start Jupyter:

```powershell
cd "D:\pip\refernce\ml\linear regression\project1"
jupyter notebook
```

Open `house_price_prediction.ipynb` and run the cells from top to bottom. The
notebook reads `california_housing_train.csv` using a relative path, so start
Jupyter from this project folder. In VS Code, open this folder, select a Python
kernel with the required packages installed, and run the notebook cells in
order.

## Modeling workflow

The notebook:

1. Loads the CSV with pandas and checks for missing values, duplicate rows,
   and feature correlations.
2. Selects the eight housing, income, and location columns as model inputs.
3. Splits the data into training and test sets, using an 80/20 split and
   `random_state=42`.
4. Fits a `LinearRegression` model on the training data.
5. Predicts values for both sets and reports the R² score for each.

This is an educational baseline model. Its predictions and evaluation scores
depend on the supplied data and do not guarantee the value of an individual
home.
