# Deep Portfolio Theory 

*Deep Portfolio Theory* is a portfolio selection method published by J. B. Heaton, N. G. Polson, J. H. Witte in May 2016


# Data

- Downloaded from Bloomberg Terminal

- Dates: from 2012/01/06 to 2016/04/29 (aligned with the paper)
	1. auto-encoder, calibration set: **2012/01/06 - 2013/12/27, 104 days** 
	2. validation, verification set: **2014/01/03 - 2016/04/29, 122 days** 

- As Section 2 of the paper states, stock data shall be treated as a matrix $X \in R^{T \times N}$, a market of $N$ stocks over $T$ time periods. You can consider it like: $T$ is number of data points (varied), $N$ is number of features (fixed).

- IBB Index Data (ibb_uq.csv) (The iShares Nasdaq Biotechnology ETF seeks to track the investment results of an index composed of biotechnology and pharmaceutical equities listed on the NASDAQ.)
    1. PX_LAST
    2. (absolute) Change
    3. % Change


- Component Stocks Data (percentage_change.csv)
    1. Some stock data are missing (not IPO yet, etc), so for data preprocessing, I ignore all the data without full record during 2012/01/06 to 2016/04/29.
    2. In this notebook I only use **percentage change** as input. I also prepare **net_change, last_price** in the repo if you are interested.


# Framework 

Python 3, Tensorflow, Keras 


