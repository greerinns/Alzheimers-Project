# Group-5-Project
#Title
#Association of Alzheimer’s disease and Healthy aging data with demographic parameters in the US.
#Team members: Greer Inns, Nazeli Mnatsakanyan, Noureddine Belhaj Harman Malhi, Stelios Kosmidis
#Project description outline: 
As populations become increasingly aged, Alzheimer’s disease became more prevalent. The primary focus of this study is on Alzheimer's #disease and related dementias, including prevalence, incidence, risk factors, and outcomes. The data can be used to identify trends and patterns in the prevalence #and incidence of these conditions, as well as to explore potential risk factors and interventions that may help to prevent or mitigate their impact in the U.S

Research
We tried to answer specific research questions:
-Does physical activity prevent Alzheimer’s disease?
-Does age affect Alzheimer’s severity?
-Is there a gender prevalence of Alzheimer’s disease ?(Women vs Men)
-Is there any US region with higher rates of Alzheimer’s disease cases?
-What is the % increase in every US state between 2015-2020?
We also speculate for the use of these database in conjunction with future ones:
-What is the correlation between physical activity (sport complexes) and AD per state?
-Does healthy diet (number of fast-food restaurants in a state) affect AD?


We used the  Datasets decribed below:
- https://www.kaggle.com/datasets/ananthu19/alzheimer-disease-and-healthy-aging-data-in-us (Alzheimer’s’ and Aging data CSV)  (States). The dataset was compiled by the Centers for Disease Control and Prevention (CDC) and includes data from several national surveys, including the Behavioral Risk Factor Surveillance System (BRFSS), the National Health and Nutrition Examination Survey (NHANES), and the National Health Interview Survey (NHIS).
-Census.gov. Total population per state

DTL

First:Data mining for this project was challenging. The data related to the hypothesis was hidden under two values in a column. The data Frame was filtered by those two question-values, then two more columns were created from the existing one.
Those columns are derived from the column called “Data_Value”. The values of one of them contains info about mean number of days with activity limitations, the values of the second column contain info about percentage of older adults who self-reported that their health is "fair" or "poor".
The names of these columns come from the unique values of the filtered column called “Question”. Columns are renamed as “Poor Health” and “Inactive Days”.
“Poor Health” and “Inactive Days” columns are there to answer one of the questions related the hypothesis.

Second: The project involved cleaning and merging data from two CSV files on state regions and Alzheimer's disease mortalities across five years by state.
Rows were dropped and renamed, and merging was successful on the state column using inner join.
Aggregate mean mortality rates were taken while grouping within region and then year.

Hypothesis 1
Question:    “Does physical activity prevent Alzheimer’s disease?”
Null Hypothesis:   “The well-being of physically inactive patients (with AD) stays the same or gets better.
Alternative hypothesis: “The well-being of physically inactive patients (with AD) gets worse.”
“Less Active - Poor Health” scatter plot shows that when the number of inactive days increases the percentage of people (with Alzheimer’s) with poor health also increases.
The correlation coefficient is 0.75 (the R-value is close to 1) which means there is a strong correlation between inactive days and poor health.
The probability (P-value) value is less than 0.05 which is strong evidence against the null hypothesis. (edited) 

Hypothesis 2
 
The hypothesis tested was that gender has an affect on Alzheimer's disease in the United States.
In this presentation we are looking at the difference is “Poor Health” percentages between Males and Females
There is not strong enough evidence for us to reject the null hypothesis in support of the alternative hypothesis that Alzheimer's disease is more prevalent based on gender.
We summarized the data of the gender specific percentages of “Poor Health” into a box plot and bar chart.
Results from the T-Test: T-Statistic = 0.3888480772932494 and a P-Value = 0.6975190881819724, >.05, not allowing us to reject the null hypothesis
In conclusion, the p-value was higher than our significance level of 0.05. We are unable to reject the null hypothesis, therefore it is possible that gender may not have an effect on AD cases.

Hypothesis 3
The hypothesis tested whether age affect Alzheimer’s severity. More specifically, if increase age leads to an increase in AD cases.
The null hypothesis: Age is not affecting AD progression.
Alternative Hypothesis: AD progression and severity increase with age.
For Specific Age groups, increase age seems to have an effect on AD progression
However, using chi-square we could not find an association specifically to a particular state. 


Hypothesis 4
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
To further investigate the specific factors contributing to regional differences, the use of the Geo API to collect data about gyms and fast food across these regions was proposed. Due to API limitations, the approach would require splitting up cities in calls, scaling that out to states, and then eventually regions, to encompassing the entire US. If explored in the future, the approach would start with very small radii rather than state-sized radii to avoid hitting the 500 feature limit.

During the preparation of this project we faced some challenges, particularly when we were trying to collect information regarding Alzheimer's patients. 
In the search for database regarding the project we realized that most databases with patient data contain sensitive information,
which hindered our direct access or free share of these data.
Some of the medical databases that were free to access contained either special terms specific to the type or the experimental parameters of the study,
or preprocessed data. In additon, our current dtabase does not contain specialized parameters such as race, medical history, drug use. Thus,  conclusions regarding the parameters of Alzheimer's disease cannot be drawn with absolute certainty. Finally, the data were collected between 2015-2020, and therefore we cannot have real time insights for the current US population.

However, our analysis can be used for a general risk assessment of Alzheimer's progression in the US.

Specifically, we can associate the current pool of data with other health-related API sources deriving from  CDC, or published NIH studies(pubmed) 
specific regional parameters (Geolocation) (API Slide), Nutritional habits (number or quality of food centers) and  Health centers (number or type of physical activities).

Base upon these facts we can conclude that despite the limitations described above, we used the current data analysis to verify and expand on the prevelence
of Alzheimer's disease progression in the aged US population.


.DS_Store
