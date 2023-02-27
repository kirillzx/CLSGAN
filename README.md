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

## Experiments
For the experiments we have used three open access datasets which describes stock prices. All data available in folder *Data* and even more [here](https://www.kaggle.com/datasets/borismarjanovic/price-volume-data-for-all-us-stocks-etfs).


![This is an image](https://github.com/kirillzx/CLSGAN/blob/main/images/Local_Extr_fisi.png)


## Hyperparameters

$$
\usepackage{booktabs}
\vspace{-5mm}
\begingroup
\setlength{\tabcolsep}{4 pt}
\renewcommand{\arraystretch}{1} 
\begin{table}[h!]
\caption{Hyperparameters for CLGAN and CLSGAN}\label{tab: hypers}
\centering
\begin{tabular}{rcc}
    \toprule
    \textbf{Hyperparameters} & \textbf{CLGAN} & \textbf{CLSGAN}\\
    \midrule
    $M$&23&20\\
    initial learning rate & 0.002 & 0.002 (and 0.02 for Supervisor)\\
    learning rate scheduler MultiStep & 0.1 after 8 epochs & 0.1 after 10 epochs\\
    generator training & every 5 iteration & every 5 iteration\\
    supervisor training & -- & every 5 iteration\\
    batch size & 80 & 80\\
    sequence length & 127 & 127\\
    number of clusters & 3 & 3\\
    clip value for discriminator & 0.01 & 0.01\\
    \bottomrule
\end{tabular}
\end{table}
\endgroup
$$
