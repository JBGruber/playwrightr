
<!-- README.md is generated from README.Rmd. Please edit that file -->

# playwightr

<!-- badges: start -->
<!-- badges: end -->

{playwrightr} provides access the python library
[playwright](https://playwright.dev/python/docs/intro)

Playwright emulates web browsers and enables reliable end-to-end testing
for modern web apps.

## Installation

1.  Install playwright (in this example, we install playwright in a new
    conda environment)

``` bash
conda create -n pw python=3.7
conda activate pw
conda config --add channels conda-forge
conda config --add channels microsoft
conda install playwright
playwright install
```

1.  Install playwrightr from GitHub

``` r
# install.packages("devtools")
devtools::install_github("benjaminguinaudeau/playwrightr")
```

## Loading playwrightr

This is a basic example which shows you how to solve a common problem:

``` r
reticulate::use_condaenv("pw", required = TRUE)
options(python_init = TRUE)
library(reticulate)
library(playwrightr)
```

## Use Playwright to browse the web

``` r
chrome <- new_browser("chrome", headless = F)
page <- chrome$pages[[1]]

page$goto("https://google.com")
```
