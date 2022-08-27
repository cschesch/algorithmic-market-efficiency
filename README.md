# Algorithmic Market Efficiency - HEC Master Thesis

In this repository, you can find the code for the Master Thesis _"Algorithmic Market Efficiency? Machine Learning, Outperformance and Arbitrage Activity along the Cross-Section of Stock Returns"_, which I wrote in 2020 for the MSc in International Finance at HEC under the supervision of Prof. Augustin Landier. You can find the Thesis and the accompanying slides on this repository.


## Abstract

The literature on market efficiency has historically focussed on how new information is reflected in market prices. In this work, we try to explore how, for a constant information set, newer and better algorithms are reflected in prices, an effect we call _algorithmic market efficiency_. We build on an emerging body of work in the field of asset pricing that shows how Machine Learning algorithms substantially surpass classical methods like Ordinary Least Squares. Reproducing _Gu et al. (2020)_, we use a large dataset of pricing factors, combined with an array of Machine Learning methods (notably trees and Neural Networks), to forecast stock returns out of sample. Nonlinear methods achieve remarkably high predictive power, and portfolios built using these predictions robustly outperform the market. To study whether this constitutes an arbitrage opportunity, or simply latent risk loadings, we analyse short interest along ML-predictions, and fail to find evidence of arbitrageurs exploiting more advanced algorithms to profit from ML-related pricing anomalies. We also do not find a decline in the profitability of a ML method after its publication. Finally, we explore market prescience, as measured by the relationship between short interest on a stock and its return, and find that it is generally low but not influenced by discoveries in this field. All of this suggests, but falls well short of proving, that Machine Learning techniques do not constitute an arbitrage opportunity and that markets are algorithmically efficient.

## Data and Data Sources

I used several data sources for this project, which you will need to collect be able to run the code:

1) Factors from Gu et al. (2020), which you can download for free from [Dacheng Xiu's webpage](https://dachxiu.chicagobooth.edu/) [3.49 GB]
2) Returns from the CRSP Database, which you can download with a WRDS access [1.22 GB]
3) The Fama-French 3-factor, 5-factor and momentum series, which you can download for free from [Kenneth French's webpage](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html) [54 KB, 46KB and 20KB]
4) Macroeconomic predictors, which you can download for free from [Amit Goyal's webpage](http://www.hec.unil.ch/agoyal/) [255 KB]
5) The Compustat Supplemental Short Interest File, which you can download with a WRDS access [293 MB]
6) The CRSP / Compustat Merged Security Monthly Dataset, which you can download with a WRDS access [3.55 GB]

For each entry, you should download the full dataset covering all periods, tickers and variables. For the code to run, you need to put all of them into the data folder, with the names `factors.csv`, `factors.csv`, `ff.csv`, `ff5.csv`, `mom.csv`, `macropredictors.csv`, `shortinterest.csv` and `securitymonthly.csv`.


## Code Structure

There are three pieces of code saved as Jupyter Notebooks:

* `datapreparation.ipynb`: this code transforms the raw databases into a coherent dataset to be used for the Machine Learning predictions, the strategy return computations and the short interest analysis; it generates one dataset called `df_ml`, used in `machinelearning.ipynb`, and one called `df`, used in `predictionanalysis.ipynb`. This code takes about 15 minutes to execute.

* `machinelearning.ipynb`: this code uses the dataset as an input and forecasts returns using various machine learning techniques; it also does some more in-depth forecasting in 2016 to study the behaviour of ML estimators as well as the marginal utility of explanatory factors, which are then saved as graphs. Executing this code is _extremely long_, it takes about 1 to 2 months on a standard laptop : if you want to save some time, you can download the predictions it generates using [this](https://drive.google.com/drive/folders/1StsgEO0vaIv3g1y0BGpSavEFJvIHBmBW?usp=sharing) Google Drive link.

* `predictionanalysis.ipynb`: this code uses the return predictions generated by `machinelearning.ipynb` to (i) analyse their predictive performance, (ii) build arbitrage portfolios around those returns, (iii) study arbitrage activity aroudn ML forecasts, (iv) study the (lack of) post-publication decline of ML-alpha, (v)
analyze _market prescience_. It generates most of the graphs and tables used in the thesis itself, but should be reasonably quick to run.

If you have any questions on the data, the code or even the thesis itself, feel free to message me at c.schesch@gmail.com.


