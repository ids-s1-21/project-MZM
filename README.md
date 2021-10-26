Project title
================
by MZM

## Summary

In our project we aim to show how different countries compare against
one another in multiple variables, one of which being the ‘Happy Planet
Index’. This will help us understand which regions or countries are able
to provide a good living standard while also having a healthy
environmental footprint. Our data is from a data set named the ‘Happy
Planet Index’ which has taken most countries and used their social
happiness, environmental impact and also inequalities and differences of
the countries people. Some important variables to know are the ‘Happy
Planet Index’ which is a combination of a countries inequalities of
living, their environmental impact and their peoples happiness. ‘Happy
Life Years’ is the amount of years a person can expect to be enjoyable
and less stressful in the given country. ‘Inequality adjusted life
expectancy’ is life expectancy but is when you take in to account the
different living standards of different groups, different incomes,
different ethnicity and others. The data set was compiled using many
open polls and data sets from the UN, York University and others.

We have analysed our data through three categories: geographic, economic
and mental health. The first category contains variables population,
ecological footprint and location (continent). Our second category
compares values using variables average well-being,happy life
years,inequality of outcomes, inequality-adjusted life expectancy, and
inequality-adjusted well-being.

We will examine the changes within these three categories through years
2015 to 2020 and compare specifically years 2015-2019 and 2020 to
understand the effects of the pandemic on the countries’ happy planet
indexes.

Write-up of your project and findings go here. Think of this as the text
of your presentation. The length should be roughly 5 minutes when read
out loud. Although pacing varies, a 5-minute speech is roughly 750
words. To use the word count addin, select the text you want to count
the words of (probably this is the Summary section of this document, go
to Addins, and select the `Word count` addin). This addin counts words
using two different algorithms, but the results should be similar and as
long as you’re in the ballpark of 750 words, you’re good! The addin will
ignore code chunks and only count the words in prose.

You can also load your data here and present any analysis results /
plots, but I strongly urge you to keep that to a minimum (maybe only the
most important graphic, if you have one you can choose). And make sure
to hide your code with `echo = FALSE` unless the point you are trying to
make is about the code itself. Your results with proper output and
graphics go in your presentation, this space is for a brief summary of
your project.

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

    ## Rows: 152
    ## Columns: 11
    ## $ hpi_rank                      <dbl> 1, NA, 3, 8, 2, 6, 10, 4, 9, NA, 12, 21,…
    ## $ country                       <chr> "Costa Rica", "Vanuatu", "Colombia", "Sw…
    ## $ iso                           <chr> "CRI", "VUT", "COL", "CHE", "ECU", "PAN"…
    ## $ continent                     <dbl> 1, 8, 1, 3, 1, 1, 1, 1, 1, 1, 2, 8, 1, 3…
    ## $ population_thousands          <dbl> 4899.336, 278.326, 48175.048, 8379.915, …
    ## $ life_expectancy_years         <dbl> 79.7, 70.0, 76.7, 83.3, 76.4, 78.0, 74.2…
    ## $ ladder_of_life_wellbeing_0_10 <dbl> 7.135618, 6.712810, 6.233715, 7.458520, …
    ## $ ecological_footprint_g_ha     <dbl> 2.7101425, NA, 2.0414124, 4.6007449, 1.6…
    ## $ hpi                           <dbl> 62.37983, NA, 58.14679, 56.11938, 59.532…
    ## $ biocapacity_for_year_g_ha     <dbl> 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, 1.6, …
    ## $ gdp_per_capita                <chr> "19211.566759340509", "3061.787239836667…

## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Include a citation for your data here. See
<http://libraryguides.vu.edu.au/c.php?g=386501&p=4347840> for guidance
on proper citation for datasets. If you got your data off the web, make
sure to note the retrieval date.

## References

List any references here. You should, at a minimum, list your data
source.
