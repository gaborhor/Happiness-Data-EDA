# Happiness-Data-EDA
Introductory-level EDA on UN World Happiness Report and World Bank Metrics from 2019

## Project Notes
This EDA was performed as part of a group project for a course on Probability and Statistics as part of
a Masters of Data Science at Denver University. It was a fully collaborative effort with classmates
Don Smith and Brittany Laurent, and results and approaches were reviewed regularly amongst ourselves
and our class supervisor.

## My Role
My primary contributions to this project were code implementation of Shapiro-Wilk testing, Q-Q Plots, Levene
Testing, and Principal Component Analysis, as well as final decisions on the communication of results and data.

## File Glossary:

happy_data_augment.csv:

  Country-indexed data from 2019 UN World Happiness Report, augmented with 2019 World Bank Metrics

gh_happiness_data_EDA.rmd, .pdf:

  R-markdown file with code and explanation of entire EDA process

PCAbiplot.png:

  Separate file of "most descriptive" interrelation between predictive variables in our data

## Data Glossary
* "country_name"
* "country_code"
* "region"

* “happy_rank” - Ranking of happiness score
* “happy_score” - Aggregate happiness score calculated from all other factors
* “happy_gdpc” - GDP per capita
* “happy_supp” - Sense of social support
* “happy_health” - Healthy life expectancy at birth
* “happy_free” - Happiness with level of personal freedom
* “happy_gen” - How often people contribute to charitable causes
* “happy_trust” - Trust level that own national government is not corrupt
* “wb_pov” - % of population below UN international poverty rate
* “wb_unemp” - % of able-bodied labor force unemployed
* “wb_elec” - % of population with access to electricity
* “wb_renew” - % of final energy use from renewable sources
* “wb_hom” - Homicide rate per 100,000 people
* “wb_debt” - National debt as % of government GDP
* "gdpc_change" - Synthetic variable constructed from comparison of UN World Happiness Report 2018 and 2019 GPDC data

## Glossary of Exploratory Approaches
* Studentized Breusch-Pagan Test for Heteroscedasticity of predictor variables
* Shapiro-Wilk Test and Q-Q Plotting for Normality of predictor variables
* Decile-level value imputation
* Pairwise correlation matrix against 'happy_score'
* Shapiro-Wilk Test and Levene Test of 'happy_score'for Normality and Homogeneity of Variance against 'region' info
* One-Way ANOVA of 'happy_score' against 'region'
* Tukey Honest-Significant-Difference Test on all ANOVA results
* Robust Regression Testing via Maximum Likelihood-type M-Estimation (chosen due to conditions of Ordinary-Least-Squares regression not being met)
* Principal Component Analysis (PCA)
