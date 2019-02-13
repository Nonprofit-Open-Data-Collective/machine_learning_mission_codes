---
title: "Data"
---

Some info about data sources...

IRS E-File Data

IRS 1023-EZ Files

# Available Activity Data

Text-based data describing nonprofit activities.

* Nonprofit missions on IRS forms (e-file database)
* Program service accomplishments (e-file database)
* We

# Available Activity Codes

See the [Taxonomy](https://nonprofit-open-data-collective.github.io/machine_learning_mission_codes/taxonomies/) section.


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
