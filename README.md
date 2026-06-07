# Used Car Price Prediction

**DSC 148 – Intro to Data Mining | Course Project**  
University of California, San Diego

**Authors:** Liuxuhong Zhao · Kangxin Peng

---

## Overview

This project predicts used car listing prices on Craigslist using machine learning regression models. We compare Linear Regression, Random Forest, and XGBoost on a dataset of 347,641 cleaned listings, and conduct a feature ablation study to identify the most influential predictors.

**Best model:** XGBoost — MAE $3,446 | R² 0.834

---

## Repository Structure

```
├── notebook.ipynb
├── demo.html
├── requirements.txt
├── README.md
└── DSC148_Project_Report_v3.docx
```

---

## Dataset

[Craigslist Used Cars Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) by Austin Reese (Kaggle)

- Raw: 426,880 listings, 26 columns
- After cleaning: 347,641 listings, 14 features

Download `vehicles.csv` from Kaggle and place it in the project root before running the notebook.

---

## Results

| Model | MAE ($) | R² | Train Time (s) |
|---|---|---|---|
| Linear Regression | 6,395.67 | 0.5913 | 0.07 |
| Random Forest | 3,342.62 | 0.8358 | 8.19 |
| **XGBoost** | **3,446.23** | **0.8337** | **1.51** |

### Top Features (Ablation Study)

| Feature | MAE without | Δ MAE |
|---|---|---|
| car_age | $6,338 | +$2,892 |
| odometer | $5,114 | +$1,668 |
| condition | $4,918 | +$1,472 |
| vehicle type | $4,838 | +$1,392 |
| cylinders | $4,793 | +$1,347 |

---

## Setup

```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

---

## Requirements

See `requirements.txt`
## Demo

Live demo: https://liuxuhongds.github.io/dsc148-used-car-price-prediction/demo.html

No installation required — runs in any browser.