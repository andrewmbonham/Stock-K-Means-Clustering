# Stock K-Means Clustering

(Note: GitHub does not display interactive scatter plots. 
Execute the code to visualize all the data, which includes
scatter plots that display the company ticker when the 
cursor is over the data point.)

## Task
The task here was to cluster S&P 500 stocks based on returns, 
volatility, and fundamental data such as PE and price-to-book ratios. 

## Description
The challenge was solved by using yfinance and `pandas` to process
equity data, which was then clustered using the `skearn` `KMeans` class
using values of `k` selected based on Silhouette analysis from `yellobrick`.

## Installation
The following Python 3 packages are required:
- numpy 
- pandas
- matplotlib
- plotly
- scipy
- sklearn
- yellowbrick
- yfinance

To install the packages, run `pip install <package>`

## Usage
Simply run all cells. The data will be obtained using `yfinance`, which 
may take 1 - 2 minutes for all ~500 companies, depending on the part of 
the notebook. Normalization is optional and various normalization code 
can be left commented or uncommented, depending on user preference. 
Values of `k` can also be adjusted at user discretion, although the 
general rule of thumb is to assess the Silhouette plot and choose a value
of `k` that produced roughly uniform widths, with all "heights" being 
greater than the mean value (dotted line). Due to randomness, this is 
not always achievable, but normalization or the lack thereof can also 
affect these plots, and thus the chosen value of `k`. 
