# Jabodetabek Kos Rental Market Analysis and Price Prediction

## Project Overview

This project presents a comprehensive data-driven analysis of the "kos" (boarding house) rental market across the Jabodetabek (Greater Jakarta) metropolitan area. The goal is to uncover key market dynamics, identify price-driving factors, and build a reliable predictive model to estimate rental prices. The analysis moves from high-level exploratory data analysis (EDA) to a statistically robust regression model, providing a full-spectrum view of the rental landscape.

---

## Project Workflow

1.  **Data Collection & Cleaning:** Data was sourced and underwent a rigorous cleaning process to handle missing values, duplicates, and inconsistencies.
2.  **Exploratory Data Analysis (EDA):** Visualizations were created using Plotly, Seaborn, and Matplotlib to explore distributions, identify trends, and formulate hypotheses.
3.  **Feature Engineering & Preprocessing:** Features were selected and prepared for modeling. This included one-hot encoding for categorical variables and standardization for numerical variables.
4.  **Modeling & Iteration:** An initial Linear Regression model revealed issues of heteroscedasticity. The key improvement was applying a **logarithmic transformation** to the price variable, leading to a more stable and statistically valid OLS (Ordinary Least Squares) model.
5.  **Evaluation & Interpretation:** The final model was evaluated on a hold-out test set, and its coefficients were interpreted to provide actionable insights in real Rupiah terms.

---

## Exploratory Data Analysis (EDA)

### Price Benchmarking & Location Trends
Analysis of price distribution across Jabodetabek reveals significant disparities. Central Jakarta and South Jakarta emerge as the regions with the highest median and average rental prices.

![Median Price by Region](Perbandingan%20Harga%20Median%20di%20Wilayah%20Jabodetabek.png)
![Average Price by Region](Perbandingan%20Harga%20Rata-Rata%20di%20Wilayah%20Jabodetabek.png)

Furthermore, there is a clear correlation between the number of available listings in a region and the median price, indicating distinct market tiers.

![Median Price vs Kos Count](Perbandingan%20Harga%20Median%20dan%20Jumlah%20Kos%20per%20Wilayah.png)

### Amenities Analysis
The number of amenities offered is a strong indicator of price. As the variety of facilities increases, so does the median rental price, confirming their role as a key value driver.

![Median Price vs Facility Count](Perbandingan%20Harga%20Median%20dan%20Jumlah%20Fasilitas.png)

---

## Model Evaluation

The final OLS model demonstrates strong predictive power and statistical validity. On unseen test data, the model achieves an **R-squared of 0.75** and a **Mean Absolute Error (MAE) of approximately Rp 252,000**.

### Actual vs. Predicted Prices
The scatter plot below shows a tight clustering of predicted values around the actual values, indicating high accuracy for the majority of the data.

![Actual vs Predicted](Actual%20vs%20Predicted%20Rental%20Price.png)

### Residual Analysis
The residual plots confirm that the model is healthy and unbiased. The "Fitted Values vs Residuals" plot shows a random scatter (**homoscedasticity**), a significant improvement achieved through log transformation. The "Residual Distribution" plot is normally distributed and centered at zero, indicating no systematic error.

![Residual Plots](Fitted%20&%20Residual%20Plot.png)

---

## Technologies Used

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn, Plotly
* **Machine Learning & Statistics:** Scikit-learn, Statsmodels