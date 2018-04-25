## NOTES

#### Possible problems
* GP Assumes that the observations come from Gaussian process, do we satisfy this?
    * * "The assumption that our observations came from a Gaussian process is a very strong assumption" https://blog.sigopt.com/posts/intuition-behind-gaussian-processes
    * We sort of do, but we know it doesn't. We try to approximate it by a Gaussian Process. 
* The toy dataset sort of works with periodic kernel
    *Add bias, not multiply

#### Approaches
* Data by weekday
* ~~Two dimensional. Weekday + weeknumber?~~
    * * Periodic kernel defined only for 1dim
    
    
#### Meeting with Michael
* Fourier transform
* log-transform data
    * Seems to work a bit better, though still hard to get the real trend for test data
* non-stationary kernels
* Brownian motion kernel
* Make some more complicated toy data with linear/RBF trend. Do experiments with data with and without periodicity. See if variance of periodic kernel is different
    *  goal is to show if modeling periodicity like this even makes sense