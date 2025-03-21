# Model Card
Explore inventory data and determine how to best optimize operational levels. 

## Model Details
- Developed by Felix Zhao, Jack Ko, and Silvano Ross at the University of Washington in IMT 574.
- SARIMAX Model - [Statsmodels ARIMA](https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html)
- XGBoost 
- 

## Intended Use
- Our intended use is to be able to predict the error in demand forecast versus actual sales to help us better manage inventory levels to prevent understocking of items.
- We would use a confidence interval to give our demand forecast a way of always being in overstocked.
- The users of this model would be managers and inventory specialists in charge of ordering supplies for their stores. 

## Factors

## Metrics

## Evaluation Data

## Training Data

## Quantitative Analysis
- We used **root-mean-squared error** and **mean absolute error** to evaluate our model performance. This measures the error in predictions based on the mean and the median.

### Ethical Considerations
- This model uses no real data and there is no possibility of a HIPPA violation. There are not even real store names. The biggest risk to humans would be potential job loss through using this model and getting incorrect predictions on how to adjust inventory. 

### Caveats and Recomnendations
- We had issues with getting accurate predictions only to determine that it may be impossible to predict demand forecast error. This made us pivot to try and develop a better buffer to prevent our demand forecast from under stocking and for not over stocking too greatly. 
