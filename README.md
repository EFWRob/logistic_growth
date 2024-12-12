#logistic_growth
R scripts for a reproducible analysis of logistic growth
Question 1:

The study aims to model the population growth over time and estimate key parameters for the logistic growth equation. The dataset comes from experiment.csv, which contained the variables t (time) and corresponding population size N (number of individuals).  
Firstly, the parameters N0 (initial population size), r (growth rate) and K (carring capacity), were estimated by splitting the dataset into two sections, which were both linearly approximated. For the first segment –the early growth phase where t<1300 and K>>N0 – a linear model was fitted to the logarithm of the population size (Log(N)) to estimate r for this phase. For the second segment – the equilibrium phase with t>2500 – a linear model was used to estimate K. 
The results from this model were that N0 was exp(6.889) ≈ 981, r was found to be ~0.01 and K was estimated to be 6 * 10^10

Question 2


The continuous exponential equation goes: f(x) = N0*e^r*t, using this in R we get: 
N1 <- N0 * exp(r * 4980). N1 (population at t=4980) = 4.602307e+24.  
This is much larger than the logistic growth which reaches equilibrium at 6.00 * 10^10, because it is limited by carrying capacity.

Question 3:
Image of growth comparison:
![growth_comparison](https://github.com/user-attachments/assets/09a8db1d-b9a9-475c-9ab4-abe96c6f4226)




