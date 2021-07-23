# Loss-Distribution-Model-Validation-
Project for Quantitative Risk Class (ECON 6295) where I improved upon another group's Excel model using Python. Our assignment was to assume the role of a model risk team and evaluate a risk model created by a different group. This group was tasked with forecasting operational losses based on data provided by our professor. They elected to use the loss distribution approach. The loss distribution is a compound distribution generated through sampling from a frequency distribution, which provides the number of loss events for a period, and a severity distribution, which provides the loss amount per loss event. Monte Carlo simulation can then be used to construct the compound distribution from sample draws of the selected frequency and severity distributions. The group used the Poisson distribution as the loss frequency distribution, parameterizing with $\lambda$ =1.065, the average number of loss events per period in the provided data, and the lognormal distribution as the loss severity distribution, parameterizing with $\mu = 1.159$ and $\sigma = 0.839$, the mean and sample standard deviation of logged loss severity data. After sampling from the loss distribution, Value at Risk (VaR) estimates could be produced, with the 90th percentile VaR being the final output of the risk model. The group constructed their model in Excel which resulted in a major problem, namely that they only used 1,000 Monte Carlo simulations, resulting in an unstable 90th percentile VaR (large fluctuations between refreshes). My code validates their results and also rectifies the problem of too few simulations. 