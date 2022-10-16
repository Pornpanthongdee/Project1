# Project 1:  SAT / ACT Standardized Test Analysis

**Pornpan Thongdee DSI by TDA**

## Problem Statement

**❓ Why Are Average SAT / ACT Scores by State Important?❓**

>For some, knowing state average test scores is fun trivia: my state is the best and smartest.  But for many students and parents, knowing state average SAT / ACT scores can be critical. For students applying for scholarships, many scholarships are more competitive in "smarter" states. For students who want to compare themselves to their in-state peers, the scores above are also very useful. For families thinking of moving states, they may want to make sure their target state has a good education system. For researchers and education designers, this data helps them see which state systems are working and which ones may be failing.


### Contents:
- [Project 1: Standardized Test Analysis](#project-1-standardized-test-analysis)
  - [Problem Statement](#problem-statement)
    - [Contents:](#contents)
  - [Background](#background)
  - [Data](#data)
  - [Outside Research](#outside-research)
  - [**Conclusion And Recommendations:**](#conclusion-and-recommendations)

## Background
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).


## Data

There are 10 datasets included in the [`data`](./data/) folder for this project. You are required to pick **at least two** of these to complete your analysis. Feel free to use more than two if you would like, or add other relevant datasets you find online.

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State
* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State



**Data sources:**

> 2017, 2018 and 2019 SAT and ACT data were provided as a part of project materials. Comparisons were made by comparison to reports at these sites:

**Data Import and Cleaning**
>Read in the sat_2018.csv and act_2018.csv files and assign them to appropriately named pandas dataframes. For the 2018 ACT Data, only the Composite scores are available. Repeating the same processes to clean the 2018 data here as in the previous sections above.

* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

**Updated data dictionary.**

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|final_df|State of the data|
|sat_part_2017|float|final_df|State participation rate for the SAT in 2017|
|sat_erw_2017|integer|final_df|State average SAT Evidence-Based Reading and Writing score in 2017|
|sat_math_2017|integer|final_df|State average SAT Math score in 2017|
|sat_total_2017|integer|final_df|State average SAT Total score in 2017|
|act_part_2017|float|final_df|State participation rate for the ACT in 2017|
|act_eng_2017|float|final_df|State average ACT English score in 2017|
|act_math_2017|float|final_df|State average ACT Math score in 2017|
|act_read_2017|float|final_df|State average ACT Reading score in 2017|
|act_sci_2017|float|final_df|State average ACT Science score in 2017|
|act_comp_2017|float|final_df|State average ACT Composite score in 2017|
|sat_part_2018|float|final_df|State participation rate for the SAT in 2018|
|sat_erw_2018|integer|final_df|State average SAT Evidence-Based Reading and Writing score in 2018|
|sat_math_2018|integer|final_df|State average SAT Math score in 2018|
|sat_total_2018|integer|final_df|State average SAT Total score in 2018|
|act_part_2018|float|final_df|State participation rate for the ACT in 2018|
|act_comp_2018|float|final_df|State average ACT Composite score in 2018|
|sat_change_part_17_to_18|float|final_df|2018 less 2017 SAT participation|
|act_change_part_17_to_18|float|final_df|2018 less 2017 ACT participation|
|sat_act_part_2017|float|final_df|2017 SAT less 2017 ACT participation|
|sat_act_part_2017|float|final_df|2018 SAT less 2018 ACT participation|
|state|object|inc_df_f|State of the data|
|per_capita_income|float|inc_df_f|State per capita income 2010 - 2014|
|median_household_income|float|inc_df_f|State median household income 2010 - 2014|
|median_family_income|float|inc_df_f|State median family income 2010 - 2014|
|population|float|inc_df_f|State population|
|no_of_households|float|inc_df_f|State number of households|
|no_families|float|inc_df_f|State number of families|
|sat_part_group|float|inc_df_f|Binned state 2018 SAT participation|
|act_part_group|float|inc_df_f|Binned state 2018 ACT participation|




## Outside Research
* Income and population data were sourced from Wikipedia at the link below with a further reference to the American Community Survey 1-Year Estimates at the link below:

* Wikipedia data
* American Community Survery

***Observations***


>Analysis of incomes and test participation show a moderate positive correlation between SAT participation, per capita income and household income. Since SAT and ACT participation rates are negatively correlated, this results in a negative correlation between ACT participation and income. Participation rates displayed little correlation with state population.



## **Conclusion And Recommendations:**

* The ACT and SAT participation distributions roughly mirror each other, with states tending to prefer one test or the other. ACT shows a large group of highly committed states, and a higher baseline participation nationwide. SAT shows a larger group of states with 50-80% participation, as well as a smaller set of highly committed states. The ACT has been doing quite well.
* ACT and SAT scores are inversely correlated with their respective participation rates. This is likely due to selection bias, as low participation means those who are participating tend to be higher achieving, and high participation means diluted quality of performance.
There are strong regional (and possibly political) affiliations associated with ACT versus SAT preference. Coastal progressive states tend to favor the SAT, while Midwestern and Mountain conservative states tend to favor the ACT.
* The SAT made clear gains in 2018 relative to the ACT. The states making these gains tended to be states in the 10-15% participation range, at the upper edge of the lower bloc, or in the 70% range, at the upper edge of the middle bloc, in the distribution of SAT participation by state. Targeting states in similar positions in the 2018 distribution should be promising for the College Board moving forward.
