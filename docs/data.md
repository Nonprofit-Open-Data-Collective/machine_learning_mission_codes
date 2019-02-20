---
title: "Data"
---

The goal of this project is to create a training dataset that can serve as a reference point for performance of program activity classification algorithms that rely on the types of text that would be readily available on websites, grant aplications, tax forms, or annual reports.

The creation of a reference dataset allows for innovation and progress since the relative performance of algorithms can be compared when they are applied to the same dataset. Performance metrics are difficult to interpret if they are drawn from different underlying data sources. 

The field of social network analysis provides some examples of this approach by benchmarking the performance of clustering algorithms using a small set of canonical datasets. 

Agarwal, G., & Kempe, D. (2008). Modularity-maximizing graph communities via mathematical programming. The European Physical Journal B, 66(3), 409-418. [PAPER](https://arxiv.org/pdf/0710.2533.pdf)



## Raw Data Sources

We have built a training dataset using data from two primary sources:

The IRS E-File database contains machine-readable text fields on nonprofit names, mission statements, and program service accomplishments. 

The IRS 1023-EZ files contain mission taxonomy codes for the traditional National Taxonomy of Exempt Entities (NTEE), as well as eight binary mission codes related to nonprofit purpose such as religious activities, scientific activities, recreational activities, or welfare activities. 

See the [taxonomy](https://nonprofit-open-data-collective.github.io/machine_learning_mission_codes/taxonomies/) section of this site for more information. 



## Available Mission and Activity Text

Text-based data describing nonprofit activities.

* Nonprofit name: Form 990 and 990-EZ, header
* Nonprofit missions on IRS forms: Form 990, Part I, Line 1; Form 990-EZ, Part III, Line 0
* Program service accomplishments: Form 990, Part III; Form 990-EZ, Part III



# Overview of the Training Dataset

How was sample created, what it represents, why a test sample is useful for benchmarking and replication.

Garbage in garbage out discussion: 
* quality of program / mission descriptions 
* quality of activity codes 

See the [Taxonomy](https://nonprofit-open-data-collective.github.io/machine_learning_mission_codes/taxonomies/) section for activity codes.

IRS versus human coding...(validity and reliability of taxonomies)



# Read Data from GitHub

We have both CSV (comma separated values) and RDS (R data set) files available for many of the datasets in the [DATA](https://github.com/Nonprofit-Open-Data-Collective/machine_learning_mission_codes/tree/master/DATA) section of this repository. 

Read CSV version:

```r
dat <- read.csv( "https://github.com/Nonprofit-Open-Data-Collective/machine_learning_mission_codes/blob/master/DATA/MISSION.csv?raw=true", stringsAsFactors=F )
```

Read RDS version:

```r
dat <- readRDS( gzcon( url( "https://github.com/Nonprofit-Open-Data-Collective/machine_learning_mission_codes/blob/master/DATA/MISSION.rds?raw=true" )))
```

<br> 
<br> 

-------------------

# Raw Mission Data 

The nonprofit mission data comes from the new IRS e-file data available on AWS as XML files. 

```r
library( xmltools )
library( purrr )
library( xml2 )
library( dplyr )

# source build functions
source( "https://raw.githubusercontent.com/Nonprofit-Open-Data-Collective/irs-990-efiler-database/master/BUILD_SCRIPTS/build_efile_database_functions.R" )

dat <- buildIndex()
table( dat$FormType, dat$TaxYear )
```

|      |  2009|   2010|   2011|   2012|   2013|   2014|   2015|   2016|  2017|
|:-----|-----:|------:|------:|------:|------:|------:|------:|------:|-----:|
|990   | 33,360| 123,107| 159,539| 179,674| 198,738| 218,614| 232,975| 214,585| 25,921|
|990EZ | 15,500|  63,253|  82,066|  93,769| 104,538| 116,461| 124,507| 121,530| 28,767|
|990PF |  2,352|  25,275|  34,597|  39,936|  45,897|  53,443|  58,724|  60,305| 20,608|


## XML Tools in R

If you want to work with the data directly you will need to use some XML tools. 

[Quick Guide to Working with XML in R](Quick_Guide_to_XML_in_R.html)

## Build Custom Databases

You can build custom datasets from the IRS XML fields. Some sapmle scripts are available here:

[Nonprofit Open Data Collective](https://github.com/Nonprofit-Open-Data-Collective/irs-990-efiler-database/blob/master/BUILD_SCRIPTS/README.md)

And many of the tables in CSV formats are available on our [Data World](https://data.world/activity/npdata) group: https://data.world/activity/npdata
