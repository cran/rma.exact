# rma.exact

The function "rma.exact" aomputes an exact (up to monte carlo error), unconditional, non-randomized CI for the grand mean in a random effects meta-analysis assuming a normal-normal model for the primary study observations. This function implements the algorithm described in:

Michael, Thornton, Xie, and Tian (2017). Exact Inference on the Random Effects Model for Meta-Analyses with Few Studies. (Submitted.)

## Example

Given K primary studies, suppose "yi" contains the reported effect estimates and "vi" their variances. Synthetic data is given below. An estimate of the grand mean is obtained as follows:

K <- 5
c0 <- 1
mu0 <- 0
tau2 <- 12.5
vi <- (seq(1, 5, length=K))^2
yi <- rnorm(K)*sqrt(vi+tau2)+mu0
rma.exact(yi=yi,vi=vi)

```R
...
```
