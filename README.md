# Gold Price Prediction using Prophet

A focused Jupyter notebook project demonstrating how to forecast historical gold prices using Prophet. This repository contains a single notebook:

- `Gold Price Prediction using Prophet.ipynb`

This is not a web application — it's an interactive notebook for exploration, training, evaluation, and short-term forecasting.

## Contents
- `Gold Price Prediction using Prophet.ipynb` — Jupyter notebook that:
  - Downloads/loads the gold price dataset (via KaggleHub or a local CSV)
  - Preprocesses the data for Prophet (`ds`, `y`)
  - Splits into train/test (90%/10%)
  - Trains a Prophet model and evaluates using RMSE
  - Visualizes forecasts and components (trend, seasonality)
  - Generates future forecasts and exports results to CSV

## Dataset
The notebook uses a historical gold price dataset (columns include `Date` and `GLD`). The notebook can download the dataset from Kaggle using KaggleHub, or you can provide a local CSV file.

Expected important columns:
- `Date` — date of observation
- `GLD` — gold price (target)

## Requirements
Install dependencies in a Python environment. Example (pip):

```bash
pip install --upgrade pip
pip install pandas matplotlib plotly prophet statsmodels kagglehub jupyterlab
```

Notes:
- Prophet may require a specific backend (cmdstanpy or pystan) depending on your platform; if pip install fails, consider the conda-forge build:

```bash
conda install -c conda-forge prophet
```

## Running the notebook
1. Clone the repository or download the notebook file.
2. Ensure dependencies are installed.
3. If the notebook downloads the dataset from Kaggle:
   - Provide Kaggle credentials (`kaggle.json`) or configure KaggleHub as required by that library.
   - Or place the dataset CSV into a `data/` folder and update the notebook path accordingly.
4. Launch Jupyter:

```bash
jupyter lab
# or
jupyter notebook
```

5. Open `Gold Price Prediction using Prophet.ipynb` and run the cells in order.

Tip: You can also upload the notebook to Colab (some Kaggle download cells may need adaptation or manual dataset upload).

## Notebook structure (high level)
1. Data download & loading
2. Preprocessing for Prophet (`ds`, `y`)
3. Exploratory visualization (trend & seasonality)
4. Train/test split (90% / 10%)
5. Train Prophet model
6. Forecast on test set + compute RMSE
7. Visualize forecasts & components
8. Retrain on full data and produce future forecasts
9. Export predictions to CSV

## Evaluation
- The notebook reports Root Mean Squared Error (RMSE) on the test partition. Lower RMSE indicates tighter fit to actual prices.

## Suggested next steps / improvements
- Hyperparameter tuning for Prophet (changepoints, seasonality modes)
- Time series cross-validation (Prophet's cross-validation utilities)
- Compare with ARIMA, SARIMAX, or LSTM models
- Add external regressors (USD index, oil price, interest rates)
- Create a small Streamlit app or dashboard for interactive forecasting

## License & Credits
- Credit: Prophet (originally developed by Meta / Facebook)
- Data source: Kaggle (refer to the dataset page for licensing)

## Contact
If you want this README updated, or need a requirements.txt / environment.yml added, tell me which files to add or which branch to use and I will update the repo.
