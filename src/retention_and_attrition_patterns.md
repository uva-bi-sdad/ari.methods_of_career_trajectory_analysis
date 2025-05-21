---
title: Retention and Attrition Patterns for Analyzing Career Trajectories
format: latex
---


Retention and attrition patterns analysis is a methodological approach that applies event history analysis (also known as survival analysis) techniques to understand and predict career trajectories within organizations. This approach focuses specifically on analyzing when and why individuals leave an organization (attrition) or stay (retention) over time, and how various factors influence these patterns. The methodology allows researchers to model the "time until event" (such as departure from an organization) while accounting for censored observations (individuals who haven't experienced the event by the end of the observation period).

## 1. Approach Description & Goal

Retention and Attrition Patterns analysis applies survival analysis/event history analysis techniques to understand career trajectories, particularly focusing on when and why employees leave or stay in an organization. The approach models the timing of critical career events such as job changes, promotions, or organizational exits, while accounting for censored observations (when individuals haven't experienced the event by the end of the study period).

The primary goals of this approach include predicting which employees are at risk of leaving an organization and when; identifying key factors that influence retention and attrition decisions; understanding patterns of career progression within organizations; developing targeted interventions to improve retention rates; and modeling career trajectories to inform talent management strategies. As noted in research, understanding the causes of events like employee turnover requires analyzing both the timing of events and the factors that influence them, making this approach particularly valuable for organizations facing high turnover costs[6][13].

## 2. Critical Variables

Typical variable categories used in retention and attrition pattern analysis include:

1. **Individual Characteristics**: Demographic variables (age, gender, race/ethnicity), educational background (level, field of study), cognitive ability (AFQT scores), personality traits (TAPAS dimensions), and prior experience[10].

2. **Job-Related Factors**: Compensation and benefits, job satisfaction, workload, work-life balance, career development opportunities, and recognition. Research shows that lack of career development remains a key driver of employee attrition—cited by 40% of departing employees[2].

3. **Organizational Factors**: Corporate culture measures (which can be 10.4 times more powerful than compensation in predicting turnover), leadership quality, team dynamics, training opportunities, and innovation levels[19].

4. **Time-Related Variables**: Tenure in organization, time since last promotion, career stage, and historical timing (economic conditions, labor market).

5. **Event-Specific Variables**: Type of attrition (voluntary vs. involuntary), reason for departure (medical/physical, misconduct, performance), and destination after departure[10].

These variables serve as predictors, controls, or outcome measures, depending on the specific research question.

## 3. Key Overviews

Allison, P.D. (1982) "Discrete-Time Methods for the Analysis of Event Histories" [6]:
Paul Allison's seminal paper introduces discrete-time methods for analyzing event history data, particularly beneficial when dealing with tied event times (multiple events occurring simultaneously). The paper addresses the challenges of conducting event history analysis, primarily focusing on two significant issues: censoring (when the event has not occurred by the end of observation) and time-varying explanatory variables. Allison demonstrates how to transform event history data into a person-period format suitable for logistic regression analysis, allowing researchers to estimate the effects of various factors on the probability of an event occurring within discrete time intervals. This approach has become foundational in career trajectory analysis because it enables researchers to account for time-dependent covariates and censored observations while using familiar statistical techniques like logistic regression.

Li, H., Ge, Y., Zhu, H., Xiong, H., & Zhao, H. (2016) "Prospecting the Career Development of Talents: A Survival Analysis Perspective" [4]:
This innovative paper applies survival analysis techniques specifically to model talent career paths, focusing on two critical issues in talent management: turnover and career progression. The authors formulate the prediction of talent retention status across a sequence of time intervals as a multi-task learning problem, where prediction at each time interval is considered a separate task. They incorporate ranking constraints to effectively model both censored and uncensored data, capturing the intrinsic properties exhibited in lifetime modeling with non-recurrent and recurrent events. For modeling career progression, they predict relative occupational levels at different time intervals, with ranking constraints imposed on different occupational levels to reduce prediction error. The authors demonstrate the effectiveness of their approach through evaluation against baseline methods using real-world talent data, providing a sophisticated framework for predicting both turnover and career advancement patterns.

Maas, I. "The Use of Event-History-Analysis in Career Research" [13]:
This comprehensive introduction to event-history analysis in career research highlights how this methodological approach has become an essential tool for sociologists studying contemporary careers. Maas contrasts event-history analysis with alternative methods like status attainment models and log-linear models, emphasizing that event-history models are better equipped for causal analysis because they clarify the direction of causality, distinguish strengths of reciprocal effects, and model effects of previous history. The chapter addresses practical challenges, including the extensive data requirements (complete information on all jobs and their timing), and discusses three types of data sources: retrospective designs, panel studies, and administrative records. Additionally, Maas explains how event-history models allow for the introduction of time-specific independent variables and describes three main types: semi-parametric models (Cox proportional hazard model), discrete-time models, and parametric models. The chapter concludes by surveying leading issues and findings from applying event history analysis to careers, examining individual characteristics, social influences, and broader socioeconomic factors.

"Introducing Survival and Event History Analysis" [16]:
This introductory text provides a comprehensive overview of survival and event history analysis techniques, explaining that these methods are particularly suited for analyzing categorical sequences of events to model entire event history career trajectories. The book focuses on the order and timing of events rather than gradual changes, making it ideal for studying career transitions, promotions, and job changes. It introduces fundamental concepts such as hazard functions, survival curves, and censoring, while explaining both parametric and non-parametric approaches to survival analysis. The text addresses practical implementation issues, including data preparation, model specification, interpretation of results, and diagnostics. Through illustrative examples, the book demonstrates how these techniques can reveal patterns in career development that might remain hidden with conventional statistical methods, making it an essential resource for researchers studying career trajectories, employee retention, and professional mobility.

## 4. Mathematical Approach

Retention and attrition pattern analysis primarily utilizes event history analysis (survival analysis) methods, which focus on modeling the time until an event occurs. In the context of career trajectories, the "event" typically refers to leaving an organization (attrition) or receiving a promotion (career progression). The mathematical approach involves several key concepts:

The fundamental concept is the hazard function, which represents the instantaneous rate at which events occur, given that the individual has survived up to that point. For career trajectory analysis, the hazard function h(t) represents the probability that an employee leaves or gets promoted in a small time interval [t, t+Δt], given that they have remained in their current state until time t:

h(t) = lim<sub>Δt→0</sub> [P(t ≤ T < t+Δt | T ≥ t) / Δt]

Where T is the random variable representing the time until the event occurs.

The survival function S(t), which represents the probability of "surviving" (remaining in the current state) beyond time t:

S(t) = P(T > t) = exp[-∫<sub>0</sub><sup>t</sup> h(u)du]

For analyzing censored data, the Kaplan-Meier estimator provides a non-parametric estimate of the survival function:

S(t) = ∏<sub>t<sub>i</sub>≤t</sub> [1 - (d<sub>i</sub>/n<sub>i</sub>)]

Where t<sub>i</sub> represents the distinct event times, d<sub>i</sub> is the number of events at time t<sub>i</sub>, and n<sub>i</sub> is the number of individuals at risk just before t<sub>i</sub>[14].

For modeling the effects of covariates, Cox proportional hazards regression is commonly used:

h(t|X) = h<sub>0</sub>(t) × exp(β<sub>1</sub>X<sub>1</sub> + β<sub>2</sub>X<sub>2</sub> + ... + β<sub>p</sub>X<sub>p</sub>)

Where h<sub>0</sub>(t) is the baseline hazard function and X<sub>1</sub>, X<sub>2</sub>, ..., X<sub>p</sub> are the covariates with corresponding coefficients β<sub>1</sub>, β<sub>2</sub>, ..., β<sub>p</sub>[14].

For discrete-time data, logistic regression can be used to model the conditional probability of an event occurring at time t, given survival up to that point:

logit[P(T = t | T ≥ t, X)] = α<sub>t</sub> + β<sub>1</sub>X<sub>1</sub> + β<sub>2</sub>X<sub>2</sub> + ... + β<sub>p</sub>X<sub>p</sub>

Where α<sub>t</sub> represents the baseline logit-hazard at time t[6].

For competing risks (multiple types of events, such as different reasons for leaving an organization), the cause-specific hazard function for event type k is:

h<sub>k</sub>(t) = lim<sub>Δt→0</sub> [P(t ≤ T < t+Δt, K = k | T ≥ t) / Δt]

Where K denotes the type of event[14].

## 5. Example Applications

"An Analysis of Career Trajectories and Occupational Transitions" (U.S. Department of Labor) [12]:
This comprehensive study by the Department of Labor examines wage growth and occupational transitions over 10-year periods to identify "launchpad" occupations that facilitate career advancement. Using longitudinal panel surveys, the researchers analyze variations in trajectories among workers starting in mid-level occupations, identifying which occupations lead to higher wage growth and better long-term outcomes. The study incorporates both occupational characteristics (skill requirements, licensing) and worker demographics to understand disparities in wage growth among different populations. By tracking actual career paths rather than theoretical possibilities, the research reveals which occupations consistently serve as reliable springboards for career advancement across different sectors and demographic groups. The trajectory analysis methodology allows for the examination of multiple outcomes beyond wage growth, including unemployment periods and educational attainment, providing a holistic view of career development patterns that can inform workforce development strategies and career counseling approaches.

"Attrition and reenlistment in the Army: Using the Tailored Adaptive Personality Assessment System" [10]:
This military-focused study employs survival analysis to predict attrition and reenlistment among U.S. Army Soldiers, evaluating both cognitive measures (Armed Forces Qualification Test) and non-cognitive assessments (Tailored Adaptive Personality Assessment System, TAPAS). The researchers examine the complete timeline of enlisted Soldiers' first term of service, categorizing attrition by reason for separation (medical/physical, misconduct, performance-related) and analyzing variations in first-term reenlistment across different Military Occupational Specialties. The analysis reveals that attrition associated with medical/physical and performance reasons tends to occur early in Soldiers' careers, while misconduct-related attrition emerges after several months of service. The study demonstrates that personality characteristics as measured by TAPAS contribute incrementally beyond cognitive ability in predicting retention outcomes, with different attrition categories showing distinctive temporal patterns. By modeling attrition over time and across categories, the research provides insights for developing targeted interventions at specific career stages to enhance force readiness and reduce the substantial costs associated with early Soldier attrition.

"Dynamic work trajectories and their interplay with family over the life course" [18]:
This innovative study applies event history analysis to examine how work trajectories and family dynamics interact throughout individuals' life courses, capturing the bidirectional relationship between career development and family transitions. The researchers utilize sequence analysis and event history methods to model entire career paths while accounting for critical family events such as marriage, childbirth, and caregiving responsibilities. The study reveals how family-related transitions influence career trajectories differently for men and women, identifying critical junctures where career paths may diverge based on family decisions. By analyzing transitions into the labor market and subsequent career movements in relation to family formation patterns, the research highlights how early career decisions create path dependencies that shape long-term outcomes. The application of survival analysis techniques allows the researchers to quantify the timing and likelihood of career disruptions following family events, providing insights into the complex interplay of work and family that traditional cross-sectional analyses would miss.

"Predicting employee attrition and explaining its determinants" [1]:
This cutting-edge study applies machine learning models to real-world data from a prominent Italian financial institution to predict employee attrition and identify its key determinants. The researchers employ survival analysis techniques to model the time until employee departure, incorporating both static factors (demographics, education, personality) and time-varying covariates (performance ratings, compensation changes, role transitions). By formulating attrition prediction as a multi-task learning problem across different time horizons, the study captures both immediate attrition risk and long-term retention patterns. The methodology accounts for competing risks by distinguishing between voluntary departures and involuntary separations, allowing for targeted interventions based on attrition type. The study demonstrates the superiority of this approach over traditional turnover models by capturing the temporal dynamics of attrition risk throughout the employee lifecycle, identifying critical periods when intervention might be most effective. The insights generated help organizations develop proactive retention strategies tailored to specific employee segments and career stages.

## 6. Critiques

Based on the search results, particularly from [9], there are several significant limitations of using survival analysis/event history analysis for studying retention and attrition patterns:

1. **Censoring Assumptions**: The approach requires specific assumptions about censored data that may not reflect reality. This can potentially bias results, especially if censoring is related to the likelihood of experiencing the event (informative censoring)[9].

2. **Complexity for Non-Statisticians**: The interpretation and implementation of survival analysis can be difficult for practitioners without specialized statistical knowledge, limiting its practical application in organizational settings[9].

3. **Modeling of Time-Dependent Covariates**: Incorporating variables that change over time (such as job satisfaction or compensation) can be methodologically complex and may lead to model misspecification if not handled properly[9].

4. **High Variability with Small Sample Sizes**: Estimates can be unstable with small numbers of events or a high censoring rate, which is particularly problematic when studying rare events or specific subgroups[9].

5. **Assumption of Independent Censoring**: The approach assumes that censoring is unrelated to prognosis, which may not always be true in organizational settings[9].

6. **Competing Risks Challenges**: Standard methods do not adequately account for competing risks (different types of departures), which can lead to biased risk estimates[9].

7. **Data Requirements**: The method requires high-quality, complete longitudinal data over follow-up periods, which can be difficult and expensive to obtain. As noted by Maas, "Not only information on all jobs, but also on the timing of the transition from one job to the other is necessary"[13].

8. **Proportional Hazards Assumption**: The commonly used Cox proportional hazards model assumes that the effect of predictors remains constant over time, which may not hold for many career-related factors[9].

## 7. Software

**R "survival" package [7]:**
The "survival" package is the foundation of survival analysis in R, maintained by Terry Therneau of the Mayo Clinic, and serves as the backbone for most survival analysis functions in the R ecosystem. It provides comprehensive implementations of essential survival analysis methods including Kaplan-Meier survival curves, Cox proportional hazards models, parametric survival models, competing risks analysis, and methods for handling time-dependent covariates. The package includes robust functions for visualizing survival data through various plotting methods, conducting hypothesis tests to compare survival curves across groups, and implementing diagnostics to assess model assumptions. With its extensive documentation and long development history (spanning over two decades), the survival package offers both basic functionality for beginners and advanced options for complex survival modeling scenarios. Its integration with other R packages extends its capabilities, making it ideal for comprehensive retention and attrition studies across various organizational contexts.

**Python "lifelines" library [8]:**
The "lifelines" library is Python's premier survival analysis package, providing a complete suite of tools for modeling and analyzing time-to-event data with an intuitive, scikit-learn inspired API that makes it accessible to data scientists already familiar with Python's data science ecosystem. The library implements core survival analysis techniques including Kaplan-Meier estimators, Cox Proportional Hazards models, Aalen's Additive model, and various parametric models (Weibull, exponential, log-normal, log-logistic), all optimized for performance with large datasets common in modern retention analysis. It features robust handling of left, right, and interval censored data, comprehensive visualization tools for survival curves and hazard functions, and built-in statistical tests for comparing survival distributions between groups. The package includes model selection tools, residual analysis functions for checking assumptions, and methods for determining variable importance, making it particularly valuable for predictive modeling of employee attrition. Lifelines' extensive documentation, tutorials, and integration with the broader Python data science ecosystem (pandas, numpy, matplotlib) make it an excellent choice for organizations using Python for their data analytics infrastructure.

**SAS Survival Analysis Procedures:**
SAS offers comprehensive survival analysis capabilities through procedures like PROC LIFETEST, PROC PHREG, and PROC ICPHREG, making it a powerful tool for retention and attrition analysis in large organizations and research institutions with existing SAS infrastructure. The software provides exceptional handling of complex survey designs, robust procedures for competing risks analysis, and sophisticated methods for dealing with time-dependent covariates that are crucial for modeling dynamic aspects of career trajectories. SAS's superior performance with extremely large datasets makes it particularly valuable for enterprise-level workforce analyses spanning thousands of employees over long time periods. The software includes extensive diagnostics for assessing proportional hazards assumptions, identifying influential observations, and checking functional forms of continuous predictors. While requiring a commercial license and specialized programming knowledge, SAS remains the gold standard in many industries for its validated statistical procedures, regulatory acceptance, and integration with broader enterprise data systems, making it particularly valuable for regulated industries where methodological reliability is paramount.

**STATA Survival Analysis Commands:**
STATA's survival analysis suite combines statistical rigor with accessibility through intuitive commands like stcox, streg, and stcurve, alongside a graphical user interface that makes it particularly approachable for researchers and HR analysts with limited programming experience. The software excels in handling complex survey designs, implementing flexible parametric survival models through its stpm2 command, and offering extensive post-estimation capabilities for predictive modeling of employee retention. STATA's strengths include exceptional documentation with practical examples, built-in publication-quality graphics for survival curves and cumulative incidence functions, and seamless integration of survival analysis with STATA's broader statistical capabilities. The software provides comprehensive support for frailty models (accounting for unobserved heterogeneity), multi-state modeling for complex career transitions, and competing risks analysis through the stcrreg command. While requiring a commercial license, STATA's balance of power and usability, combined with its strong presence in academic research, makes it particularly valuable for organizations collaborating with academic partners on retention research or seeking methodological approaches grounded in peer-reviewed literature.

## 8. Example Study Design

### Example Retention and Attrition Patterns Study of Career Trajectories of U.S. Army Officers

#### Key Variables

The study would incorporate variables from multiple domains to comprehensively analyze officer retention and attrition patterns:

1. **Branch-Specific Indicators:**
   - **Armor Division:** Technical proficiency scores, tactical evaluation results, field exercise performance ratings
   - **Logistics Division:** Supply chain management effectiveness metrics, resource allocation efficiency ratings, logistical planning assessment scores
   - **Aviation Division:** Flight hour accumulation, aircraft qualification levels, mission success rates
   - **Cyber Division:** Technical certification achievement, cyber competition performance, problem-solving assessment scores

2. **Career Progression Indicators:**
   - Time between promotions
   - Performance evaluation scores
   - Command position assignments
   - Specialized training completion
   - Deployment history (frequency, duration, locations)

3. **Non-Cognitive Attributes:**
   - TAPAS (Tailored Adaptive Personality Assessment System) scores on dimensions such as achievement, dominance, attention seeking, and selflessness
   - Resilience measures
   - Leadership style assessments
   - Team cohesion ratings

4. **Demographic and Background Variables:**
   - Age at commission
   - Commissioning source (ROTC, West Point, OCS)
   - Educational background (degree field, advanced degrees)
   - Prior enlisted service
   - Family status (marital status, children, military spouse)

5. **Organizational Context Factors:**
   - Unit morale indicators
   - Leadership quality metrics
   - Operational tempo
   - Geographic location preferences versus assignments

6. **Event Specifics:**
   - Type of separation (voluntary, involuntary)
   - Reason for departure (categorized as medical/physical, performance-related, or misconduct)
   - Career destination after Army (civilian sector, different military branch, retirement)

#### Sample & Data Collection

The study would utilize a longitudinal design following a cohort of Army officers from their commissioning date through either separation or a predetermined endpoint (e.g., 10 years of service). The sample would include:

- Officers commissioned between 2015-2020 across all four branch divisions (Armor, Logistics, Aviation, and Cyber)
- Stratified sampling to ensure adequate representation of each branch and demographic subgroups
- Target sample size of approximately 5,000 officers to allow for branch-specific analyses while maintaining statistical power

Data collection would involve:
1. **Administrative Data:** Integration of personnel records from military Human Resources Command databases, including promotion histories, performance evaluations, assignment records, and separation codes
2. **Assessment Data:** TAPAS scores and other psychological assessments conducted during officer accession
3. **Survey Data:** Annual surveys to capture time-varying factors such as job satisfaction, career intentions, perceived leadership quality, and work-life balance
4. **Exit Interviews:** Detailed interviews with separating officers to capture qualitative insights on departure reasons
5. **Post-Separation Tracking:** Limited follow-up on career trajectories of officers after separation (where permissible)

Data would be integrated into a person-period format suitable for event history analysis, with one record per officer per time period (quarterly observations).

#### Analysis Approach

The analysis would employ a multi-method survival analysis approach:

1. **Descriptive Analysis:**
   - Kaplan-Meier survival curves to visualize retention patterns by branch, commissioning source, and other key variables
   - Cumulative incidence functions to examine competing risks (different types of separation)
   - Temporal patterns of attrition across career stages and historical periods

2. **Cox Proportional Hazards Modeling:**
   - Branch-specific models to identify risk factors for attrition unique to each division
   - Time-varying covariates to account for changing factors throughout officers' careers
   - Stratified models to account for potential violations of the proportional hazards assumption

3. **Discrete-Time Hazard Modeling:**
   - Logistic regression on person-period data to predict quarterly attrition probability
   - Multinomial logistic regression to model competing risks (different separation types)
   - Inclusion of branch-specific fixed effects and interactions

4. **Sequence Analysis:**
   - Optimal matching techniques to identify typical career trajectory patterns
   - Cluster analysis of career sequences to categorize career path typologies
   - Association of trajectory clusters with retention outcomes

5. **Machine Learning Extensions:**
   - Random forest survival models to identify non-linear relationships and interactions
   - Survival trees to identify critical decision points in officer careers

The analysis would specifically test for:
- Branch-specific retention factors
- Interaction between non-cognitive attributes and branch-specific requirements
- Time-varying effects of predictor variables across career stages
- Competing risks for different types of separations

#### Potential Findings

The study could potentially yield several important findings:

1. **Branch-Specific Retention Patterns:**
   - Identification of unique attrition timelines and risk periods for each branch (e.g., Aviation officers may show higher retention during specialized training periods but increased attrition after minimum service obligation completion)
   - Branch-specific protective factors (e.g., technical certification in Cyber Division may reduce attrition risk by 30%)
   - Differential impact of deployment on retention across branches

2. **Career Trajectory Typologies:**
   - Identification of 4-6 common career path patterns across branches
   - Association between early career experiences and long-term retention
   - Critical transition points where intervention would be most effective

3. **Non-Cognitive Predictors:**
   - TAPAS dimensions most predictive of retention in each branch (e.g., dominance may predict retention in Armor but not in Cyber)
   - Interaction between resilience measures and operational tempo in predicting retention
   - Changes in the predictive power of non-cognitive attributes across career stages

4. **Competing Risks Insights:**
   - Different predictor profiles for various separation types (medical, performance, misconduct)
   - Timing patterns showing when different types of attrition are most likely to occur
   - Branch differences in predominant separation reasons

5. **Intervention Timing:**
   - Identification of optimal timing for retention interventions by branch
   - Critical periods where retention risk spikes across all branches
   - Early warning indicators that precede separation decisions by 6-12 months

#### Potential Implications

The findings could have several significant implications for Army talent management:

1. **Tailored Retention Strategies:**
   - Development of branch-specific retention incentives targeting the unique factors driving attrition in each division
   - Personalized career counseling based on officer profiles and identified risk factors
   - Timing interventions to coincide with identified high-risk periods for specific officer types

2. **Selection and Assessment:**
   - Refinement of officer selection criteria to include non-cognitive attributes most strongly associated with retention in specific branches
   - Enhanced matching of officer candidates to branches based on predictive profiles
   - Improved identification of candidates likely to thrive in specific branch environments

3. **Career Path Design:**
   - Restructuring of career development programs to address critical attrition points
   - Creation of alternative career paths within branches to accommodate diverse motivations
   - Development of "bridge assignments" to facilitate retention during high-risk transition periods

4. **Leadership Development:**
   - Training programs for commanders focusing on factors within their control that influence retention
   - Building leadership awareness of branch-specific retention challenges
   - Cultivating leadership styles shown to enhance subordinate retention

5. **Organizational Policy:**
   - Evidence-based revisions to assignment policies to optimize retention
   - Family support programs targeted to address branch-specific work-life challenges
   - Operational tempo management informed by retention impact models

6. **Cost-Benefit Analysis:**
   - Quantification of the return on investment for various retention initiatives
   - Prioritization of interventions based on potential retention impact and implementation cost
   - Branch-specific benchmarking for retention targets based on realistic expectations

This study design would provide the Army with unprecedented insights into officer career trajectories across different branches, allowing for more strategic, evidence-based approaches to talent management and retention.

## Sources
[1] Predicting employee attrition and explaining its determinants https://www.sciencedirect.com/science/article/pii/S0957417425001976\
[2] Lack Of Career Development Drives Employee Attrition - Gartner https://www.gartner.com/smarterwithgartner/lack-of-career-development-drives-employee-attrition\
[3] How to Reduce Employee Attrition: 11 Strategies to Retain Your ... https://www.deel.com/blog/how-to-reduce-attrition-rate/\
[4] Prospecting the Career Development of Talents: A Survival Analysis ... https://www.kdd.org/kdd2017/papers/view/prospecting-the-career-development-of-talents-a-survival-analysis-perspecti\
[5] Introducing Survival and Event History Analysis - Sequence Analysis https://methods.sagepub.com/book/mono/introducing-survival-and-event-history-analysis/chpt/sequence-analysis\
[6] [PDF] Discrete-Time Methods for the Analysis of Event Histories Author(s) https://statisticalhorizons.com/wp-content/uploads/Allison.SM82.pdf\
[7] therneau/survival: Survival package for R - GitHub https://github.com/therneau/survival\
[8] lifelines — lifelines 0.30.0 documentation https://lifelines.readthedocs.io\
[9] Limitations of survival analysis - Cross Validated https://stats.stackexchange.com/questions/242477/limitations-of-survival-analysis\
[10] Attrition and reenlistment in the Army: Using the Tailored Adaptive ... https://pmc.ncbi.nlm.nih.gov/articles/PMC10013530/\
[11] Why Do Employees Stay? A Clear Career Path and Good Pay, for ... https://hbr.org/2017/03/why-do-employees-stay-a-clear-career-path-and-good-pay-for-starters\
[12] [PDF] An Analysis of Career Trajectories and Occupational Transitions https://www.dol.gov/sites/dolgov/files/OASP/evaluation/pdf/Building%20Better%20Pathways%20An%20Analysis%20of%20Career%20Trajectories%20and%20Occupational%20Transitions.pdf\
[13] [PDF] The Use of Event-History-Analysis in Career Research https://iisg.nl/publications/moderncareer-03.pdf\
[14] [PDF] Event History / Survival Analysis - Code Horizons https://codehorizons.com/wp-content/uploads/2020/04/SA-Online-Sample-Materials.pdf\
[15] Employee Attrition Explained: Types, Calculation, Impact, & Strategies https://www.clicdata.com/blog/employee-attrition/\
[16] [PDF] An Introduction to Event History Analysis - spia@uga.edu https://spia.uga.edu/faculty_pages/rbakker/pols8501/OxfordOneNotes.pdf\
[17] How to Use Data to Better Understand Attrition and Retention https://www.omnihr.co/blog/attrition-and-retention\
[18] Dynamic work trajectories and their interplay with family over the life ... https://pmc.ncbi.nlm.nih.gov/articles/PMC10250675/\
[19] Toxic Culture Is Driving the Great Resignation https://sloanreview.mit.edu/article/toxic-culture-is-driving-the-great-resignation/\
[20] Unraveling attrition and retention: A qualitative study with ... https://pmc.ncbi.nlm.nih.gov/articles/PMC11492032/\
[21] [PDF] The Effects of Perstempo on Officer Retention in the U.S. Military https://www.rand.org/content/dam/rand/pubs/monograph_reports/2007/MR1556.pdf\
[22] [PDF] department of the army career engagement survey https://talent.army.mil/wp-content/uploads/2023/09/DACES-Third-Annual-Report_Final.pdf\
[23] [PDF] Event History Analysis - NCRM EPrints Repository https://eprints.ncrm.ac.uk/id/eprint/4467/1/MethodsReviewPaperNCRM-004.pdf\
[24] [PDF] The Contribution of Life Course Research, Part II: Causation as ... https://emergingtrends.stanford.edu/files/original/2c61672d320e9a6fc63a6a58177377560de64b7d.pdf\
[25] Survival Analysis Using SAS: A Practical Guide, Second Edition https://www.goodreads.com/book/show/8333054-survival-analysis-using-sas\
[26] Employee-Turnover-Insights-using-Survival-Analysis - GitHub https://github.com/razamehar/Employee-Turnover-Insights-using-Survival-Analysis\
[27] Understanding Life-Course Analysis - Doc McKee https://docmckee.com/oer/soc/sociology-glossary/life-course-analysis-definition/\
[28] Introducing Survival and Event History ... - Sage Research Methods https://methods.sagepub.com/book/mono/introducing-survival-and-event-history-analysis/back-matter/d239\
[29] Event History Analysis - Sage Research Methods https://methods.sagepub.com/book/mono/event-history-analysis/toc\
[30] Event History and Survival Analysis - Sage Research Methods https://methods.sagepub.com/book/mono/event-history-analysis-2e/toc\
[31] [PDF] Event History Analysis - Statistical Horizons https://statisticalhorizons.com/wp-content/uploads/EventHistoryChapter_HandbookOfDataAnalysis.pdf\
[32] Event History Analysis With Stata - Google Books https://books.google.com/books/about/Event_History_Analysis_With_Stata.html?id=tolbBAAAQBAJ\
[33] "Event History & Survival Analysis" - Penn Arts & Sciences https://www.sas.upenn.edu/~allison/Allison2.html\
[34] [PDF] Analysis of Officer Retention and Success in the US Army by ... https://digitalcommons.uri.edu/cgi/viewcontent.cgi?article=1886&context=srhonorsprog\
[35] [PDF] army officer retention: historical context https://talent.army.mil/wp-content/uploads/pdf_uploads/course-material/Retaining-Officer-Talent-Historical-Context.pdf\
[36] So honestly though, is Officer retention really that bad? : r/army https://www.reddit.com/r/army/comments/1e7ht83/so_honestly_though_is_officer_retention_really/\
[37] Sustaining a resilient force through retention - Army.mil https://www.army.mil/article-amp/149542/sustaining_a_resilient_force_through_retention\
[38] [PDF] An Analysis of the Effect of Commissioning Sources on Retention ... https://apps.dtic.mil/sti/tr/pdf/ADA424559.pdf\
[39] Minority officers stay in the Army longer, receive fewer promotions https://taskandpurpose.com/news/army-minority-retention-promotion-study/\
[40] [PDF] Analysis of First-Term Army Attrition. - DTIC https://apps.dtic.mil/sti/tr/pdf/ADA362968.pdf\
