# K1996, JEL
Paper: Kocherlakota, Narayana R. "The equity premium: It's still a puzzle." Journal of Economic Literature 34.1 (1996): 42-71.

Contributor: Dian Jiao 

Email: dj2526@columbia.edu

## Introduction
I replicated Figures 1 to 3 and Tables 1 to 4 in Kocherlakota (1996). As a validation check, I also replicate Grossman and Shiller 1981, p. 225, fig. 1. 

## Data Description
I use the consumption data from [Shiller’s website](http://www.econ.yale.edu/~shiller/data.htm). In my replication, I focuse on 1948 and onward. The red dotted line indicates the beginning of the sample period in my replication, and the black dotted line indicates the ending of the sample period in Kocherlakota (1996). 

Shiller's data does not include the 3-month treasury bill rate used in Kocherlakota (1996), so I used the real one-year interest rate as an approximation, which, though not identical, is arguably a reasonable proxy for the riskless rate. 

## Technical Specification
Coding Language: Python
Software: jupyter notebook

## Comments
There are two points I am unclear about the paper:
1. One puzzle is how Kocherlakota (1996) solves the case for $\alpha=1$ in Table 4, where the condition is not well-defined. 
2. The second is the equation provided under Table 3, $e_t=\beta(c_{t+1}/c_t)^{-\alpha}(R_{t+1}^b-1)$ seems wrong. I followed equation (2b') instead, i.e., $e_t=\beta(c_{t+1}/c_t)^{-\alpha}R_{t+1}^b-1$. Only in this way was I able to replicate similar results. 

Some major differences:
1. In replicating Table 2, the sample means of $e$ vary more w.r.t. $\alpha$, and the t-stats are smaller. 
2. In replicating Table 3, the t-stats are less significant. 
3. In replicating Table 4, the fitted IESs vary less w.r.t. $\alpha$. 

My results differ from Kocherlakota's (1996) for two major reasons:
- The distributional features of the variables are significantly different in the two sample periods (see the replicating figures). In particular, the stock return and real riskless rate are less volatile post-1948, and there are fewer negative real riskless rates appearing post-1948.
- In my results, I use the real one-year interest rate as an approximation for the riskless rate, which is different from the nuanced data choices in Kocherlakota (1996). This causes observable differences even within the sample period of Kocherlakota (1996) (see the line charts). 