

# Motivation

Recent inflation number and house price records in Canada have constantly make news. This report is inspired by [the analysis carried out by Bank of Canada in 2015](https://www.bankofcanada.ca/2015/08/long-term-evolution-house-prices/), however, I want to use more up-to-date data from Statistics Canada.

**please note that due to limited storage of git repos, the csv files referenced in DataAnalysis.ipynb need to be redownload using metadata files in data/raw**

# Summarized findings
- Overview of New housing price index (NHPI) in Canada and the 5 economically biggest province in Canada

    - From Fig 1 we can see that from 1990, new house price index (NHPI) in general for Canada remained relatively stable during 1990-1999, grew linearly during 2010-2018, experienced exponential growth during 2000-2008 and 2019-2021. Suprisingly, Canada's NHPI is only minimally affected by financial crisis in 2008.

    ![Fig 1. NHPI for total house value from 1990 to 2022](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig1.png?raw=true)

    - From Fig 2, the order of the NHPI among the top 5 provinces remained consistent during 1990-2005 period where the order follows as BC, QC, ON (close second), AB, SK. During 2006-2019, it can be observed that new house prices in the Prairies increase dramatically, and the top 5 provinces remain similar level of NHPI. However, from 2019, we can observe a bifurcation of NHPI among the 5 into 2 groups: ON, BC, QC vs AB and SK.

    ![Fig 2. NHPI for total house value of 5 economically largest province from 1990 to 2022](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig2.png?raw=true)

- Demand side analysis

    - NHPI vs median income:

        - From Fig. 3, for Canada, it seems that median income correlates with NHPI. However, we can see that the NHPI increases at a quicker rate than median income. For instance, during 2000-2020, while NHPI increases more than 166%, median total income for an average canadian only increases less than 133%.

        ![Fig 3. NHPI vs Total median income for Canada](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig3.png?raw=true)

        - In general, the provinces NHPI and total median income follow the same behavior as Canada in general: median income does not increase as quickly as NHPI. For instance from 2000 to 2020, the rate of increases of NHPI vs median income for each provinces are:
            - Ontario (Fig 4): 190% vs 114%
            - Quebec (Fig 5): 198% vs 134%
            - BC (Fig 6): 147% vs 130%
            - Alberta (Fig 7): 211% vs 124%
            - Saskatchewan (Fig 8): 237% vs 144%

        ![Fig 4. NHPI vs Total median income for Ontario](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig4.png?raw=true)

        ![Fig 5. NHPI vs Total median income for Quebec](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig5.png?raw=true)

        ![Fig 6. NHPI vs Total median income for British Columbia](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig6.png?raw=true)

        ![Fig 7. NHPI vs Total median income for Alberta](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig7.png?raw=true)

        - It is also very interesting to note that for all except SK, we can see a dip in median income from the 90s that bottoms around 2000. However, NHPI curves only follow the same behavior in ON, which is not severe, and BC, which is quite severe.

        ![Fig 8. NHPI vs Total median income for Saskatchewan](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig8.png?raw=true)

        - Additionally, QC's NPHI has never really decrease but only plateaued.

        - Among the provinces only BC and AB experience a drop in NHPI during economic recession of 2008, whereas the NHPI of the other provinces do not seem to correlate with the event.

    - NHPI vs population:

        - From Fig 9. it is very suprising to see how well the 2 curves of NHPI and population correlate.

        ![Fig 9. Fig 9. NHPI vs Population for Canada](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig9.png?raw=true)

        - Among the provinces, the two fascinating cases are BC and SK:

            - For BC, in Fig 12, during 1995 and 2005, we can see the drop and the rebound of NHPI happens during the period of population growth rate slows down

            ![Fig 12. Fig 12. NHPI vs Population for British Columbia](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig12.png?raw=true)

            - For SK, in Fig 14, up to 2005, the population had been slowly decreasing. However, despite this fact, NHPI still grows linearly. More shockingly, after 2005, population experiences a sudden growth and almost immediately we can see the rate of increase of NHPI immediately speed up. It is very likely that the population increase is due to the introduction of a new immigration program and is not from inter-province migration, and these new immigrants to SK might have purchased homes which increase the demand thus increase the price of new homes. However, this is an speculative observation that requires further data-driven investigation to be proven correct.

            ![Fig 14. NHPI vs Population for Saskatchewan](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig14.png?raw=true)
- Supply side analysis

    - NHPI vs industrial product price index (IPPI):
        - Over a long period of time, it can be seen that NHPI does not correlate with industrial product price index as shown in Fig 15. Specifically, during 2000-2018, it is clear that NHPI increases at a faster rate than IPPI. Moreover, NHPI can even drop for Vancouver while IPPI increases slightly during the same period. All of this indicates IPPI generally only play a minor role in NHPI.

        ![Fig 15. NHPI vs IPPI for Canada and Top 3 economically biggest provinces](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig15.png?raw=true)

        - However, when there is a sudden spike in IPPI as shown in Fig 16, where IPPI increases by 150%, only during 8 months, between July 2020 and March 2021. We can see NHPI correlates immediately with IPPI of construction materical.

        ![Fig 16. NHPI vs IPPI for Canada and Top 3 economically biggest provinces from January 2019](https://github.com/ChinhTranKaizen/StatCanHousing/blob/main/Figures/Fig16.png?raw=true)

        - Interestingly, if we look at Quebec case, we can see in the figure that its NHPI increased before there were a change in IPPI of construction product. Thus, there remains an interesting case to look into to find the possible elements that could explain this behavior of NHPI of Quebec.

        - Finally, we can see there exists a delayed in change of rate between the IPPI and NHPI of Canada and the provinces. Thus, carrying out the cross-correlation analysis between IPPI and NHPI time series during this time segment would be eye-opening on the effect of construction material price on new housing price.

# Future work
- Change normalization method to a more accurate one

- Analyze the period for QC where IPPI does not change but NHPI still increases

- Look more closely at BC case where NHPI had a bowl shaped curve from 1995 and 2005

- To prepare the time series data for cross-correlation analysis or any future machine learning tasks, I should try to employ sophisticated time-series normalizing tool such as [adaptive normalization](https://homepages.dcc.ufmg.br/~glpappa/papers/Ogasawaraetal-2010-IJCNN.pdf) or [normalization with deep-learning](https://arxiv.org/pdf/1902.07892.pdf), which has [a github page](https://github.com/gdepalma93/PyTorch-Timeseries-Normalization).
