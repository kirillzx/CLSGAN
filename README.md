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
General pipeline of our method is presented below. For a detail description see the article.
![Pipeline](https://github.com/kirillzx/CLSGAN/blob/main/images/pipeline_V3-1.png)

We also proposed the modification of existing GAN architectures, adding Supervisor and second Discriminator.
![CLSGAN](https://github.com/kirillzx/CLSGAN/blob/main/images/CLS-GAN_Pipeline-1.png)

<img src="https://github.com/kirillzx/CLSGAN/blob/main/images/CLS-GAN_Pipeline-1.png"  width="60%" height="30%">

## Experiments
For the experiments we have used three open access datasets which describes stock prices. All data available in folder *Data* and even more [here](https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs).
For the quality assessment we have used distribution statistics (skewness, kurtosis), sum of absolute squared values of spectral density, Jensen-Schannon divergence, two-sample Kolmogorov-Smirnov test statistic, local extrema, autocorrelation and machine learning metrics (MSE on forecasting by time series cross-validation).

![Table](https://github.com/kirillzx/CLSGAN/blob/main/images/table.png)

![Autocorr](https://github.com/kirillzx/CLSGAN/blob/main/images/autocorr.png)

![LocalExtrema](https://github.com/kirillzx/CLSGAN/blob/main/images/local_extrema.png)

![Distr](https://github.com/kirillzx/CLSGAN/blob/main/images/distributions.png)


## Hyperparameters
![Hypers](https://github.com/kirillzx/CLSGAN/blob/main/images/hypers.png) 
