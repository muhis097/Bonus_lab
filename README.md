
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Lab4

<!-- badges: start -->

[![R-CMD-check](https://github.com/muhis097/Lab4n/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/muhis097/Lab4n/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

The goal of Lab4 is to …

## Installation

You can install the development version of Lab4 from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("muhis097/Lab4n")
```

## Example
## Lab 4 Project : Linear Regression in Refrence Class Style

In this package a satisfactory solution for Linear Regression was developed. In order to describe the functionaity of this class, a default data set included in Rstudio namely "Iris" is used. In first Step The main Regression model is coded. The end user can access internal method in various ways:

```{r , echo=FALSE}
data("iris")
lmod=linreg$new(Petal.Length ~ Species, data = iris)

print(lmod)


```
### print
print function simply output the result of regression in a nice way:

```{r 3 print}
lmod$print()
```
### Resid

The resid function shows the residuals as numeric vector.

```{r Resid}
lmod$resid()

```
### Pred

The Pred function return the predicted values of "y".

```{r pred}

lmod$pred()

```
### Coef
The coef function return the coecients as a named vector:

```{r coef}
lmod$coef()
```
### plot

The plot function shows the figure of The_fitted_valuesvs The_residuals in two modes 1- normal plot  2- Standardized plot(apllied scaling)

```{r Plot}
lmod$plot()

```

### Summary

This function return a similar printout as printed for lm objects, but here only the coefficients with their standard error, t-value and p-value as well as the estimate of σ and the degrees of freedom in the model is shown:

```{r Summary}

lmod$summary()

```
