# Data_Science_Final

# Airbnb Price Prediction (Chicago)

## Project Overview

This project builds a machine learning model to predict Airbnb listing prices in Chicago based on property characteristics, location, and listing features.

The final model uses Gradient Boosting and achieves strong performance by capturing nonlinear relationships in spatial and listing data.

---

## Dataset

Source: Inside Airbnb (Chicago dataset)

Features used:

* Bedrooms
* Bathrooms
* Review score rating
* Latitude and longitude
* Room type (one-hot encoded)
* Accommodates
* Amenities count
* Availability (days per year)

Target:

* Price (USD per night)

---

## Methodology

### Data Cleaning

* Removed invalid and extreme values
* Converted price from string to numeric
* Fixed misaligned columns
* Filled missing values using median

### Feature Engineering

* One-hot encoding for room type
* Created amenities_count feature
* Included geographic coordinates
* Log transformation applied to price

### Models

* Random Forest (baseline)
* Gradient Boosting (final model)

### Evaluation Metrics

* R2 Score
* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)

---

## Results

| Model             | R2     | MAE   | RMSE  |
| ----------------- | ------ | ----- | ----- |
| Random Forest     | 0.6636 | 42.33 | 63.97 |
| Gradient Boosting | 0.6708 | 41.99 | 63.28 |

Gradient Boosting performed best and was selected as the final model.

---

## How to Run

### Option 1: Run Notebook

1. Open notebook.ipynb in Google Colab
2. Upload dataset (airbnb.csv)
3. Run all cells

### Option 2: Run Streamlit App

Install dependencies:

```
pip install -r requirements.txt
```

Run app:

```
streamlit run app.py
```

---

## Files

* notebook.ipynb → full pipeline
* app.py → Streamlit web app
* airbnb_rf_model.joblib → trained model
* requirements.txt → dependencies

---

## Notes

* If model file is missing, re-run training cells in notebook
* Dataset can be downloaded from Inside Airbnb: http://insideairbnb.com/get-the-data/

---
