# Business Forecasting

Repository contains datasets and reusable three‑phase forecasting pipeline that powers three notebook scenarios (`Prophet market`, `Prophet money`, `Prophet pcs`).

## Requirements

- Python 3.10 or newer
- Recommended packages:
  - `pandas`, `numpy`, `statsmodels`, `scikit-learn`, `xgboost`
  - `nbformat`, `jupyter`

Install everything at once (upgrade `pip` first to avoid wheel issues):

```bash
python -m pip install --upgrade pip
python -m pip install pandas numpy statsmodels scikit-learn xgboost nbformat jupyter
```

## Quick Start

1. Launch Jupyter from the project root:
   ```bash
   jupyter notebook
   ```
2. Open один із ноутбуків:
   - `Prophet market.ipynb` (прогноз ринку на рівні `product_group_id`)
   - `Prophet money.ipynb` (прогноз виручки по `category_id`)
   - `Prophet pcs.ipynb` (прогноз щотижневих продажів по `sku_id`)
3. Запусти всі комірки згори донизу. Після завершення у корені з’явиться відповідний CSV:
   - `market_three_phase_forecast.csv`
   - `money_three_phase_forecast.csv`
   - `pcs_three_phase_forecast.csv`

## Оновлення ноутбуків після змін

Якщо вносиш зміни у `three_phase_linear.py` або хочеш відтворити ноутбуки з нуля, виконай:
```bash
python build_notebooks.py
```
Після цього знову відкрий потрібний ноутбук і повтори запуск, щоб отримати оновлений прогноз.
