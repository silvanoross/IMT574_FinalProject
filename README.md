# Inventory Optimization Model Card

Advanced forecasting system for optimizing inventory levels and operational efficiency

<table>
<tr>
<td width="50%" valign="top" style="padding-right: 15px;">

## Model Details

*Developed by Felix Zhao, Jack Ko, and Silvano Ross at the University of Washington in IMT 574.*

- **SARIMAX Model** - [Statsmodels SARIMAX](https://www.statsmodels.org/stable/generated/statsmodels.tsa.statespace.sarimax.SARIMAX.html) for time series forecasting
- **XGBoost Random Forest Regressor** - [XGBRFRegressor](https://xgboost.readthedocs.io/en/stable/python/python_api.html#xgboost.XGBRFRegressor) for ensemble learning

## Intended Use

- Predict the error between demand forecasts and actual sales to optimize inventory management
- Identify when demand forecasts are likely to fall within acceptable error margins
- Anticipate scenarios where demand fails to meet actual sales
- Primary users: Inventory managers and supply chain specialists

## Training Data

Due to the time series nature of our analysis, we implemented a chronological data splitting strategy:

- The first 80% of chronologically ordered data was designated for model training
- Features with high correlation were eliminated to prevent data leakage
- Temporal validation was used to ensure the model could generalize to future periods

</td>
<td width="50%" valign="top" style="padding-left: 15px;">

## Evaluation Data

Our evaluation framework utilized the remaining 20% of chronological data:

- Out-of-sample testing on the most recent time periods
- Multiple evaluation metrics for comprehensive assessment


&nbsp; 

## Quantitative Analysis

We employed multiple complementary metrics:

- **RMSE** (Root Mean Squared Error): Measures the average magnitude of forecast errors
- **MAE** (Mean Absolute Error): Quantifies the average absolute difference
- **R²** (R-squared): Determines the proportion of variance explained

## Ethical Considerations

Our ethical assessment indicates minimal risk as the model:

- Uses synthetic data with no personally identifiable information
- Contains no real store names or branded product information
- Primary human impact: Potential job displacement through automation



</td>
</tr>
<tr>
<td colspan="2" style="padding-top: 20px; padding-bottom: 10px;">

## Caveats, Limitations and Recommendations

- We discovered challenges in directly predicting demand forecast errors
- Current scope is limited to a single store, region, and product category
- **Recommended extension:** Implement a grid search-style approach across all stores, products, and regions
- A framework of individually trained models would better account for diverse purchasing patterns

</td>
</tr>
</table>
