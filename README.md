# Data Science Projects

Projects completed during the **TripleTen Data Science Bootcamp (2025–2026)**. They cover supervised learning (regression and classification), time series forecasting, statistical analysis and hypothesis testing, using Python, pandas, scikit-learn, LightGBM, CatBoost and XGBoost.

> The notebooks are written in Spanish. Datasets are provided by the bootcamp platform and are not included in this repository; each notebook shows its outputs.

## Machine learning projects

| Project | Problem | Approach | Result |
|---|---|---|---|
| [Rusty Bargain: used car price prediction](rusty-bargain-price-prediction.ipynb) | Predict the market value of a used car from its specifications. | Outlier filtering and missing value treatment; one-hot encoding vs. native categorical handling depending on the model. Compared linear regression, decision tree, random forest, LightGBM, CatBoost and XGBoost on error and on training/prediction time. | LightGBM: **RMSE ≈ 1,524** (linear regression: 2,799), with a training time of about 6 s. Chosen as the best quality/speed trade-off. |
| [Interconnect: customer churn prediction](interconnect-churn-prediction.ipynb) | Identify telecom customers likely to cancel, so retention offers can be targeted. | Integrated contract, personal, internet and phone data; engineered features such as tenure; handled class imbalance with class weighting; tuned LightGBM with `RandomizedSearchCV`. Compared against logistic regression and random forest baselines. | Test set: **AUC-ROC 0.84**, **Recall 0.80**, F1 0.62. Recall is up from 0.49–0.57 in the baselines, so about 4 of 5 customers who leave are flagged. |
| [Sweet Lift Taxi: hourly demand forecasting](sweet-lift-taxi-forecasting.ipynb) | Forecast taxi orders for the next hour at airports, to allocate drivers in peak periods. | Lag features, rolling statistics and calendar variables; `TimeSeriesSplit` for tuning to respect temporal order. Compared naive, mean, linear regression, random forest and LightGBM. | LightGBM: **test RMSE ≈ 41.6**, below the target of 48. Baselines: 58.9 (naive, previous hour) and 84.7 (mean). |

## Statistical analysis projects

| Project | Question | Result |
|---|---|---|
| [Megaline: which prepaid plan earns more?](megaline-tariff-analysis.ipynb) | Compare the Surf and Ultimate plans using usage data from 500 customers in 2018. | Built a monthly user table following the billing rules (rounding of minutes and GB). Ultimate shows higher and more stable average revenue; a two-sample test rejects equal average revenue at α = 0.05. |
| [Video game market analysis](video-game-market-analysis.ipynb) | Which platforms and genres to prioritize for a 2017 campaign. | Used 2010–2016 data. Platforms have a life cycle of about 5–7 years; PS4 and Xbox One lead growth. Action, Shooter and Sports are the top genres. Regional profiles differ (Japan prefers 3DS and RPGs). |
| [Chicago taxi trips](chicago-taxi-trips-analysis.ipynb) | Which companies and neighborhoods concentrate trips, and does weather affect trips to O'Hare airport? | Charts of trips by company and top drop-off neighborhoods. Two-sample t-test (α = 0.05) on the duration of Saturday trips from the Loop to O'Hare: **rejects equal mean duration** between bad and good weather (t ≈ 6.9). |

## Tools

Python · pandas · NumPy · scikit-learn · LightGBM · CatBoost · XGBoost · SciPy · Matplotlib · Jupyter

## Contact

**Josué Espino** · [LinkedIn](https://linkedin.com/in/espino-josue) · [Portfolio](https://josueespino501.github.io)
