# Motivation

Recent inflation number and house price records have constantly make news. This report is inspired by [the analysis carried out by Bank of Canada in 2015](https://www.bankofcanada.ca/2015/08/long-term-evolution-house-prices/) using more up-to-date data from Statistics Canada.

# Summarized findings

# Future work
- Change normalization method to a more accurate one

# Set back of the current work
- Normalizing time series non-stationary economic data is done currently using MinMaxScaler, which is not accurate but is a quick way to produce proof of concept.
    - To lead to a more accurate result, and to prepare the time series data for any future machine learning tasks, one should employ more sophisticated tool such as [adaptive normalization](https://homepages.dcc.ufmg.br/~glpappa/papers/Ogasawaraetal-2010-IJCNN.pdf) or [normalization with deep-learning](https://arxiv.org/pdf/1902.07892.pdf), which has [a github page](https://github.com/gdepalma93/PyTorch-Timeseries-Normalization).