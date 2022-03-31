# Motivation

Recent inflation number and house price records in Canada have constantly make news. This report is inspired by [the analysis carried out by Bank of Canada in 2015](https://www.bankofcanada.ca/2015/08/long-term-evolution-house-prices/), however, I want to use more up-to-date data from Statistics Canada.

# Summarized findings
- Overview of New housing price index (NHPI) in Canada and the 5 economically biggest province in Canada
    - From Fig 1 we can see that from 1990, new house price index (NHPI) in general for Canada remained relatively stable during 1990-1999, grew linearly during 2010-2018, experienced exponential growth during 2000-2008 and 2019-2021. Suprisingly, Canada's NHPI is only minimally affected by financial crisis in 2008.
    ![Fig 1. NHPI for total house value from 1990 to 2022](/StatCanHousing/Figures/Fig1.png?raw=true "NHPI for total house value from 1990 to 2022")

# Future work
- Change normalization method to a more accurate one

- Analyze the period for QC where IPPI does not change but NHPI still increases

- Look more closely at BC case where NHPI had a bowl shaped curve from 1995 and 2005

# Set back of the current work
- Normalizing time series non-stationary economic data is done currently using MinMaxScaler, which is not accurate but is a quick way to produce proof of concept.
    - To lead to a more accurate result, and to prepare the time series data for any future machine learning tasks, one should employ more sophisticated tool such as [adaptive normalization](https://homepages.dcc.ufmg.br/~glpappa/papers/Ogasawaraetal-2010-IJCNN.pdf) or [normalization with deep-learning](https://arxiv.org/pdf/1902.07892.pdf), which has [a github page](https://github.com/gdepalma93/PyTorch-Timeseries-Normalization).