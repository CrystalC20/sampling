# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: Crystal Chen

### Instances of sampling
1. `infected_indices = np.random.choice(ppl.index, size=int(len(ppl) * ATTACK_RATE), replace=False)`: 
    - PURPOSE: identify a subsent of people from a population of 1000 who get COVID-19
    - SAMPLING FRAME: the entire population
    - SAMPLE SIZE: 10% of the population (i.e., 100 people)
    - SAMPLING METHOD: simple random sampling
    - DISTRIBUTION: uniform distribution as everyone has an equal chance of being infected (i.e., chosen)
2. `ppl.loc[ppl['infected'], 'traced'] = np.random.rand(sum(ppl['infected'])) < TRACE_SUCCESS`:
    - PURPOSE: to identify from among the infected individuals who receive primary contact tracing
    - SAMPLING FRAME: infected individuals
    - SAMPLE SIZE: 20% of infected individuals
    - SAMPLING METHOD: each infected person receives a value from 0 to 1 drawn from a uniform distribution. Those who have a value less than 0.2 (i.e., trace success) is tracked.   
    - DISTRIBUTION: uniform distribution since infected individuals have equal likelihood of being picked for primary tracing

### Judging reproducibility 
The script is able to reproduce similar results for the distribution of the trueproportion (i.e., infection from weddings in blue) as the distribution is centered around 0.2 just like the true proportion distribution in the original blogpost. However, the script doesn’t seem to produce similar results for the distribution of observed proportions (i.e., traced to weddings in red) because while this distribution is centered somewhat lower than 0.2 with a long left tail (i.e. right-skewed), the distribution of observed proportions in the original blogpost was left skewed. However, the script still manages to highlight how contact tracing can lead to an observed distribution of proportions that is not reflective of the true distribution. 

### Modifying m=1000 to m=100
There are significant changes to both the true (blue) and observed (red) proportion distributions each time the script is run. The true distribution sometimes is more heavily clustered around 0.2 and sometimes less. Similarly, the observed distribution is sometimes more clustered around 0.15-0.2 and other times, less so. 

### Changing script to make results reproducible
Note: I am modifying the original script so m=1000 instead of m=100. 

The only change I made was to add `np.random.seed(0)` before the code that generates 1000 simulations (i.e. `results = [simulate_event(m) for m in range(1000)]`). This ensures that when random sampling occurs, it always generates the same set of random samples between different executions of the script, leading to reproducible results. 


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
