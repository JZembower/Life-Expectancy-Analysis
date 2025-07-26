# Assessing the Predictability of Life Expectancy

This project investigates the factors influencing life expectancy across various countries using a comprehensive dataset from the World Health Organization (WHO) and United Nations (UN). The goal is to identify key predictor variables and understand their relationship with life expectancy, both for a single year and over a multi-year period.

## Authors

Jonah Zembower, Ben Nicholson, Andrew Smith, Maria Morales Laguarda

## Date

December 11, 2024

## Project Overview

The project aims to determine if various socio-economic, health, and demographic variables can effectively predict the life expectancy of a given country. It involves extensive data analysis, hypothesis testing, and the application of multiple linear regression and non-parametric statistical methods.

## Data

The primary dataset used is `Life Expectancy Data.csv`, which includes data from 2000 to 2015 for 183 countries. A subset of this data for the year 2015 is also available as `2015_data.csv`. The dataset comprises 20 predictor variables related to:

* **Mortality Rates**: Adult Mortality, infant deaths, under-five deaths.
* **Disease Rates**: Hepatitis B, Measles, Polio, Diphtheria, HIV/AIDS.
* **Health and Lifestyle**: Alcohol, BMI, thinness (1-19 years, 5-9 years).
* **Economic Factors**: Percentage expenditure, Total expenditure, GDP, Income composition of resources.
* **Demographics**: Population, Schooling.
* **Country Status**: Status (Developing/Developed).

Missing data was observed, particularly in lesser-known countries.

## Exploratory Data Analysis (EDA)

Initial data exploration involved:

* **Correlation Matrix**: Visualizing the relationships between all variables, revealing both positive and negative correlations, some of which were strong.
* **Pairplots**: Showcasing the individual relationships between each variable, highlighting varying strengths of association.
* **Life Expectancy Distributions**: Analyzing the distribution of life expectancy, with a median of approximately 74 years, and assessing for potential non-normality.
* **Outlier Detection**: Identifying outliers in the data.

## Hypothesis Testing

The central hypothesis explored was:

* **Null Hypothesis (H0)**: No variables can aid in the prediction of life expectancy for a given country.
* **Alternative Hypothesis (HA)**: There are some variables that can predict life expectancy for a given country.

Statistical significance was found for several predictor variables in relation to life expectancy.

## Modeling Approaches

### Multiple Linear Regression

Multiple linear regression models were built to predict life expectancy, for both the 2015 data and the entire 2000-2015 dataset.

* **Assumptions**: The regression models generally followed the assumptions of linearity and normality of residuals. However, assumptions of homoscedasticity (constant variance of residuals) and the absence of influential points were rejected, indicating areas for potential model refinement.
* **Key Predictors (2015 data)**: Under-five deaths, HIV/AIDS, and Income composition of resources were identified as effective predictors.
* **Key Predictors (2000-2015 data)**: Polio vaccination rates, Diphtheria vaccination rates, HIV/AIDS prevalence, GDP, thinness among 5-9 year olds, Income Composition of Resources, and Schooling were found to be effective long-term predictors.

### ANOVA of Continents

An ANOVA (Analysis of Variance) test was performed by grouping countries into continents to assess if there were statistically significant differences in life expectancy values across continents. Significant differences were indeed found.

### Non-Parametric Tests

Complementary non-parametric tests were conducted to further explore statistical differences:

* **Kruskal-Wallis Test**: Indicated a statistically significant difference in life expectancy across all continents.
* **Mann-Whitney U Test**: Found statistically significant differences in life expectancy in most paired continental comparisons (e.g., Asia vs. Europe, Asia vs. Africa, Europe vs. Africa).
* **Chi-squared Test for Independence**: Showed that the continent variable was statistically different from the "is developed" status variable.

## Conclusion

The project successfully demonstrated that various predictor variables related to health, economics, and demographics are statistically significant in predicting life expectancy. While the regression models largely met linearity and normality assumptions, challenges with homoscedasticity and influential points were noted. Crucially, significant disparities in life expectancy were identified across continents. The analysis supports the ability to predict life expectancy with high accuracy for both a single year and over a range of years.

## Future Study

* **New Variables**: Incorporate additional variables related to life expectancy and quality of living that were not included in this dataset.
* **Other Predictions**: Explore predicting other variables from the dataset, such as Population or GDP.
* **Recent Data Analysis**: Assess more recent data, especially considering the impact of global events like COVID-19 on life expectancy.
* **Further ANOVA Analysis**: Conduct more in-depth ANOVA analysis to understand how other variables relate across different continents.

## Technologies Used

The project was developed in Python and utilized the following libraries:

* **pandas**: For data manipulation and analysis.
* **matplotlib.pyplot** & **seaborn**: For data visualization.
* **numpy**: For numerical operations.
* **statsmodels.api**: For statistical modeling, particularly multiple linear regression.
* **scipy.stats**: For non-parametric statistical tests.

## Files in the Repository

* `Life Expectancy Data.csv`: The complete dataset containing life expectancy and related variables from 2000-2015.
* `2015_data.csv`: A subset of the main dataset, specifically for the year 2015.
* `Final_Project.ipynb`: The Jupyter Notebook containing all the code for data loading, preprocessing, EDA, hypothesis testing, statistical modeling, and visualization.
* `Final Project Report.docx`: A detailed report outlining the project's methodology, findings, and conclusions.
* `Final Project.pptx`: A presentation summarizing the project for an audience.
