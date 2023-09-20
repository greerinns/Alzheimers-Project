# Analysis of Alzheimer’s Data Amongst Different Demographics in the US (Project 1, Group 5)

## Project Overview

**Project Code:**
   - Health_analysis-Final.ipynb
   - Alz_Mortality.ipynb
   - API_Attempt.ipynb (an attempt to use APIs in the future)
   
![Project Image](https://user-images.githubusercontent.com/125541671/233536834-88942bbf-8cc9-40bb-9030-44be811a1206.png)

This project centers around Alzheimer's disease and related dementias, with a primary objective of identifying trends and patterns in their prevalence and incidence. Additionally, the project explores potential risk factors and interventions that may help prevent or mitigate their impact in the United States.

## Research Questions

The project seeks to answer several key research questions:
1. Does physical activity prevent Alzheimer’s disease?
2. Does age affect the severity of Alzheimer’s?
3. Does gender have an effect on the prevalence of Alzheimer’s disease?
4. Is there significant variance in Alzheimer’s mortality between US regions?
5. What is the percentage increase in every US state between 2015-2020?
6. Is there a correlation between physical activity (sport complexes) and Alzheimer's disease per state?
7. Does a healthy diet (number of fast-food restaurants in a state) affect Alzheimer's disease?

## Data Sources

To address these research questions, the project relies on various datasets, including:
- Alzheimer’s and Aging data CSV
- Alzheimer’s mortality dataset
- Census.gov state regions data in CSV format
- Total population per state data

These datasets were compiled by the Centers for Disease Control and Prevention (CDC) and encompass data from national surveys such as the Behavioral Risk Factor Surveillance System (BRFSS), the National Health and Nutrition Examination Survey (NHANES), and the National Health Interview Survey (NHIS).

## Data Analysis Highlights

### Data Cleaning Challenge

One of the notable challenges encountered during data mining was that relevant data for hypothesis testing was hidden within two values in a column. The project addressed this challenge by filtering the data based on these two question-values and creating two additional columns from the existing one. These new columns, named "Poor Health" and "Inactive Days," were derived from the "Data_Value" column and used to answer a hypothesis-related question. A scatter plot of "Less Active - Poor Health" revealed a strong positive correlation between the number of inactive days and the percentage of people with Alzheimer's disease who reported poor health (correlation coefficient: 0.75). Furthermore, the p-value was less than 0.05, providing strong evidence against the null hypothesis.

### Age Group Testing

To test the hypothesis regarding age and Alzheimer's severity, the project filtered the dataset to select individuals aged 50-64 and 65+. As both "Poor Health" and "Age Group" are continuous variables, t-testing and box plotting were employed. The t-test yielded a significant result, indicating a statistically significant difference between the means of the two age groups.

### Gender and Alzheimer's Prevalence

The project also explored whether gender has an effect on Alzheimer's disease prevalence in the United States. Filtering the data allowed the separation of data by gender, and hypothesis testing was conducted. The results did not provide strong enough evidence to reject the null hypothesis, suggesting that there may not be a significant effect of gender on Alzheimer's disease cases.

### Regional Differences in Alzheimer's Mortality

The project conducted an in-depth analysis of Alzheimer's disease mortality rates across different US regions. A chi-square test was employed to determine whether there is a significant association between Age Group and States. The results indicated strong evidence to support the alternative hypothesis, suggesting that Alzheimer's disease mortality rates are region-dependent in the United States.

## Implications and Future Work

The findings of this project have significant implications for understanding Alzheimer's disease and its regional variations. Possible explanations for regional differences include lifestyle factors, environmental influences, and access to healthcare. Further research into specific contributing factors may inform future interventions.

A proposed future step in this project is the use of the Geo API to gather data on gyms and fast-food establishments across regions, providing additional insights into the factors contributing to regional variations in Alzheimer's disease.

In conclusion, this project provides valuable insights into Alzheimer's disease trends and potential influencing factors, with the potential to impact future research and interventions in this critical area of public health.
