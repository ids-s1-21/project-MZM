Project_Research
================
MZM
24/11/2021

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.1 ──

    ## ✓ ggplot2 3.3.5     ✓ purrr   0.3.4
    ## ✓ tibble  3.1.3     ✓ dplyr   1.0.7
    ## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
    ## ✓ readr   2.0.0     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

    ## 
    ## Attaching package: 'janitor'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     chisq.test, fisher.test

``` r
tidy_name_year <- function(data, year_no){
  data <- data %>%
    clean_names() %>%
    mutate(year = year_no)
  return(data)
}

tidy_append_data <- function(data1, data2, data3, 
                             data4, data5){
  data <- bind_rows(data1, data2)
  data <- bind_rows(data, data3)
  data <- bind_rows(data, data4)
  data <- bind_rows(data, data5)
  
  data <- data %>%
  rename("pop_1000s"     = population_thousands,
         "life_exp"      = life_expectancy_years,
         "wellbeing"     = ladder_of_life_wellbeing_0_10,
         "eco_footprint" = ecological_footprint_g_ha,
         "biocapacity"   = biocapacity_for_year_g_ha,
         "gdp"           = gdp_per_capita,
         "region"        = continent) %>%
  transform(gdp = as.numeric(gdp))
}
```

``` r
hpi_2016 <- read_excel("/cloud/project/data/hpi_2016_data.xlsx")
hpi_2017 <- read_excel("/cloud/project/data/hpi_2017_data.xlsx")
hpi_2018 <- read_excel("/cloud/project/data/hpi_2018_data.xlsx") 
hpi_2019 <- read_excel("/cloud/project/data/hpi_2019_data.xlsx")
hpi_2020 <- read_excel("/cloud/project/data/hpi_2020_data.xlsx")

hpi_2016 <- tidy_name_year(hpi_2016, 2016)
hpi_2017 <- tidy_name_year(hpi_2017, 2017)
hpi_2018 <- tidy_name_year(hpi_2018, 2018)
hpi_2019 <- tidy_name_year(hpi_2019, 2019)
hpi_2020 <- tidy_name_year(hpi_2020, 2020)

hpi_data <- tidy_append_data(hpi_2016, hpi_2017, hpi_2018, 
                             hpi_2019, hpi_2020)
```

    ## Warning in eval(substitute(list(...)), `_data`, parent.frame()): NAs introduced
    ## by coercion

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

You can also embed plots, for example:

![](Project_Research_files/figure-gfm/pressure-1.png)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
