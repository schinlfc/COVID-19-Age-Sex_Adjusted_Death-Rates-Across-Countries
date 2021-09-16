# COVID-19-Age-Sex_Adjusted_Death-Rates-Across-Countries
This project tries to investigate how each country performances in regards to COVID-19.

### I came up with a way to measure performance metric with this simple exercise.

Step 1: Download age- and sex-specific population counts by country in 2020 from https://www.census.gov/data/developers/data-sets/international-database.html

Step 2: Get  age- and sex-specific infection fatality ratio estimates by COVID from this published paper -- https://www.nature.com/articles/s41586-020-2918-0

Step 3: Multiply the age- and sex-specific infection fatality ratio estimates by age- and sex-specific population counts. This will deliver expected deaths from COVID by age and sex

Step 4: Sum age- and sex-specific death count from COVID

Step 5: Divide expected count of death by COVID over the the population to get age- and sex-adjusted expected COVID death rate

Step 6: Get the most recent observed death rates by country from this link -- https://github.com/owid/covid-19-data/blob/master/public/data/README.md

Step 7: Regress the following equation:

Observed death rates = B0 + B1*Age-sex adjusted
                            expected death rates + Epsilon

Step 8: Derive the standardized residuals from Step 7. This will be a metric for performance

Step 9: Plot the standardized residuals against age- and sex-adjusted expected death rates
