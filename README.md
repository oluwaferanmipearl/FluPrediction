# FluPrediction

Project Overview: 

Influenza remains one of the most widespread illnesses globally, posing serious public health challenges year after year. This project explores the environmental triggers of flu outbreaks by developing and evaluating advanced machine learning models to predict the spread of influenza in England, United Kingdom.

Spanning data from June 2015 to July 2024, the study integrates weather variables and air quality indicators to understand their influence on key flu subtypes — A(H1N1), A(H3N2), and Influenza B.

Using six machine learning models — including Gradient Boosting, Random Forest, and LSTM , the Gradient Boosting multivariate model consistently outperformed the others, achieving an R² of 0.774 and reducing prediction error significantly compared to univariate approaches.

Key environmental contributors identified include:

-Low temperature

-High relative humidity

-PM2.5

-SO₂

These insights are essential for improving public health preparedness, guiding vaccination strategies, and shaping data-driven early warning systems for influenza outbreaks.

Thank you for checking out my project!
I appreciate your interest and support.

A brief poster presentation slide has been provided at the link below, where you can find more information about the write-up and project details:
👉 https://drive.google.com/file/d/1C3_TB5k7mOaaXn78HenAnVnv1-WNBic5/view?usp=sharing

For those seeking an in-depth understanding, a 50-page detailed explanation of the project is also available at the same link. It includes methodology, data sources, model evaluations, results, and key insights.

👉https://drive.google.com/file/d/1hp08yuSHVqHvrO6X2c2sBiXKbiWwYkCg/view?usp=sharing

Please note: This project is shared under the CC BY-NC 4.0 License. Feel free to explore and learn from it, but do not use it for commercial purposes or reproduce it without proper attribution.


## 🗂️ Project Notebook and File Descriptions

### 📁 `prediction/`

- **`GBPred.ipynb`**  
  Uses **Gradient Boosting** to predict flu cases using **all variables combined** — both **weather (W)** and **air quality (AQ)**. This is a **multivariate model**.

- **`GBPred2.ipynb`**  
  Applies Gradient Boosting on **each input group separately** — one run for AQ and another for W. Helps compare performance between **individual factors** vs combined inputs.

- **`LSTM.ipynb`**  
  Uses **Long Short-Term Memory (LSTM)** neural network to model **time-series prediction** of flu spread using sequential AQ and W data.

- **`RDPred.ipynb`**  
  Implements **Random Forest Regression** to predict flu cases using combined variables. Focuses on model interpretability and ensemble performance.

- **`Univariate.ipynb`**  
  Predicts flu using **only one group of variables at a time** (e.g., AQ-only or W-only). Useful for benchmarking the predictive power of each group.

---

### 📁 `datasets/`

- **`airquality/`**  
  Contains raw/processed **air quality** data (PM2.5, CO, NO₂, SO₂, etc.).

- **`weather/`**  
  Contains **meteorological** data such as temperature, humidity, wind speed, surface pressure, etc.

- **`flu/`**  
  Stores flu surveillance data, possibly broken down by type (e.g., A(H1N1), B) and time.

- **`final_aggregated_data.csv`**  
  The **merged dataset** used for modeling. It combines flu, AQ, and W features aligned by time period (e.g., week).

---

### 📁 Main Repository Files

- **`CST.ipynb`**  
  Initial **exploratory data analysis (EDA)** — loads datasets, inspects structure, handles missing values, feature engineering and explores distributions.

- **`CSTPred.ipynb`**  
  Early **model experimentation** notebook. Tests multiple models to evaluate which approach performs best.

- **`CorrAnalysis.ipynb`**  
  Performs **correlation analysis and SHAP interpretation**. Explores how AQ and W variables relate to flu types and overall flu trends.

- **`merge_data.ipynb`**  
  Shows how flu, weather, and air quality data were **joined and merged** to create the final prediction-ready dataset.

- **`README.md`**  
  The file you’re reading — includes an overview, links to the poster and full project write-up, and licensing details.

