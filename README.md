
<!-- README.md is generated from README.Rmd. Please edit that file -->

# CancerMutAnalyzer

Cancer Mutation Analysis and Visualization Suite.

<!-- badges: start -->
<!-- https://www.codefactor.io/repository/github/anjalisilva/testingpackage/issues -->

[![CodeFactor](https://www.codefactor.io/repository/github/martien2kk/CancerMutAnalyzer/badge)](https://www.codefactor.io/repository/github/martien2kk/CancerMutAnalyzer)
[![GitHub
issues](https://img.shields.io/github/issues/martien2kk/CancerMutAnalyzer)](https://github.com/martien2kk/CancerMutAnalyzer/issues)
[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)
![GitHub language
count](https://img.shields.io/github/languages/count/martien2kk/CancerMutAnalyzer)
![GitHub commit activity
(branch)](https://img.shields.io/github/commit-activity/y/martien2kk/CancerMutAnalyzer/master)

<!-- https://shields.io/category/license -->
<!-- badges: end -->

## Description

The `CancerMutAnalyzer` is an R package designed to streamline and
enhance the workflow for analyzing mutation data in cancer research. The
package focuses on processing, visualizing, and analyzing mutation
frequencies and genomic contexts, particularly targeting single
nucleotide polymorphisms (SNPs) and other mutation types within cancer
datasets. By providing functions for data extraction, filtering,
sequence analysis, and visualizations (such as heatmaps of mutation
frequencies), the package enables researchers to quickly identify
mutation patterns and genomic signatures associated with different
cancer types or tumor samples. <br> This package adds to the current
bioinformatics workflow by simplifying mutation analysis tasks that
typically require multiple steps across various software. By
centralizing these steps in one package, researchers can conduct
analyses more efficiently, reduce the risk of errors from file
conversions, and gain insights through streamlined visualizations. One
unique feature of this package is the ability to examine the local
nucleotide context surrounding mutations, which can be used to detect
mutational hotspots or enrich mutation data with GC content or
sequence-based patterns. Additionally, it addresses common issues such
as data formatting, base filtering, and customized visualization for
specific mutation characteristics, making it a comprehensive and
user-friendly tool for cancer genomics. <br> <br> <br> The
`CancerMutAnalyzer` package was developed using
`R version 4.4.1 (2024-06-14 ucrt)`, `Platform: x86_64-w64-mingw32/x64`
and `Running under: Windows 11 x64 (build 22631)`.

## Installation

Provide the following text and commands, customized to your R package.
E.g., <br> <br> <br> To install the latest version of the package:

``` r
install.packages("devtools")
library("devtools")
devtools::install_github("martien2kk/CancerMutAnalyzer", build_vignettes = TRUE)
library("CancerMutAnalyzer")
```

To run the Shiny app:

``` r
runTestingPackage() # not for Assessment 4; only for Assessment 5
```

## Overview

Provide the following commands, customized to your R package. Then
provide a list of user accessible functions within the package and a
brief description of each. Include one image illustrating the overview
of the package that shows the inputs and outputs. Ensure the image is
deposited in the correct location, as discussed in class. Point the user
to vignettes for a tutorial of your package. E.g., <br> <br> <br>

``` r
ls("package:CancerMutAnalyzer")
data(package = "CancerMutAnalyzer") 
browseVignettes("CancerMutAnalyzer")
```

`CancerMutAnalyzer` contains 3 functions.

1.  ***InfCriteriaCalculation*** for calculating information criteria
    given dataset dimensions, log-likelihood and probability.

2.  ***NormFactors*** for calculating normalization factors via via
    trimmed mean of M-values (TMM).

3.  ***InfCriteriaPlot*** for plotting information criteria values as a
    scatter plot.

The package also contains two RNA sequencing datasets, called GeneCounts
and GeneCounts2. Refer to package vignettes for more details. An
overview of the package is illustrated below.

![](./inst/extdata/SILVA_A_A1.png)

## Contributions

Provide a paragraph clearly indicating the name of the author of the
package and contributions from the author. Outline contributions from
other packages/sources for each function. Outline contributions from
generative AI tool(s) for each function. Include how the tools were used
and how the results from AI tools were incorporated. Remember your
individual contributions to the package are important. E.g., <br> <br>
<br>

The author of the package is Keren Zhang The author wrote the
*InfCriteriaCalculation* function, which calculates the information
criteria values given data specifications. Here, the Bayesian
information criterion (BIC), Akaike information criterion (AIC) and
Integrated Complete Likelihood (ICL) are calculated. The
*InfCriteriaCalculation* function makes use of map function from
`mclust` R package to generate information criteria values. The `stats`
R package is used for generating multinomially distributed random number
vectors. Part of the code for *InfCriteriaCalculation* function has been
taken from `<NamePackage>` R package. (Section of the borrowed code
should be clearly indicated and referenced in the InfCriteriaCalculation
R script). The *InfCriteriaPlot* is written by the author and generates
a plot of information criteria values. The *InfCriteriaPlot* function
makes use of the `graphics` R package. *NormFactors* is a function that
calculates normalization factors via Trimmed Mean of M-values (TMM).
*NormFactors* function uses Trimmed Mean of M-values (TMM) as
implemented in `edgeR` R package. No generative AI tools were used in
the development of this package.

## References

Provide full references for all sources used, including for the packages
and tools mentioned under ‘Contributions’, in one format. E.g., <br>
<br>

- Akaike, H. (1973). Information theory and an extension of the maximum
  likelihood principle. In *Second International Symposium on
  Information Theory*, New York, USA, 267–281. Springer Verlag.
  <https://link.springer.com/chapter/10.1007/978-1-4612-1694-0_15>.

- Biernacki, C., G. Celeux, and G. Govaert (2000). Assessing a mixture
  model for clustering with the integrated classification likelihood.
  *IEEE Transactions on Pattern Analysis and Machine Intelligence* 22.
  <https://hal.inria.fr/inria-00073163/document>

- BioRender. (2020). Image created by Silva, A. Retrieved October 30,
  2020, from <https://app.biorender.com/>

- Chang, W., J. Cheng, J. Allaire, C. Sievert, B. Schloerke, Y. Xie, J.
  Allen, J. McPherson, A. Dipert, B. Borges (2023). *shiny: Web
  Application Framework for R*. R package version 1.8.0,
  <https://CRAN.R-project.org/package=shiny>

- McCarthy, D. J., Y. Chen and G. K. Smyth (2012). Differential
  expression analysis of multifactor RNA-Seq experiments with respect to
  biological variation. *Nucleic Acids Research* 40. 4288-4297.
  <https://pubmed.ncbi.nlm.nih.gov/22287627/>

- R Core Team (2023). R: A language and environment for statistical
  computing. R Foundation for Statistical Computing, Vienna, Austria.
  <https://www.R-project.org/>

- Robinson, M. D., D.J. McCarthy and G. K. Smyth (2010). edgeR: a
  Bioconductor package for differential expression analysis of digital
  gene expression data. *Bioinformatics* 26, 139-140.
  <https://pubmed.ncbi.nlm.nih.gov/19910308/>

- Schwarz, G. (1978). Estimating the dimension of a model. *The Annals
  of Statistics* 6, 461–464.
  <https://projecteuclid.org/euclid.aos/1176344136>.

- Scrucca, L., M. Fop, T. B. Murphy and A. E. Raftery (2016) mclust 5:
  clustering, classification and density estimation using Gaussian
  finite mixture models. *The R Journal* 8(1), 289-317.
  <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5096736/>

- Wickham, H. ggplot2: Elegant Graphics for Data Analysis.
  Springer-Verlag New York, 2016.

- Wickham, H. and J. Bryan (2019). *R Packages* (2nd edition). Newton,
  Massachusetts: O’Reilly Media. <https://r-pkgs.org/>

## Acknowledgements

Provide the following text, customized to your R package. E.g., <br>
<br> <br> This package was developed as part of an assessment for 2024
BCB410H: Applied Bioinformatics course at the University of Toronto,
Toronto, CANADA. `CancerMutAnalyzer` welcomes issues, enhancement
requests, and other contributions. To submit an issue, use the [GitHub
issues](https://github.com/martien2kk/CancerMutAnalyzer/issues). Many
thanks to those who provided feedback to improve this package.

## Package Structure

The package structure is illustrated below: <br> <br> The package tree
structure is provided below.

``` r
- TestingPackage
  |- TestingPackage.Rproj
  |- DESCRIPTION
  |- NAMESPACE
  |- LICENSE
  |- README
  |- data
    |- GeneCounts.rda
    |- GeneCounts2.rda
  |- inst
    CITATION
    |- extdata
      |- SILVA_A_A1.png
      |- GeneCountsData2.csv
    |- shiny-scripts 
        |- app.R
  |- man
    |- GeneCounts.Rd
    |- InfCriteriaCalculation.Rd
    |- NormFactors.Rd
    |- InfCriteriaPlot.Rd
  |- R
    |- data.R
    |- InfCriteriaCalculation.R
    |- InfCriteriaPlot.R
    |- NormFactorCalculation.R
  |- vignettes
    |- TestingPackageVignette.Rmd
  |- tests
    |- testthat.R
    |- testthat
      |- test-InfCriteriaCalculation.R
```
