# EX-2-Time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city

## AIM:
To Write a Program to time series analysis and decomposition on the monthly average temperature of a city/country

## Equipments Required:
Hardware – PCs

Anaconda – Python 3.7 Installation / Jupyter notebook

## Procedure:
1 Import the numpy and matplotlib.pyplot modules.

2 Read the dataset using pandas

3 plot the data using matplotlib.pyplot library function

4 Plot the data according to need, either seasonal_decomposition or trend plot.

5 Display the overall results.

## Program:
```
/*
To Write a Program to time series analysis and decomposition on the monthly average temperature of a city/country 
Developed by: Praveen s
RegisterNumber:  212222240077
*/
import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose
data =pd.read_csv("/content/temperatures.csv",parse_dates=["YEAR"])
data.head()

data.set_index("YEAR",inplace=True)
data.index=pd.to_datetime(data.index)

data.dropna(inplace=True)
data.plot()

result=seasonal_decompose(data["ANNUAL"],model="multiplicable",period=12)

result.seasonal.plot()

result.trend.plot()

result.plot()
```
## Output:
### data.head()
![Screenshot 2023-10-06 155049](https://github.com/s-adhithya/EX-2-Time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city/assets/113497423/e8c5a394-dc25-4242-9b0e-8248c109b2f4)


### data.plot()
![Screenshot 2023-10-06 155112](https://github.com/s-adhithya/EX-2-Time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city/assets/113497423/95056fe9-a62a-4b73-98ef-f52c86578cb8)


### result.seasonal.plot()
![Screenshot 2023-10-06 155133](https://github.com/s-adhithya/EX-2-Time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city/assets/113497423/53ad4d87-1582-4aa1-aabb-3ce348665576)


### result.trend.plot()
![Screenshot 2023-10-06 155201](https://github.com/s-adhithya/EX-2-Time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city/assets/113497423/84865d9e-96ac-493c-9af9-78ccd81921d3)

### result.plot()
![Screenshot 2023-10-06 155226](https://github.com/s-adhithya/EX-2-Time-series-analysis-and-decomposition-on-the-monthly-average-temperature-of-a-city/assets/113497423/0678a913-0ed7-4a07-aa57-ec0b969b08fb)


## Result:
Thus the program to time series analysis and decomposition on the monthly average temperature of a city/country is written and verified using python programming.
