Time series data has many important applications such as stocks, weather and GDP. Certain statistical tests that can be used normaly may not work on time dependent data because of its cyclical nature. With time seriese we can manipulate and look at the data in ways that reveal trends in the data despite its cyclic nature. We can easily make an ARMA model by using the statsmodel module.
```python
from statsmodels.tsa.arima_model import ARMA
#df is our data that is indexed by a time component.
ar = ARMA(df['target'].diff().values[1:], (3, 1)).fit()
ar.summary()
```
