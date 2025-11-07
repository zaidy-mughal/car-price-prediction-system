## Cars Price Prediction (Regression)

This project builds a simple end‑to‑end workflow for predicting used car prices with classical machine learning. It includes cleaned/encoded datasets and a Jupyter notebook that walks through exploratory analysis, feature preparation, model training, and evaluation using scikit‑learn.

### What’s inside

- `cars_price_prediction_regression.ipynb` — main notebook with EDA, preprocessing, model training, and evaluation
- `car_price.csv` — primary dataset used in the notebook
- `car_price_toy_data.csv` — small sample dataset for quick experimentation
- `car_price_encoded_dataset.csv` — pre‑encoded dataset variant (useful to skip encoding steps)
- `requirements.txt` — pinned dependencies for reproducibility

### Key capabilities

- Load and explore car price data (basic EDA and visualizations)
- Prepare features: handle missing values, encode categoricals, scale/transform as needed
- Train and compare multiple regression models from scikit‑learn
- Report standard regression metrics (e.g., MAE, RMSE, R²) and visualize results

## Getting started

### 1) Environment

Recommended: Python 3.10+ with a virtual environment.

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt
```

Core libraries used include: pandas, numpy, scikit‑learn, matplotlib (see `requirements.txt` for full list and versions).

### 2) Run the notebook

Open the notebook in VS Code or Jupyter and execute cells top‑to‑bottom:

```text
cars_price_prediction_regression.ipynb
```

If your data files are in a different location, adjust the file paths in the first data‑loading cell of the notebook.

## Data notes

- The notebook typically uses `car_price.csv` as the source dataset.
- `car_price_toy_data.csv` is a much smaller subset that runs fast and is helpful for quick iterations.
- `car_price_encoded_dataset.csv` contains pre‑encoded features and can be used to skip encoding in the pipeline.

Common columns in car price datasets include make/model, year, mileage, fuel type, transmission, and other attributes; the notebook will show exactly which fields are present and how they’re processed.

## Results and evaluation

Model performance is reported directly in the notebook using standard regression metrics (e.g., MAE, RMSE, R²). Plots and tables are rendered inline. Use the toy dataset for quick checks and the full dataset for final metrics.

## Repository structure

```
.
├── cars_price_prediction_regression.ipynb  # Main notebook (EDA → features → models → evaluation)
├── car_price.csv                           # Full dataset
├── car_price_toy_data.csv                  # Tiny sample dataset
├── car_price_encoded_dataset.csv           # Pre‑encoded dataset
├── requirements.txt                        # Pinned dependencies
└── README.md                               # You are here
```

## Troubleshooting

- If imports fail, ensure your virtual environment is activated and dependencies are installed with `pip install -r requirements.txt`.
- If you see kernel errors in Jupyter/VS Code, select the Python interpreter from your `.venv`.
- Some plots may require a UI backend; VS Code’s notebook UI renders them inline by default.

## Next steps

- Add a lightweight Python script to train/evaluate from the command line (mirroring the notebook steps)
- Persist the best model (e.g., with `joblib`) and provide a minimal inference example
- Parameterize preprocessing/model choices for quick experimentation

—

If you have questions or want to extend the project (new models, features, or deployment), feel free to open an issue or start a discussion.