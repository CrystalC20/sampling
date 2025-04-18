# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
2. Sample size
3. Target population
4. Sampling frame
5. Survey mode(s) 
6. Timeline
7. Response rate
8. Weights
9. Data processing
10. Cleaning, imputation, etc
11. Sources of error
12. Limitations, known biases, etc
13. Link to documentation and any additional sources used


# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `1`

**Describe the purpose of your survey:** The purpose of my study is to provide an holistic view of employee opinions regarding their work. The survey will target pros and cons of employees' work, whether support is available, time spent on work, and suggested improvements. 

**Describe your target population, sampling frame, sampling units, and observational units:**
- **target population:** All employees in entry- and lower-level positions. Note that given high turnover seems to be predominantly among these lower-level positions, the survey will focus on this subset of employees rather than all employees across the company.  
- **sampling frame:** all entry- and lower-level employees who have worked at the company for at least 1 month. Note that instead of defining the sampling frame as the target population, I've decided to sample from employees who are not extremely new hires as they likely have more insights about their work and the workplace given they have worked in their position forsome time whereas new hires may still be adjusting to their work or in a probationary/training period where they have yet to take on the full scope of their position. But depending on the company structure, it may also be reasonable to simply sample from the entire target population instead. 
- **sampling units:** individual employees.
- **sampling strategy:** stratified sampling with strata defined by department. From among the employees in entry- and lower-level posotions who have worked at the company for at least a month, I would stratify the sampling frame by department and randomly sample 10% (or some other reasonable percentage) of employees in each strata. Chosen employees will be invited via email to complete an employee satisfaction survey. 

**Questions:**
1. What do you enjoy about your work? (Open response)
2. What are some common challenges related to your work? (Open response)
3. When a challenge arises, do you feel your colleagues are able to support you in overcoming the challenge? (Y/N)
4. Do you work overtime? If yes, please provide an estimated number of hours per week. (Y/N, with option to provide text response)
5. What changes could be implemented to better support your work? (Multiple choice)
    - More professional training
    - More team check-ins
    - Improved system for flagging issues to colleagues
    - Other: (Open response)

- Note: survey questions will not include any information which can be easily pulled from an employee's file (e.g., age, gender, department, supervisor, etc.). This will help reduce the number of questions the employee has to answer. However, this kind of information would still be incorporated in the analysis. 


## Part B - Survey Evaluation:

Identify and describe survey features:
1. **Sample type:** stratified sampling with strata being defined by province/census metropolitan area (total number of strata = 27). A random member per household aged 15 years or older is sampled to answer the survey. It is unclear if all households are sampled. 
2. **Sample size:** documentation indicated that a "field sample" of 50,000 was selected, but only 40,000 subsequent invitations were sent to complete the questionnaire. It was not entirely clear why there was a difference in the field sample vs. invitations. 
3. **Target population:** all ersons 15 years of age and older living in the ten provinces of Canada, excluding full time (residing 6+ months) residents of institutions.
4. **Sampling frame:** combined landline and mobile phone numbers from census in addition to "various administrative sources with Statistics Canada's dwelling frame" which was defined as groupings of numbers that are associated with a shared address or single telephone numbers in the instance where the number could not be linked to an address. 
5. **Survey mode(s):** they employed a method called "rejective sampling" to determine the kinds of surveys selected individuals completed. Sampled individuals are identified as a volunteer or non-volunteer. All volunteers complete a long interview. Meanwhile non-volunteers are randomly divided into two groups, one which completes a long interview and one which completes a short interview. 
6. **Timeline:** data collection occured between September 4th to December 28th, 2018.
7. **Response rate:** 41.9%
8. **Weights:** the microfile contains a basic weighting factor called *WGHT_PER* which specifies the weighting per person (non-institutionalized and 15+ years old). 
9. **Data processing:** processing using "SSPE generalized processing steps" with automatic edits centered around familial relations, data consistency and flow path edits.  
10. **Cleaning, imputation, etc:** 
    - Used CATI data capture system to identify when responses were out of range, with immediate resolution via the CATI system or by the interviewer. Anything that was not immediately resolved was flagged with interviewer comments. Resolutions were subsequently done at head office. 
    - Imputations were generally made by filling in missing data from a donor record that was most similar to the recipient (respondent) record. A scoring process based on comparisons between recipient and donor records was used to identify the most similar donor record. Ties were broken via random selection between the two highly similar donor records. When donor imputation was not possible, mean emputation was used instead. 
11. **Sources of error:** 
    - Imperfect coverage as a result of households without telephones being excluded from sampling frame.
    - Non-response at both individual and household levels. 
12. **Limitations, known biases, etc:** Both imperfect coverage and non-response may introduce some bias/error the data. Coverage bias was accounted for by adjusting estimates through weighting that takes into consideration households without telephones. Non-response bias was accounted for through adjustments in the wurvey weights.   
13. **Link to documentation and any additional sources used:** 
    - https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&SDDS=4430


## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 18/04/2025`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
