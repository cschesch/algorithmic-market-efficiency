# algorithmic-market-efficiency

**Algorithmic Market Efficiency - HEC Master Thesis**

In this repository, you can find the code for the Master Thesis "Algorithmic Market Efficiency? Machine Learning, Outperformance and Arbitrage Activity along the Cross-Section of Stock Returns", which I wrote for the MSc in International Finance at HEC under thee supervision of Prof. Augustin Landier. You can find the thesis here, and the corresponding slides here.

**Abstract**

The literature on market efficiency has historically focussed on how new information is reflected in market prices. In this work, we try to explore how, for a constant information set, newer and better algorithms are reflected in prices, an effect we call algorithmic market efficiency. We build on an emerging body of work in the field of asset pricing that shows how Machine Learning algorithms substantially surpass classical methods like Ordinary Least Squares. Reproducing Gu et al. (2020), we use a large dataset of pricing factors, combined with an array of Machine Learning methods (notably trees and Neural Networks), to forecast stock returns out of sample. Nonlinear methods achieve remarkably high predictive power, and portfolios built using these predictions robustly outperform the market. To study whether this constitutes an arbitrage opportunity, or simply latent risk loadings, we analyse short interest along ML-predictions, and fail to find evidence of arbitrageurs exploiting more advanced algorithms to profit from ML-related pricing anomalies. We also do not find a decline in the profitability of a ML method after its publication. Finally, we explore market prescience, as measured by the relationship between short interest on a stock and its return, and find that it is generally low but not influenced by discoveries in this field. All of this suggests, but falls well short of proving, that Machine Learning techniques do not constitute an arbitrage opportunity and that markets are algorithmically efficient.

**Data and Data Sources**

I used several data sources for this project, which you well need to collect be able to run the code:

1) Factors from Gu et al. (2020), which you can download for free from [Dacheng Xiu's webpage](https://dachxiu.chicagobooth.edu/) [???]
2) Returns from the CRSP Database, which you can download with a WRDS access [???]
3) Fama-French factors, which you can download for free from [Kenneth French's webpage](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html) [???]
4) Macroeconomic predictors, which you can download for free from [Amit Goyal's webpage](http://www.hec.unil.ch/agoyal/) [???]
5) The Compustat Supplemental Short Interest File, which you can download with a WRDS access
6) The CRSP / Compustat Merged Security Monthly Dataset, which you can download with a WRDS access

**Code Structure**

There are three pieces of code saved as Jupyter Notebooks, 
