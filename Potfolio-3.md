Portfolio 3: Preparing Dataset
================

The goal of this and the proceeding portfolio pieces will be to rerun my
thesis project using R. Therefore, this first project will detail the
steps to transform the the .sav datasets I used in SPSS to .rds files.

``` r
library(haven) # necessary to read SPSS .sav files
library(readxl) # to read excel files

thesis_data <- read_sav("main_analysis_data.sav")

secondary_data <- read_sav("exploratory_data.sav")

life_event_data <- read_sav("life_event_prescreen.sav")

demographic_data <- read_excel("demographic_data.xlsx")
```

    ## New names:
    ## • `` -> `...7`
    ## • `` -> `...8`
    ## • `` -> `...9`
    ## • `` -> `...10`
    ## • `` -> `...11`
    ## • `` -> `...12`
    ## • `` -> `...13`

## Exploring the Data

``` r
saveRDS(thesis_data, "thesis_data.rds")
saveRDS(secondary_data, "secondary_data.rds")
saveRDS(life_event_data, "life_event_data.rds")
saveRDS(demographic_data, "demographic_data.rds")
```

Okay now that all the data looks good and has been saved in a .rds
format I should be able to rerun all the thesis analyses in Rstudio!
