# Group-5-Project

Data mining for this project was challenging. The data related to the hypothesis was hidden under two values in a column. The data Frame was filtered by those two question-values, then two more columns were created from the existing one.
Those columns are derived from the column called “Data_Value”. The values of one of them contains info about mean number of days with activity limitations, the values of the second column contain info about percentage of older adults who self-reported that their health is "fair" or "poor".
The names of these columns come from the unique values of the filtered column called “Question”. Columns are renamed as “Poor Health” and “Inactive Days”.
“Poor Health” and “Inactive Days” columns are there to answer one of the questions related the hypothesis.
Question:    “Does physical activity prevent Alzheimer’s disease?”
Null Hypothesis:   “The well-being of physically inactive patients (with AD) stays the same or gets better.
 Alternative hypothesis: “The well-being of physically inactive patients (with AD) gets worse.”
“Less Active - Poor Health” scatter plot shows that when the number of inactive days increases the percentage of people (with Alzheimer’s) with poor health also increases.
The correlation coefficient is 0.75 (the R-value is close to 1) which means there is a strong correlation between inactive days and poor health.
The probability (P-value) value is less than 0.05 which is strong evidence against the null hypothesis. (edited) 

Alz Mortality Dataset Summary:
ETL
The project involved cleaning and merging data from two CSV files on state regions and Alzheimer's disease mortalities across five years by state.
Rows were dropped and renamed, and merging was successful on the state column using inner join.
Aggregate mean mortality rates were taken while grouping within region and then year.
Hypothesis
The hypothesis tested was that the mortality rates of Alzheimer's disease in the United States are region-dependent.
Regional differences in Alzheimer's disease mortality refer to the variations in the number of Alzheimer's disease deaths across different regions in the United States, specifically in this presentation looking at Midwest, Northeast, South, and West.
There is strong evidence to support the alternative hypothesis that Alzheimer's disease mortality rates are region-dependent in the United States.
We summarized the data of the regional mortality rate averages over the course of 2015 to 2020 into a box and whisker plot
Results from the Anova Test: P-Value = 3.75e-12, <.05, supporting the alternative hypothesis
Possible explanations for regional differences include differences in lifestyle factors such as diet and exercise, as well as variations in environmental factors such as air pollution or access to healthcare.
Implications
As the alternative hypothesis suggests, there may be important implications for understanding the underlying causes of Alzheimer's disease and developing effective prevention and treatment strategies.
This could lead to further research into the specific factors that contribute to the regional differences in Alzheimer's disease mortality rates in the United States.
API Slide
To further investigate the specific factors contributing to regional differences, the use of the Geo API to collect data about gyms and fast food across these regions was proposed.
Due to API limitations, the approach would require splitting up cities in calls, scaling that out to states, and then eventually regions, to encompassing the entire US.
If explored in the future, the approach would start with very small radii rather than state-sized radii to avoid hitting the 500 feature limit.
(edited)
.DS_Store