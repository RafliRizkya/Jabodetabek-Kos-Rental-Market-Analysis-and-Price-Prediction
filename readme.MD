# Jabodetabek Kos Rental Market Analysis and Price Prediction

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Scikit--learn%20%7C%20Statsmodels-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

## Project Overview

This project presents a comprehensive data-driven analysis of the "kos" (boarding house) rental market across the Jabodetabek (Greater Jakarta) metropolitan area. The goal is to uncover key market dynamics, identify price-driving factors, and build a reliable predictive model to estimate rental prices. The analysis moves from high-level exploratory data analysis (EDA) to a statistically robust regression model, providing a full-spectrum view of the rental landscape.

---

## Key Analyses

This repository covers four main analytical pillars:

* **Price Benchmarking:** A comparative analysis of kos rental prices across all major regions in Jabodetabek, identifying the most and least expensive areas.
* **Location & Density Trends:** Geospatial and density analysis to spot which regions and sub-districts have higher concentrations of kos listings and how density correlates with price.
* **Amenities Analysis:** A deep dive into which facilities (e.g., WiFi, AC, private bathrooms) are most common and quantifying their statistical impact on rental prices.
* **Predictive Modeling:** Development and refinement of a machine learning model to accurately estimate kos rental prices based on location, size, and amenities.

---

## Project Workflow

1.  **Data Collection & Cleaning:** Data was sourced and underwent a rigorous cleaning process to handle missing values, duplicates, and inconsistencies.
2.  **Exploratory Data Analysis (EDA):** Visualizations were created using Plotly, Seaborn, and Matplotlib to explore distributions, identify trends, and formulate hypotheses.
3.  **Feature Engineering & Preprocessing:** Features were selected and prepared for modeling. This included one-hot encoding for categorical variables and standardization for numerical variables.
4.  **Modeling & Iteration:** An initial Linear Regression model revealed issues of heteroscedasticity. The key improvement was applying a **logarithmic transformation** to the price variable, leading to a more stable and statistically valid OLS (Ordinary Least Squares) model.
5.  **Evaluation & Interpretation:** The final model was evaluated on a hold-out test set, and its coefficients were interpreted to provide actionable insights in real Rupiah terms.

---

## Key Insights

* **Geographic Price Drivers:** Location is the most significant price determinant. **Jakarta Selatan** and **Jakarta Pusat** command the highest rental premiums in the Jabodetabek area.
* **High-Impact Amenities:** The presence of an **Air Conditioner (AC)** and a **Water Heater (Air Panas)** were found to be among the most significant facility-based price drivers.
* **Model Performance:** The final OLS model successfully explains **78.1%** of the price variance on the training data (`R-squared = 0.781`).
* **Predictive Accuracy:** On unseen test data, the model achieves a strong **R-squared of 0.75** and a **Mean Absolute Error (MAE) of approximately Rp 252,000**, making it a reliable tool for price estimation.

---

## Technologies Used

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn, Plotly
* **Machine Learning & Statistics:** Scikit-learn, Statsmodels