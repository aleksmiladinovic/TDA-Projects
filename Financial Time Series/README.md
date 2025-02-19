# Financial Time Series

In this notebook, we demonstrate the use of Topological Data Analysis (TDA) methods in predicting the *crysis* in technological industries.

For this purpose, we use the stock market values of six tech companies over the period from 2019 to 2024. The companies involved include: *Apple*, *Tesla*, *Nvidia*, *Microsoft*, *Google* and *Meta*.  
The data used in this notebook is obtained from the Kaggle platform and can be found [here](https://www.kaggle.com/datasets/saketk511/2019-2024-us-stock-market-data).

The main idea follows that of the paper *Topological Data Analysis of Financial Time Series: Landscapes of Crashes* by Marian Gidea and Yuri Katz, which can be found [here](https://arxiv.org/abs/1703.04385).

Given a $6$-dimensional time series (as in our case), we take a sliding window of size $w$. Hence, each window consists of $w$ $6$-dimensional points. For each window we compute the persistence diagram of the Vietoris-Rips complex on the points of the window. We then compute the $L^p$-norms (with $p=1,2$) of the persistence landscape of the persistence classes in the dimension $1$. Consequently, we obtain a series of $L^p$-norms of our sliding window. This data gives us an insight into the stability of the Stock Market.

**Why persistent landscapes?**  
Persistence landscapes are computed from persistence diagrams, and, although both persistence diagrams and landscapes admit a metric, persistence landscapes can be embedded into a Banach space, meaning that we can extract all of the standard statistical properties. For more information, see the original paper of Gidea and Katz.
