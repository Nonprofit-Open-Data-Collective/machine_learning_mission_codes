---
title: "R Packages"
---


## Installing Packages

```r
install.packages( c( "quanteda", "purrr", "xml2", "dplyr", "XML", "jsonlite" ) )
devtools::install_github( 'ultinomics/xmltools' )
library( xmltools )
library( purrr )
library( xml2 )
library( dplyr )
library( XML )
library( jsonlite )
```



## Package Descriptions

We used the following R packages for analysis:

**quanteda**: Quantitative Analysis of Textual Data [ [documentation](https://quanteda.io/index.html) ]



## Raw Mission Data 

The nonprofit mission data comes from the new IRS e-file data dump on AWS. If you want to work with the data directly you will need to use some XML tools. 

[Quick Guide to Working with XML in R](Quick_Guide_to_XML_in_R.html)


