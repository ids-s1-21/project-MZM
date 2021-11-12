Project proposal
================
MZM

``` r
library(tidyverse)
library(broom)
library(readxl)
library(janitor)
library(scales)
```

## 1. Introduction

In our project we aim to show how different countries compare against
one another in multiple variables, one of which being the ‘Happy Planet
Index’. This will help us understand which regions or countries are able
to provide a good living standard while also having a healthy
environmental footprint. Our data is from a data set named the ‘Happy
Planet Index’ which has taken most countries and used their social
happiness, environmental impact and also inequalities and differences of
the countries people. Some important variables to know are the ‘Happy
Planet Index’ which is a combination of a countries inequalities of
living, their environmental impact and their peoples happiness. ‘Eco
Footprint’ is the average demand for the natural resources of the
environment, so how much land and resources would be needed to sustain
the country. ‘Biocapacity’ is the average wellbeing reported by the
citizens of a country, measured through a survey in which people ranked
their wellbeing from 1 to 10. The data set was compiled using many open
polls and data sets from the UN, York University and others.

## 2. Data

    ## Warning in eval(substitute(list(...)), `_data`, parent.frame()): NAs introduced
    ## by coercion

``` r
glimpse(hpi_data)
```

    ## Rows: 760
    ## Columns: 12
    ## $ hpi_rank      <dbl> 1, NA, 3, 8, 2, 6, 10, 4, 9, NA, 12, 21, 13, 23, 20, 7, …
    ## $ country       <chr> "Costa Rica", "Vanuatu", "Colombia", "Switzerland", "Ecu…
    ## $ iso           <chr> "CRI", "VUT", "COL", "CHE", "ECU", "PAN", "JAM", "GTM", …
    ## $ region        <chr> "Latin America", "East Asia", "Latin America", "Western …
    ## $ pop_1000s     <dbl> 4899.336, 278.326, 48175.048, 8379.915, 16491.116, 4037.…
    ## $ life_exp      <dbl> 79.7, 70.0, 76.7, 83.3, 76.4, 78.0, 74.2, 73.5, 74.7, 77…
    ## $ wellbeing     <dbl> 7.135618, 6.712810, 6.233715, 7.458520, 6.115438, 6.1176…
    ## $ eco_footprint <dbl> 2.7101425, NA, 2.0414124, 4.6007449, 1.6910607, 2.260211…
    ## $ hpi           <dbl> 62.37983, NA, 58.14679, 56.11938, 59.53255, 56.93162, 55…
    ## $ biocapacity   <dbl> 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1…
    ## $ gdp           <dbl> 19211.567, 3061.787, 14242.807, 66344.075, 11551.617, 29…
    ## $ year          <dbl> 2016, 2016, 2016, 2016, 2016, 2016, 2016, 2016, 2016, 20…

``` r
hpi_data %>%
  ggplot(aes(x = year, y = wellbeing, group = year)) +
  geom_violin(trim = FALSE) +
  facet_wrap(~region) +
  labs(
    title = "Wellbeing around the world",
    subtitle = "Over time",
    x = "Years",
    y = "Wellbeing measure"
  )
```

    ## Warning: Removed 75 rows containing non-finite values (stat_ydensity).

![](proposal_files/figure-gfm/wellbeing-time%20plot-1.png)<!-- -->

``` r
hpi_data %>%
  ggplot(aes(x = gdp, y = life_exp, colour = region)) +
  geom_point() +
  facet_wrap(~year) +
  labs(
    title = "GDP and life expectancy around the world",
    subtitle = "Over time",
    x = "GDP per capaita (in thousands)",
    y = "Life expectancy",
    region = "Region"
  ) +
  theme(legend.position = "bottom") +
  scale_x_continuous(labels = label_dollar(scale = 0.001,
                                           prefix = "$",
                                           suffix = "K"))
```

    ## Warning: Removed 167 rows containing missing values (geom_point).

![](proposal_files/figure-gfm/gdp-life_exp%20plot-1.png)<!-- -->

``` r
hpi_data %>%
  ggplot(aes(x = eco_footprint, fill = region)) +
  geom_histogram() +
  facet_wrap(~region) +
  labs(
    title = "Ecological footprint of countries",
    subtitle = "Faceted by region",
    x = "Ecological footprint (in global hectares)",
    y = "Number of countries"
  ) +
  theme(legend.position = "none")
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

    ## Warning: Removed 48 rows containing non-finite values (stat_bin).

![](proposal_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

## 3. Data analysis plan

We have analysed our data through three categories: geographic, economic
and mental health. The first category contains variables population,
ecological footprint and location (continent). Our second category
compares values using variables average well-being,happy life
years,inequality of outcomes, inequality-adjusted life expectancy, and
inequality-adjusted well-being.

We will examine the changes within these three categories through years
2016 to 2020 and compare specifically years 2016-2019 and 2020 to
understand the effects of the pandemic on the countries’ happy planet
indexes.

Method: We are planning on taking the average of values of data tables
from years 2016 to 2019 and creating another table. Comparing the new
data frame, containing the averages of all values for the necessary
variables, with values of 2020 will give us a more reliable
difference/change due to the pandemic. Our analysis will contain three
graphs (one for each category) with all the necessary variables.

Conclusion: We expect decrease in mental health and economic factors due
to the pandemic.
