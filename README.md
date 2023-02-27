# Synthetic financial time series generation with regime clustering
### Authors: Kirill Zakharov, Elizaveta Stavinova

Official realisation by our article (link will be later).
## Installation
To use the method's code, you must install following Python libraries:
```
pip install ruptures
pip install stumpy
pip install scipy
pip install sklearn
pip install torch torchvision
pip install yfinance
pip install pyts
pip install statsmodels
pip install fbprophet
```


## Method
General pipeline of out method is presented below.
![Pipeline](https://github.com/kirillzx/CLSGAN/blob/main/images/pipeline_V3-1.png)

## Experiments
For experiments we have used three open access datasets which describes stock prices. All data available in folder *Data* and even more [here](https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs).

![This is an image](https://github.com/kirillzx/CLSGAN/blob/main/images/Local_Extr_fisi.png)
