
<!-- README.md is generated from README.Rmd. Please edit that file -->
MDBED
=====

<!-- badges: start -->
<!-- badges: end -->
The goal of MDBED is to provide 3D plots of the Moran-Downton bivariate Exponential distribution (BED), generate bivariate random values, and also provide values of the joint and conditional PDFs and CDFs.

Installation
------------

You can install the released version of MDBED from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("lfduquey/MDBED")
```

Example
-------

This is a basic example of one of the functions of MDBED; the rBED function. This functions generates jointly Exponential random values (x,y). The required inputs are the n values to be generated, the correlation coefficient, and the scale parameters of the marginal distributions. The pairs (x,y) are plotted for a better interpretation.

``` r
library(MDBED)
## basic example code
Data<-rBED(n=100,Betax=1,Betay=1,rho=0.85)
plot(Data[,1],Data[,2], xlab = "x", ylab = "y")
```

<img src="man/figures/README-example-1.png" width="100%" />
