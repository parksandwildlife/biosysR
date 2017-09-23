
<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Travis-CI Build Status](https://travis-ci.org/parksandwildlife/biosysR.png?branch=master)](https://travis-ci.org/parksandwildlife/biosysR) [![Coverage Status](https://coveralls.io/repos/github/parksandwildlife/biosysR/badge.svg?branch=master)](https://coveralls.io/github/parksandwildlife/biosysR?branch=master)

biosysR makes BioSys data accessible in R
=========================================

TODO section on BioSys.

If the data consumer however wishes to analyse data in a statistical package like R, the data need to be transformed from a nested list of lists (JSON) into a two-dimensional tablular structure.

The main purpose of `biosysR` is to facilitate reading, parsing and using BioSys data by providing helpers to access the API and flatten the API outputs into a [tidy](http://vita.had.co.nz/papers/tidy-data.html) `dplyr::tibble`.

Installation
------------

Install `biosystR` from GitHub:

``` r
# install.packages("devtools")
devtools::install_github("parksandwildlife/biosysR")
```

Setup
=====

Obtain a Biosys username and password and add to your `~/.Rprofile`:

``` r
Sys.setenv(BIOSYS_API_USERNAME = "USERNAME")
Sys.setenv(BIOSYS_API_PASSWORD = "PASSWORD")
```

Restart your R session to load the new environment variables. \#\# Usage example

TODO

Learn more
----------

See the vignette for in-depth examples of transforming, analysing and visualising data.

``` r
vignette("biosysR")
```

Contribute
==========

Every contribution, constructive feedback, or suggestion is welcome!

Send us your ideas and requests as [issues](https://github.com/parksandwildlife/biosysr/issues) or submit a pull request.

Pull requests should eventually pass tests and checks (not introducing new ERRORs, WARNINGs or NOTEs apart from the "New CRAN package" NOTE):

``` r
devtools::document(roclets=c('rd', 'collate', 'namespace', 'vignette'))
devtools::test()
devtools::check(check_version = T, force_suggests = T, cran = T)
covr::codecov()
```

To enable local testing of the API as well as checking and upload of test coverage, add these two lines with the respective tokens to your .Rprofile:

``` r
Sys.setenv(CODECOV_TOKEN = "my-codecov-token")
Sys.setenv(MY_API_TOKEN = "my-api-token")
```
