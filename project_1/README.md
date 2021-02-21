# Project 1: What Factors Affect SAT Participation in US States?

In this project, I examined the SAT and ACT participation rates and aggregated scores from 2017 and 2018 with the objective of determining a state in the USA where the College Board may next invest into with the intent of increasing SAT participation.

I determined the data science problem statement to be:

Does:

1. ACT participation,
2. SAT average scores, or
3. ACT average scores

For a given year affect SAT participation for that year, and

4. What other factors outside of the given data affect it?

I have simulated the time performing this project to 2019 and limited my use of sources to information available in 2019 and earlier to account for the age of the datasets given.

---

## Executive Summary

The technical report is located in folder /code/ and accompanying visual presentation in folder /presentation/.

The data used for this project are from the following sources: SAT (2017), SAT (2018), ACT (2017), ACT (2018). These sources may be found in the /data folder with the 2017 and 2018 datasets combined as /data/combined_2017.csv and /data/combined_2018.csv. All other datasets in the /data/ folder are components of the eventual final_with_outside.csv dataset.

These datasets were combined and evaluated using various data visualization techniques with the aim of finding relationships between their combined data.


### Summary of Findings & Recommendations

From the given data, I found that:
1. SAT and ACT participation rates had an inversely correlated relationship. This comes as no surprise given that each exam requires preparation over a number of months or years, the papers may be re-taken, and since colleges have no preference for one exam over the other. 
2. Participation had an inversely correlated relationship with aggregate exam scores. This is also not a surprising finding given that if either exam was optional, and if colleges accept both equally, then it would be beneficial for students to take only the exam they excel in. In a state with the SATs being optional and ACT being compulsory or having a high participation rate, the average total of the SAT in that state will likely be very high (since only students who know they can/will perform well will voluntarily take it).
3. A high average score in one exam is inversely correlated with the exam score in the other exam. This is a consequence of observation 1.
4. If the SAT or ACT was taken in 2017, it would continue to be taken in 2018. This would also make intuitive sense given states would want to track their performance on the same standard over a long period of time. It would be preferable for the state chosen for investment not have a history of taking the ACT. There were, however, exceptions found to this.
5. Average SAT Total and ACT Composite are indicative of average performance in each of their respective component papers.

Unfortunately, the relationship between 2017 SAT Scores and 2018 SAT Participation (ie. to answer the question, will perceived difficulty of paper (difficult due to lower scoring) affect participation the next year?) This question could not be answered due to exam observation 2 -- that exam score is highly dependent upon participation. Individual student performance data samples will be required to answer this question.

Next, we looked into demographics. It was found that:
6. States which favoured SAT tended to be on the East and West coast, while Mountain and Mid-western states tend to favour ACT.

Two states were exception to this trend: Colorado and Illinois. They gained significantly in SAT Participation in 2018 from 2017 due to states abandoning PARCC/Smarter Balanced high school testing and ESSA allowing states to use SAT as their primary high school examination. Colorado chose to start using SAT over ACT in 2018.

After comparing the relationship between Median Household Income in 2018 by state, it was determined that:
7. SAT participation was positively correlated with Median Household Income.

Oregon is recommended as the state for College Board to invest in due to several favourable factors:
1. Over USD 70,000 in median household income, similar to Colorado and Illinois.
2. Has an SAT Participation rate of under 50%.
3. Also has a low ACT Participation of under 50%
4. Is currently still using the Smarter Balanced high school tests, which are being phased out nation-wide.
5. As an added bonus, Oregon is located on the west coast and is next to Idaho, California and Washington, all of which favour the SAT.

### Data Dictionary

1. Using Only Given Data. This may be found in /data/final.csv:
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT and ACT|State in the USA|
|2018_ & 2017_sat_participation|float|SAT|%-Participation in SAT 2017 represented as a float from 0.0 - 1.0.|
|2018_ & 2017_sat_ebrw|float|SAT|Average score of SAT 2017 Evidence-based Reading and Writing. Range from 200 - 800.|
|2018_ & 2017_sat_math|float|SAT|Same as above, but for SAT 2017 Math.|
|2018_ & 2017_sat_total|float|SAT|Sum of 2017_sat_ebrw and 2017_sat_math. Range from 400 - 1600. Indicative of student's overall SAT performance.|
|2018_ & 2017_act_participation|float|ACT|%-Participation in ACT 2017 represented as a float from 0.0 - 1.0.|
|2018_ & 2017_act_english|float|ACT|Average score of ACT 2017 English paper. Range from 1 - 36.|
|2018_ & 2017_act_math|float|ACT|Same as above, but for ACT 2017 Math.|
|2018_ & 2017_act_reading|float|ACT|Same as above, but for ACT 2017 Reading.|
|2018_ & 2017_act_science|float|ACT|Same as above, but for ACT 2017 Science.|
|2018_ & 2017_act_total|float|ACT|Average of 2017_act_english, 2017_act_math, 2017_act_reading, and 2017_act_science. Range from 1 - 36. Indicative of student's overall ACT performance.|

2. Adjusted to include outside data. This may be found in /data/final_with_outside.csv
|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|SAT and ACT|State in the USA|
|2018_ & 2017_sat_participation|float|SAT|%-Participation in SAT 2017 represented as a float from 0.0 - 1.0.|
|2018_ & 2017_sat_total|float|SAT|Sum of 2017_sat_ebrw and 2017_sat_math. Range from 400 - 1600. Indicative of student's overall SAT performance.|
|2018_ & 2017_act_participation|float|ACT|%-Participation in ACT 2017 represented as a float from 0.0 - 1.0.|
|2018_ & 2017_act_total|float|ACT|Average of 2017_act_english, 2017_act_math, 2017_act_reading, and 2017_act_science. Range from 1 - 36. Indicative of student's overall ACT performance.|
|2018_sat_part_diff|float|SAT|%-change in 2017 to 2018 SAT Participation, represented as a float between 0.0 - 1.0|
|sat_main|boolean|Outside|Boolean indicating if SAT is already the state's adopted high school examination.|
|act_main|boolean|Outside|Boolean indicating if ACT is already the state's adopted high school examination.|
|parcc_main|boolean|Outside|Boolean indicating if state was still using the PARCC/Smarter Balanced high school examination.|
|median_household_income|float|Outside|Median Household Income circa 2018 per State.|
