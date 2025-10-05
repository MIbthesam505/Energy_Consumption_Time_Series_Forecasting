# ⚡ Time Series Forecasting with AR, ARIMA, and Other Models

This repository contains experiments with **time series forecasting algorithms** applied to electricity consumption data. The focus is on building and comparing different forecasting methods such as **AR (AutoRegression)**, **ARIMA**, and other classical models.

---

## 📂 Project Structure

```
forecastingAlgos.ipynb   # Main Jupyter Notebook with all implementations
data/                    # (Optional) Directory to store dataset
README.md                # Project documentation
```

---

## 📊 Dataset

The project uses a **household electricity consumption dataset**.

* Key variable: `Global_active_power`
* Time indexed (resampled daily / monthly for trend analysis).

You can replace this dataset with any univariate time series by updating the `dfSeven` variable in the notebook.

---

## 🚀 Implemented Methods

### 1. Exploratory Data Analysis (EDA)

* Overall energy trend plotting
* Monthly consumption trends using `matplotlib`

### 2. AR (AutoRegression)

* Uses `statsmodels.tsa.ar_model.AutoReg`
* Splits the dataset into **train/test sets**
* Forecasts values and evaluates performance with **Mean Squared Error (MSE)**

### 3. ARIMA

* Uses `statsmodels.tsa.arima.model.ARIMA`
* Tested with configurations like `(2,2,1)`
* Produces predictions for test set
* Evaluation using **MSE** and error percentage

### 4. (Optional Extensions)

* Auto-adjustment of lags in AR to avoid small dataset issues
* Handling of outliers and stationarity checks

---

## 📈 Results

* Plots show **true vs predicted values** for each model
* Error metrics (MSE, % error) are displayed on plots
* ARIMA typically outperforms AR, but results depend on dataset length and stationarity

---

## ⚙️ Requirements

Install dependencies before running the notebook:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels plotly
```

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Launch Jupyter Notebook:

   ```bash
   jupyter notebook forecastingAlgos.ipynb
   ```
3. Run cells in order to reproduce results.

---

## 📌 Key Notes

* `AR` from older `statsmodels` is deprecated → replaced with `AutoReg`.
* `ARIMA` from `statsmodels.tsa.arima_model` is deprecated → replaced with `statsmodels.tsa.arima.model.ARIMA`.
* Code is updated accordingly to avoid compatibility issues.

---

## 📚 References

* [Statsmodels Documentation](https://www.statsmodels.org/stable/index.html)
* [Box-Jenkins Methodology for ARIMA](https://en.wikipedia.org/wiki/Box–Jenkins_method)

---

## ✨ Future Improvements

* Add SARIMA for seasonality
* Compare with machine learning models (XGBoost, LSTMs)
* Deploy a small interactive dashboard using Plotly/Dash

---

Would you like me to also include **sample output plots (screenshots)** in the README (GitHub supports inline images), so your repo looks more attractive?
