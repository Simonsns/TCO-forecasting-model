# Greening Europe's truck fleets: a Monte Carlo approach

In France, the transport sector is the biggest emitter of greenhouse gas emissions, accounting for 31.1% of the total (France, 2019) (Insee, 2023, formatted). 
Against a backdrop of accelerating emissions reduction policies at European level, such as the Fit for 55 objectives, alternative powertrains are multiplying and offering highly ambitious alternatives. Nevertheless, players in the transport sector find them-selves forced to transform their fleets by making major capital investments. What's more, the uncertainty of the future market for the various energies and the probable but not certain economies of scale are putting the brakes on France's emission reduction ambitions. In order to provide the most objective possible analysis of the various fuels of the future, we have chosen to use a total cost of ownership analysis to assess the viability of each energy source separately, from a purely economic point of view. The aim of our work is therefore to calculate the most cost-effective energy source by 2050, comparing each with its diesel counterpart. 
We wanted to study the economic viability of as many alternative energies as possible, so as to provide a fairly complete picture of the information available to users.

To account for future uncertainties - whether related to vehicle acquisition costs, energy price trajectories, economies of scale or technological advances - we have adopted a Monte Carlo approach. This method enables us to generate probabilistic price intervals rather than relying on fixed estimates, thereby capturing the variability inherent in market dynamics and technological evolution. By simulating a wide range of possible scenarios, we aim to provide a more robust and realistic assessment of future costs.

Within the framework of this project, optimized libraries such as NumPy and Numba were used to accelerate calculations considerably, particularly for tensor manipulation and addition. The Monte Carlo approach implemented is based on **a tensor representation of the simulations**: each dimension of the tensor corresponds to a specific index of the problem (vehicle type, fuel, year), while the last dimension groups together all the simulated realizations. This structure effectively exploits the parallelism and low-level optimizations offered by these libraries, significantly reducing computation time. 

Finally, price trajectories can be of two kinds: 
- From simulations based on ARIMA models of historical energy market data (price_energy_evolutions.ipynb)
- Or from a random draw of between -2% and 2% of the price growth rate, with the prices from the Stratégie Nationale Bas Carbone (SNBC) as the trajectory base.

**More details in the methodology section**
