# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Statistical Summaries and Inference of SAT/ACT Data

### Overview

In Project 1, we are going to analyze the SAT and ACT data sets in 2017 and 2018. The data files are derived from the following sources:

* [SAT 2017](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/)
* [ACT 2017](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows)
* [SAT 2018](https://reports.collegeboard.org/sat-suite-program-results/state-results)
* [ACT 2018](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)

After reading the corresponding data files, cleaning the data, fixing mistyped entries, correcting the data types, renaming columns, and merging the data frames, the following data set is available:

|Feature|Type|Dataset|Description|
|---|---|---|---|
|act\_17_participation| *integer* | ACT 2017 | The Partcipation percentage of each state in the ACT exam conducted in 2017 | 
|act\_17_english| *float* | ACT 2017 | The average English score of each state in the ACT exam conducted in 2017 | 
|act\_17_math| *float* | ACT 2017 | The average Math score of each state in the ACT exam conducted in 2017 |
|act\_17_reading| *float* | ACT 2017 | The average Reading score of each state in the ACT exam conducted in 2017 |
|act\_17_science| *float* | ACT 2017 | The average Science score of each state in the ACT exam conducted in 2017 |
|act\_17_composite| *float* | ACT 2017 | The average Composite score of each state in the ACT exam conducted in 2017 |
|sat\_17_participation| *integer* | SAT 2017 | The Partcipation percentage of each state in the SAT exam conducted in 2017 |
|sat\_17_reading\_and\_writing| *integer* | SAT 2017 | The average Evidence-Based Reading and Writing score of each state in the SAT exam conducted in 2017 |
|sat\_17_math| *integer* | SAT 2017 | The average Math score of each state in the SAT exam conducted in 2017 |
|sat\_17_total| *integer* | SAT 2017 | The average Total score of each state in the SAT exam conducted in 2017 |
|act\_18_participation| *integer* | ACT 2018 | The Partcipation percentage of each state in the ACT exam conducted in 2018 | 
|act\_17_composite| *float* | ACT 2018 | The average Composite score of each state in the ACT exam conducted in 2018 |
|sat\_18_participation| *integer* | SAT 2018 | The Partcipation percentage of each state in the SAT exam conducted in 2018 |
|sat\_18_reading\_and\_writing| *integer* | SAT 2018 | The average Evidence-Based Reading and Writing score of each state in the SAT exam conducted in 2018 |
|sat\_18_math| *integer* | SAT 2018 | The average Math score of each state in the SAT exam conducted in 2018 |
|sat\_18_total| *integer* | SAT 2018 | The average Total score of each state in the SAT exam conducted in 2018 |

### Analysis 

After preparing the data frame that is ready to work with, using sorting, masking, and visualization techniques, I tried to investigate interesting trends in SAT and ACT data.

I found that none of the column distributions really represent a normal distribution. The distribution of scores within each state is most probably normal because they are based on a large sample. But considering relatively small number of states (51) and different factors in each state (different particiaption rates, different educational background, etc), comparing different states does not yield a normal distribution.

In addition, I realized that on average, in both SAT and ACT exams, the total/composite score is negatively correlated to the participation rate. In other words, the higher the participation rate the lower the average total score and vice versa. This explains why some states which have undergone a rapid growth in participation in either of these exams experience a drop in their average total score.

Also, I chose the states of **Colorado**, **Illinois**, and **West Virginia** for further study. The reason is that these states demonstrate the highest rate of growth in the participation rate in SAT 2018 and the steepest rate of decline in SAT 2018 average total score. The first two states also represent the steepest drop in participation and the highest growth rate in the average composite score of the ACT exam conducted in 2018. 

In case of Illinois, the Illinois High School Accountability Assessments in June 2018 made a contract with College Board, which administers the SAT, to expand their duties as the state’s official tester over ACT (see [here](https://www.ilnews.org/news/schools/college-exam-company-raises-questions-about-with-illinois-act-sat/article_c4a805ca-8b93-11e8-b9d4-f7ab2c28ae00.html)). Although the fairness of this contract has raised many questions, but this is the approved policy in Illinois so far and the majority of juniors in that state took the SAT exam this year. This rapid transition to this new system of standardized tests is probably the main reason behind 8% drop in the average score of the SAT exam. However, some experts have blamed the teacher shortage for the low scores (see [here](https://chalkbeat.org/posts/chicago/2018/09/12/teacher-shortage-blamed-as-fewer-illinois-sat-pass-rates-decline-parcc-scores-flatten/)).

In Colorado, in 2016, the state Department of Education chose the College Board, makers of the SAT, over the ACT testing company to conduct the standardized test (see [here](https://chalkbeat.org/posts/co/2015/12/23/goodbye-act-hello-sat-a-significant-change-for-colorado-high-schoolers/)). Juniors took the SAT for the first time in 2017 as a mandatory state test (see [here](https://www.chalkbeat.org/posts/co/2017/08/17/sat-scores-show-mixed-results-on-whether-colorado-juniors-are-on-track-for-college/)). It seems that Colorado is gradually transitioning from ACT to SAT exam and each year the number of students taking the SAT exam will grow compared to the year before. It is likely that 15% drop in the average score of the SAT exam is due to the fact that this year the number of participants is more than doubled and these new students have a more diverse educational background, ethnicity, etc. So, the new average better reflects the average literacy level of students across the entire state.

West Virginia is the other key battle the ACT company has lost to the College Board. In 2017, the West Virginia Department of Education chose the SAT as the new statewide standardized test to replace the Smarter Balanced exam for high school juniors (see [here](https://www.wvgazettemail.com/news/education/wv-chooses-sat-as-new-high-school-standardized-test-for/article_b60d2618-4943-56f6-b180-4b4442172ef8.html)). According to Charlestone Gazette Mail, "This is the first time, at least in recent years, that a popular college-entrance exam will be given to most West Virginia public school students for free". Similar to Colorado, a more diversified population of students taking the SAT test is probably responsible for about 8% drop in the average score of this exam in 2018.

### Recommendation 

The states which have decided to adopt a new platform of standardized tests should allow for a smooth transition from the old system to the new system in order the educators and the students be able to adapt themselves gradually. Otherwise, a big jump in the participation rate of either of these exams will only deteriorate the average score of that state and it may result in a distrust of the new platform.