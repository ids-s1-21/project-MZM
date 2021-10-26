# Happy Planet Index data

This data file is 14 x 140, it has 14 variables and 140 observations

## happy_planet_index.xlsx

- `hpi_rank`: The rank each country got in the happy planet index.
- `country`: The country to which the observations relate.
- `region`: The region of the world the country is located in.
- `avg_life_exp`: Average life expectancy for the country.
- `avg_wellbeing`: Average wellbeing reported by the citizens of a country, measured through a survey in which people ranked their wellbeing from 1 to 10.
- `happy_life_years`: A metric used to combine average life expectancy and average wellbeing, calculated as follows: (avg_life_exp * avg_wellbeing / 10).
- `footprint`: The average amount of landed required for a countries consumption per capita, includes the area: to absorb CO2 emmisions, provide renewable resources like food, and occupied by infrastructure (gha = global hectares).
- `inequality_outcome`: A measure to illustrate the impact of inequalities in life expectancy and wellbeing expressed as a percentage in decimal, the higher the decimal the more impactful the inequalities are in a country.
- `inequality_life_exp`: The mean life expectancy of a country adjusted for inequality in life expectancy distribution, using the Atkinson Index.
- `inequality_wellbeing`: The mean reported wellbeing of a country adjusted for inequality in wellbeing distribution, using the Atkinson Index.
- `hpi`: The happy planet index for a country, calculated as follows: (happy_life_years * inequality_outcome / footprint).
- `gdp_capita`: Gross Domestic Product per cpaita of a country.
- `pop`: A country's population.
- `gini_index`: Index representing wealth inequality within a country (higher the value, higher the inequality).
