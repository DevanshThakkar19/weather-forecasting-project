# Weather Trend Forecasting

PM Accelerator-style assessment: exploratory analysis, forecasting, and anomaly detection on a global weather repository dataset.

## Stack

Python · pandas · scikit-learn · statsmodels · Prophet · XGBoost · matplotlib/seaborn

## Data

`data/cleaned_weather_data.csv` is included (cleaned analysis-ready table). The main notebook starts from this file.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/weather_forecasting_analysis.ipynb
```

Plots are written under `reports/`.

## Contents

```
├── data/cleaned_weather_data.csv
├── notebooks/weather_forecasting_analysis.ipynb
├── reports/                  # generated figures
├── requirements.txt
└── README.md
```

## Author

**Devansh Thakkar** — MS Artificial Intelligence, Northeastern University  
[github.com/DevanshThakkar19](https://github.com/DevanshThakkar19)
