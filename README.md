# Option Pricing
This project applies an object oriented approach to compute the prices of American and European Call and Put options using different pricing methods such as Monte Carlo, the analytical Black-Scholes formula and the Binomial tree method.

## *Option Pricing using Binomial Tree Model*
Generates a binomial option pricing tree based on the parameters one inputs in order to achieve the price of the option premium. Applicable to European as well as American options. 

![demo](src/Binomial%20Tree%20Model/Pictures/Screen%20Shot%202019-07-23%20at%202.07.12%20PM.png)
  

## *Option Pricing Using Monte Carlo Simulation*

#### The project "MC" has been taken from https://github.com/RedwanBouizi/MC.git and is used for understanding purposes. I do not claim copyright over this material.

### Description ###
In this project we have implemented some Monte-Carlo simulations around the Black-Scholes and Heston models.
Given some parameters of an european call option, this code computes for {100, 10000, 100000} simulations the following quantities:
- price
- delta
- gamma
- vega

Some reduction variance methods have been implemented:
- Antithetic Variables
- Control Variates
- Importance Sampling

All of them show great improvements in the estimator accuracy.


We have also plotted the price and greeks on a same scale against the spot, maturity and volatility (only for the Black-Scholes model in the latter).


### Requirements ###
- gnuplot > 5.2 (tested with qt terminal) http://www.gnuplot.info/download.html
- gnuplot-iostream interface http://stahlke.org/dan/gnuplot-iostream/
- boost > 1.63.0 http://www.boost.org/users/download/
- cmake > 3.8 https://cmake.org/download/

### Build and run ###
1. clone the git repository: `git clone https://github.com/RedwanBouizi/MC.git`
2. go to MC directory: `cd MC`
3. create a build directory: `mkdir build`
4. go to build directory: `cd build`
5. `cmake ../`
6. `make`

Both the library and executable should now be built respectively in `/src` and `/tests`. To run the executable, follow these commands:
1. `cd tests`
2. `./example -1 -2 -3`

Option 1: performs price and greeks computation using the Black-Scholes and Heston models.

Option 2: outputs several graphs telling about the influence of spot, maturity, volatility over the price and greeks computations.

Option 3: shows how the asymmetry (price and greeks) evolves as the correlation between brownian motions in the Heston model increases.

The latter is quite long, which is why we have included the outputs below.

![demo](src/Monte%20Carlo/MC/gifs/price.gif)

![demo](src/Monte%20Carlo/MC/gifs/delta.gif)

![demo](src/Monte%20Carlo/MC/gifs/gamma.gif)

![demo](src/Monte%20Carlo/MC/gifs/vega.gif)

