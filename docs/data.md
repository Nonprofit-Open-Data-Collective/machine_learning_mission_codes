---
title: "Data"
---

Some info about data sources...


## Import from GitHub

We have both CSV (comma separated values) and RDS (R data set) files available for many of the datasets. 

Read CSV version:

```r
dat <- read.csv( "https://github.com/Nonprofit-Open-Data-Collective/machine_learning_mission_codes/blob/master/DATA/MISSION.csv?raw=true", stringsAsFactors=F )
```

Read RDS version:

```r
dat <- readRDS( gzcon( url( "https://github.com/Nonprofit-Open-Data-Collective/machine_learning_mission_codes/blob/master/DATA/MISSION.rds?raw=true" )))
```
