---
title: Promotion Board Analysis for Analyzing Career Trajectories
format: latex
---

Promotion Board Analysis offers a powerful methodological framework for understanding the factors that shape military career trajectories and promotion outcomes. By combining rigorous statistical approaches with comprehensive data on officer careers, this methodology can provide valuable insights for both organizational leadership and individual officers. The approach is particularly valuable for identifying optimal developmental pathways, understanding the relative importance of different career experiences, and ensuring alignment between stated promotion criteria and actual promotion outcomes.

## 1. Approach Description & Goal

Promotion Board Analysis is a methodological approach that examines the decision-making processes and outcomes of formal promotion systems, particularly in hierarchical organizations like the military. This approach systematically analyzes the factors that influence promotion decisions, the patterns in promotion rates across different groups, and the relationship between promotion outcomes and various career and personal attributes.

The primary goals of Promotion Board Analysis include: (1) understanding which factors most significantly impact promotion success; (2) identifying potential biases or inconsistencies in the promotion system; (3) predicting future promotion outcomes and career trajectories; (4) informing policy decisions related to professional development and talent management; and (5) optimizing organizational human resource practices to ensure fair and merit-based advancement opportunities.

In military contexts, this approach is particularly valuable as promotion boards operate according to structured processes with clearly defined criteria, providing rich data for statistical analysis. The approach typically combines quantitative methods like survival analysis, logistic regression, and multi-state modeling with qualitative assessments of promotion board documentation and policies.

## 2. Critical Variables

Promotion Board Analysis typically incorporates several categories of variables as inputs:

**Personal Demographics**: 
- Age/year group
- Gender
- Race/ethnicity
- Marital status and family composition

**Educational Background**:
- Commissioning source (military academy, ROTC, OCS)
- Education level (bachelor's, master's, doctorate)
- Academic performance metrics (GPA, class rank)
- Academic major/specialization
- Advanced military education completion

**Professional Qualifications**:
- Time in service and time in grade
- Key developmental positions held
- Command time and staff experience
- Joint service assignments
- Deployment experience (locations, duration, combat vs. non-combat)

**Performance Metrics**:
- Evaluation report ratings
- Awards and decorations
- Physical fitness scores
- Specialized skills and certifications

**Career Management Factors**:
- Branch/specialty alignment with organizational needs
- Career field/branch transfers
- Utilization of talent management programs
- Prior enlisted service experience
- Mentorship relationships

**External Factors**:
- Promotion opportunity percentages
- Year-specific policies and focus areas
- Organizational structure changes
- War/peacetime context

The analysis typically examines these variables both individually and in combination to understand their relative influence on promotion outcomes and career trajectories.

## 3. Key Overviews

McAllaster's "Forecasting Army Officer Attrition with Logistic Regression Using The SAS System" (1999) provides a foundational overview of applying statistical methods to military personnel analysis. The paper explains how Army personnel analysts model and forecast officer attrition using logistic regression, applying this approach to predict binary outcomes (whether officers stay or leave the Army). McAllaster's methodology involves analyzing over 150 homogeneous cohorts of officers using 14 years of legacy data. The paper demonstrates how SAS Software can be leveraged to summarize vast amounts of data (over a million observations), model binomial outcomes and forecast trends using logistic regression, and repeat the statistical analysis code using macro language. This work established important analytical frameworks for understanding career trajectories within the military context[5].

Putter and colleagues' application of multi-state models in their R package 'mstate' (2024) provides a comprehensive methodological framework for analyzing career transitions. Their approach extends beyond simple binary outcomes to model complex career trajectories with multiple possible states and transitions. The package implements functions for data preparation, descriptive statistics, hazard estimation, and prediction using either Aalen-Johansen estimators or simulation techniques. Their methodology is particularly suited for analyzing competing risks (such as promotion versus attrition) and multi-state transitions (such as movements between different ranks or positions). This statistical approach provides researchers with tools to understand not just whether officers are promoted but also the timing and sequencing of career events[10].

In "Analysis of the Survival Patterns of United States Naval Officers," researchers conduct a comprehensive survival analysis on officer cohorts who entered service between 1983 and 1990. The study employs three survival analysis procedures—LIFETEST, LIFEREG, and PHREG—to examine factors influencing officer career longevity. The research findings demonstrate that commissioning source has significant effects on survival rates, with Naval Academy graduates showing better retention than officers from other commissioning sources. The study provides valuable insights into how demographic variables (gender, race), educational background, and career specialization affect officer retention, showing different patterns for voluntary versus involuntary separations. This work establishes survival analysis as a powerful tool for understanding military career trajectories[6].

"The Impact of Removing Demographic Indicators from Military Promotion Boards" (2024) presents findings from a comprehensive study conducted by the Institute for Defense Analyses (IDA) on potential bias in military promotion systems. Using a mixed-methods approach, IDA researchers analyzed historical officer promotion data across all military branches to assess whether removing demographic indicators from promotion board materials would reduce bias. After controlling for various factors including rank, year, and competitive category, their analysis found that past policy changes removing some demographic indicators did not significantly impact promotion rates for minority officers. The study also examined how names potentially indicative of minority status predicted promotion outcomes, finding no significant associations. This research provides important methodological insights into how to analyze potential bias in promotion systems[7].

## 4. Mathematical Approach

Promotion Board Analysis employs several statistical methodologies to model and analyze career progression, with the most common approaches being survival analysis, logistic regression, and multi-state modeling.

**Survival Analysis / Event History Analysis**:
This approach models the time until an event of interest (such as promotion) occurs. The basic concept involves estimating the survival function:

$$ S(t) = Pr(T > t) $$

which represents the probability that an officer's time to promotion (T) exceeds a specified time (t). The hazard function, representing the instantaneous rate of promotion at time t given survival up to that point, is defined as:

$$ h(t) = \lim_{\Delta t \to 0} \frac{Pr(t \leq T < t + \Delta t | T \geq t)}{\Delta t} $$

The Cox proportional hazards model, a semi-parametric approach commonly used in Promotion Board Analysis, relates the hazard function to a set of covariates:

$$ h(t|X) = h_0(t) \exp(\beta_1 X_1 + \beta_2 X_2 + ... + \beta_p X_p) $$

where h₀(t) is the baseline hazard function and X₁, X₂, ..., Xₚ are covariates (such as educational background, performance ratings, etc.).

**Logistic Regression**:
For binary outcomes (promoted vs. not promoted), logistic regression models the log-odds of promotion as a linear function of predictor variables:

$$ \log\left(\frac{p}{1-p}\right) = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + ... + \beta_p X_p $$

where p is the probability of promotion, and X₁, X₂, ..., Xₚ are predictor variables. The coefficients (β) represent the change in log-odds associated with a one-unit increase in the corresponding predictor.

**Multi-state Modeling**:
This approach models transitions between different career states (e.g., Lieutenant to Captain to Major, or active duty to separation). The transition intensity or hazard from state r to state s is defined as:

$$ \alpha_{rs}(t|Z) = \lim_{\Delta t \to 0} \frac{P(S(t + \Delta t) = s | S(t) = r, Z)}{\Delta t} $$

where S(t) is the state at time t and Z represents covariates. These transition intensities can be modeled using Cox-type models:

$$ \alpha_{rs}(t|Z) = \alpha_{rs,0}(t) \exp(\beta_{rs}^T Z) $$

**Competing Risks Analysis**:
In the military context, officers face multiple possible career outcomes (promotion, voluntary separation, involuntary separation, etc.). Competing risks analysis, a specialized form of survival analysis, models the cause-specific hazard for each possible outcome:

$$ h_k(t) = \lim_{\Delta t \to 0} \frac{P(t \leq T < t + \Delta t, K = k | T \geq t)}{\Delta t} $$

where K represents the specific type of event (e.g., K=1 for promotion, K=2 for voluntary separation).

**Practical Implementation**:
In practice, Promotion Board Analysis often involves:
1. Data preparation, including creation of person-period datasets
2. Descriptive analysis using Kaplan-Meier survival curves to visualize promotion rates over time
3. Model fitting using Cox proportional hazards models or logistic regression
4. Model validation and diagnostics
5. Interpretation of coefficients to identify significant predictors of promotion
6. Prediction of future promotion outcomes for individuals or cohorts

These mathematical approaches allow researchers to quantify the effects of various factors on promotion outcomes while accounting for the time-dependent nature of career progression.

## 5. Example Applications

"Analysis of the Survival Patterns of United States Naval Officers" presents a comprehensive application of survival analysis to understand officer retention and career trajectories in the U.S. Navy. The study analyzed officer cohorts who entered service between 1983 and 1990, using Navy Officer Data Card information and annual promotion board results. Three survival analysis procedures—LIFETEST, LIFEREG, and PHREG—were employed to examine factors influencing career longevity. Key findings revealed that commissioning source significantly affects survival rates, with Naval Academy graduates showing better retention than officers from other sources. Interestingly, the research found that females and African-Americans demonstrated better survival rates than males and whites, and that prior enlisted personnel and older officers had higher survival rates. When analyzing voluntary and involuntary separations separately, the factors showed different effects—for example, being African-American had negative effects on involuntary separations but positive effects on voluntary separations. This study exemplifies how survival analysis can provide nuanced insights into the complex interplay of factors affecting military career trajectories[6].

"An Analysis of Selected Army Promotion Board Results" examines Army officer professional development by analyzing Lieutenant Colonel promotion board outcomes. The study focuses on comparing the pre-OPMS (Officer Personnel Management System) and OPMS approaches to officer development, specifically investigating whether OPMS is meeting its stated goals through promotion patterns. The research methodology involved contingency table analysis and individual tests for differences in proportions for each specialty listed as over or under aligned at the time of the promotion board's convening. A key finding was that promotion under OPMS was not alleviating specialty alignment problems for the analyzed lists. The researchers recommended a two-step course of action focused on providing better guidance to promotion boards to address specialty alignment issues. This study demonstrates how analyzing promotion board results can reveal systemic issues in career management systems and inform policy recommendations[18].

"Forecasting Army Officer Attrition with Logistic Regression" details how Army personnel analysts model and predict officer career decisions using logistic regression. The paper explains a statistical application that employs a simple logistic regression model with fiscal year as the predictor variable to forecast whether officers stay or leave the Army. Despite the simplicity of the underlying model, the complete application is described as large and complex because it runs logistic regression against more than 150 homogeneous officer cohorts. The methodology includes a semi-automatic capability to identify and exclude inappropriate outliers through SAS Macro Language. This approach demonstrates how statistical modeling can process vast amounts of historical data (fourteen years and over a million observations) to identify patterns and predict future outcomes in military career trajectories. The application showcases how logistic regression can be applied at scale to inform workforce planning and talent management in large organizations[5].

"The Impact of Removing Demographic Indicators from Military Promotion Boards" presents findings from an Institute for Defense Analyses (IDA) study examining whether removing race, ethnicity, and gender identifiers from promotion board materials would reduce bias in military promotion systems. IDA researchers analyzed historical officer promotion data across all military branches, specifically examining the impact of past policy changes that removed certain demographic indicators (such as candidate photos) on minority officer promotion rates. After controlling for rank, year, competitive category, and linear time trends, the analysis found that these policy changes did not significantly impact promotion rates for minority officers relative to non-minority officers. Additionally, the researchers examined whether names potentially indicative of minority status predicted promotion outcomes, finding no significant associations. The study concluded that completely removing all identifying information would be highly challenging from a feasibility standpoint and might not be the most effective approach to reducing bias. This research provides valuable insights into methodological approaches for analyzing potential bias in promotion systems and evaluating the effectiveness of policy interventions[7].

## 6. Critiques

Promotion Board Analysis, while valuable for understanding career trajectories, faces several significant limitations that researchers should consider when employing this methodology.

**Data Limitations**: A fundamental challenge in Promotion Board Analysis is access to complete, accurate, and timely data. Military personnel records may contain inconsistencies, missing values, or measurement errors that compromise analysis quality. As noted in the study of Army promotion board results, researchers often struggle to "accurately identify in the data base used those officers who were considered for promotion"[18]. Additionally, longitudinal data spanning entire careers may be unavailable or incomplete, particularly for specialized career fields or during periods of organizational change.

**Endogeneity and Selection Bias**: Promotion outcomes are not randomly distributed but result from complex selection processes that may already incorporate many of the variables being studied. Officers self-select into different career tracks, and their decisions regarding education, assignments, and specialization are endogenous to their promotion prospects. This creates challenges in isolating causal effects of specific factors on promotion outcomes. As demonstrated in the naval officer survival patterns study, there are significant differences in survival rates between voluntary and involuntary separations that complicate interpretation of career trajectory patterns[6].

**Changing Organizational Contexts**: Military promotion systems evolve over time with changing policies, priorities, and organizational structures. This temporal instability makes it difficult to compare promotion patterns across different time periods or to build models with consistent predictive validity. The IDA study on demographic indicators in promotion boards notes that "promotion boards have already adopted many best practices to mitigate bias," suggesting that the promotion system itself is a moving target for analysis[7].

**Limited Insight into Decision Processes**: Quantitative analysis of promotion outcomes provides limited insight into the actual decision-making processes of promotion boards. The deliberations of board members are typically confidential, and the weights assigned to different factors may vary across boards and individuals. This "black box" aspect limits researchers' ability to fully understand how different variables influence promotion decisions in practice.

**Methodological Challenges**: The statistical methods commonly used in Promotion Board Analysis have their own limitations. Survival analysis and logistic regression both require assumptions about the functional form of relationships and the distribution of residuals that may not hold in practice. Additionally, these methods may struggle to capture complex, non-linear relationships or interaction effects between variables that influence promotion outcomes.

**External Validity Concerns**: Findings from Promotion Board Analysis in one military branch or time period may not generalize to other contexts. For example, factors that predict promotion success for Army officers may differ from those for Navy officers, or patterns observed during peacetime may differ from those during conflict periods.

These limitations suggest that Promotion Board Analysis should be complemented with other methodological approaches, including qualitative studies of promotion board proceedings, experimental designs testing specific hypotheses about promotion decisions, and comparative studies across different organizational contexts.

## 7. Software

**R 'survival' Package**: The 'survival' package is a cornerstone tool for analyzing time-to-event data in R, maintained primarily by Terry Therneau. As described in the CRAN documentation, this package contains "core survival analysis routines, including definition of Surv objects, Kaplan-Meier and Aalen-Johansen (multi-state) curves, Cox models, and parametric accelerated failure time models"[9]. The package offers functionality for handling right-censored, left-censored, and interval-censored data, as well as time-dependent covariates—features that are particularly valuable for analyzing military career trajectories where some officers' outcomes may be censored (e.g., still serving at the end of the observation period). The 'survival' package provides robust visualization capabilities for survival curves and includes methods for model diagnostics and validation. Its integration with other R packages makes it suitable for comprehensive analyses of promotion patterns and career duration.

**R 'mstate' Package**: Developed by Hein Putter and colleagues, the 'mstate' package extends survival analysis capabilities in R to handle multi-state models and competing risks. According to CRAN documentation, mstate "contains functions for data preparation, descriptives, hazard estimation and prediction with Aalen-Johansen or simulation in competing risks and multi-state models"[10]. This package is particularly valuable for military career analysis because it can model complex transitions between different ranks and positions while accounting for competing outcomes like voluntary separation, involuntary separation, or retirement. The package facilitates the creation of transition matrices, state occupation probabilities, and expected length of stay in each state. For researchers studying officer career trajectories, 'mstate' provides tools to understand not just whether officers are promoted but also the timing and sequencing of career events within a unified analytical framework.

**Python 'lifelines' Package**: The 'lifelines' library is a comprehensive Python package for survival analysis, offering functionality similar to R's 'survival' package but within the Python ecosystem. As demonstrated in the documentation, 'lifelines' provides implementations of various survival models including Kaplan-Meier estimators, Cox Proportional Hazard models, and parametric survival models[11]. The package includes tools for visualizing survival curves, comparing survival functions across groups, and performing statistical tests to assess differences in survival distributions. 'lifelines' offers good integration with other Python data science libraries such as pandas and scikit-learn, making it suitable for incorporation into broader data analysis workflows. For military promotion analysis, 'lifelines' provides an accessible entry point for Python users to model time-to-promotion and identify factors influencing career advancement.

**SAS System**: The SAS System provides comprehensive capabilities for survival analysis and logistic regression through procedures like PROC LIFETEST, PROC LIFEREG, PROC PHREG, and PROC GENMOD. As demonstrated in McAllaster's paper on forecasting Army officer attrition, SAS is particularly powerful for analyzing large, complex datasets with multiple cohorts[5]. The system's macro language capabilities enable repeatable analyses across different subgroups, which is valuable when examining promotion patterns across different military branches or specialties. SAS also offers advanced capabilities for handling complex survey designs, missing data, and longitudinal analysis. While proprietary and more expensive than open-source alternatives, SAS remains widely used in government and military settings where its validated procedures, comprehensive documentation, and technical support make it a preferred choice for mission-critical analyses of personnel data.

**Custom Military Analysis Tools**: Beyond general-purpose statistical software, various military organizations have developed custom tools for analyzing promotion data. These specialized applications typically integrate with military personnel databases and incorporate service-specific business rules and policies. For example, the Air Force Reserve Personnel Center uses specialized tools to calculate "promotion eligibility criteria" and track the "entire promotion process for each board"[2]. Similarly, the Army's Military Personnel Center publishes specialized analyses of "specialty alignment" that inform promotion planning[18]. These custom tools, while not generally available to academic researchers, represent important components of the software ecosystem for Promotion Board Analysis within military organizations. They often incorporate service-specific methods for calculating promotion zones, eligibility, and selection criteria that supplement the more general analytical capabilities of commercial statistical packages.

## 8. Example Study Design

### Key Variables

**Officer Demographic Variables**:
- Year group/commissioning cohort
- Gender
- Race/ethnicity
- Prior enlisted service status
- Commissioning source (Military Academy, ROTC, OCS)
- Education level and academic discipline

**Branch-Specific Developmental Indicators**:
- *Armor*: Vehicle qualification levels, gunnery scores, combat deployments as armor officer
- *Logistics*: Supply chain certification levels, joint logistics experience, support operation assignments
- *Aviation*: Flight hours by aircraft type, instructor pilot status, aviation maintenance experience
- *Cyber*: Technical certifications, civilian-equivalent qualifications, specialized training completion

**Career Milestone Variables**:
- Timing of key developmental (KD) position completion
- Duration in KD positions (24-36 months suggested for "Most Qualified" status)[1]
- Command time at company/battalion levels
- Joint service assignment completion
- Advanced military education timing and performance

**Performance Metrics**:
- Officer evaluation report scores and narrative assessment
- Awards and decorations (categorized by type and significance)
- Selection for specialized programs or fellowships
- Previous below-zone promotion selections

**Non-Cognitive Attributes**:
- Leadership assessment scores
- Peer evaluations (if available)
- Subordinate feedback measures
- Mentorship and talent development activities

### Sample & Data Collection

The study will analyze a comprehensive dataset of U.S. Army officers across the four branch divisions (Armor, Logistics, Aviation, and Cyber) who were eligible for promotion to Lieutenant Colonel (O-5) during fiscal years 2020-2025. This timeframe provides recent data while allowing for analysis of promotion outcomes across multiple board cycles.

Data collection will involve aggregating information from multiple authoritative sources:
1. The Officer Record Brief (ORB) for demographic and career history information
2. The Official Military Personnel File (OMPF) for performance evaluations and awards
3. Branch-specific databases for specialized qualifications and metrics
4. Army promotion board results identifying selected and non-selected officers
5. Post-board statistical reports indicating promotion rates by various categories

For each officer in the dataset, we will collect comprehensive career history data from commissioning through the promotion board consideration date. This longitudinal approach allows for time-dependent analysis of career trajectories and enables the identification of critical developmental timing effects.

A stratified random sampling approach will ensure adequate representation across all four branches, with oversampling of smaller branches (particularly Cyber) to enable meaningful statistical analysis within each branch category. The target sample size is 2,000 officers per branch, for a total sample of 8,000 officers, providing sufficient statistical power for both branch-specific and cross-branch analyses.

### Analysis Approach

The analysis will employ a multi-method approach combining survival analysis, logistic regression, and multi-state modeling to comprehensively examine promotion patterns and career trajectories:

**Step 1: Descriptive Analysis**
- Generate Kaplan-Meier survival curves to visualize time-to-promotion patterns by branch, demographic groups, and other key variables
- Conduct preliminary comparative analyses to identify potential differences in promotion rates across branches and subgroups
- Perform exploratory data analysis to identify potential collinearity among predictors and inform subsequent modeling decisions

**Step 2: Cox Proportional Hazards Modeling**
- Develop branch-specific Cox models predicting time-to-promotion using relevant predictors
- Test the proportional hazards assumption and implement time-dependent covariates where appropriate
- Examine interaction effects between branch-specific development indicators and general career factors

**Step 3: Logistic Regression Analysis**
- Implement logistic regression models predicting in-zone promotion selection (binary outcome)
- Compare model specifications to identify the most influential predictors of promotion success
- Calculate adjusted odds ratios to quantify the impact of specific developmental experiences on promotion likelihood

**Step 4: Multi-state Modeling**
- Develop multi-state models capturing transitions between career states (e.g., company command → battalion XO → battalion command)
- Calculate state occupation probabilities and transition intensities between states
- Identify optimal career progression pathways associated with promotion success

**Step 5: Competing Risks Analysis**
- Model competing outcomes including promotion, voluntary separation, and involuntary separation
- Calculate cause-specific hazards for each outcome type
- Identify factors that differentially predict various career outcomes

**Step 6: Integration and Interpretation**
- Synthesize findings across analytical approaches to identify consistent patterns
- Develop branch-specific career progression models
- Compare results to official career progression guidance to identify alignment or misalignment

### Potential Findings

The analysis is expected to yield several categories of findings:

**Branch-Specific Developmental Patterns**:
- The analysis may reveal that Armor officers with combined arms experience and combat deployments have significantly higher promotion rates than those without such experience
- For Logistics officers, joint logistics assignments may emerge as more predictive of promotion than branch-specific assignments
- Aviation officers might show a non-linear relationship between flight hours and promotion likelihood, with diminishing returns beyond a certain threshold
- Cyber officers with industry certifications and operational experience might demonstrate higher promotion rates than those focused solely on technical specialization

**Timing Effects**:
- The analysis may identify optimal timing windows for completing key developmental positions, potentially differing by branch
- Early completion of advanced military education might show stronger positive effects for some branches than others
- Time spent in joint assignments might demonstrate differential returns across branches

**Demographic Influences**:
- The study might reveal whether demographic factors continue to influence promotion outcomes after controlling for performance and developmental variables
- Different commissioning sources might be associated with different career trajectory patterns across branches

**Integration of Non-Cognitive Attributes**:
- Leadership assessments might emerge as stronger predictors of promotion in command-centric branches like Armor
- Technical problem-solving abilities might show stronger associations with promotion success in Cyber

**Cross-Branch Comparisons**:
- The analysis may identify common factors that predict promotion success across all branches, such as joint service experience
- Branch-specific factors might explain varying proportions of promotion variance, potentially indicating differences in promotion board emphasis

**Career Trajectory Typologies**:
- The multi-state modeling approach might identify distinct "career trajectory types" associated with higher promotion likelihood
- These typologies might differ substantially across branches, suggesting different optimal paths to success

### Potential Implications

**Career Management Policy**:
- Findings could inform updates to branch-specific career maps and developmental timelines published by the Army
- Results might suggest modifications to the "Most Qualified Looks Like" guidance provided to promotion boards[1]
- Analysis could identify misalignments between stated career progression policies and actual promotion outcomes

**Officer Development Programs**:
- Results could guide branch-specific adjustments to officer development programs and assignment priorities
- Findings might inform branch managers about optimal timing and sequencing of key developmental experiences
- The analysis could highlight developmental gaps that should be addressed through new training or assignment opportunities

**Promotion Board Guidance**:
- Findings could inform more precise guidance to promotion boards about how to evaluate branch-specific accomplishments
- Results might suggest adjustments to promotion board composition to ensure appropriate expertise in evaluating specialized experiences
- Analysis could identify potential unintended consequences of current promotion criteria

**Talent Management Initiatives**:
- The identification of successful career trajectory patterns could inform talent marketplace algorithms and assignment prioritization
- Findings might suggest opportunities for cross-branch developmental assignments that enhance promotion potential
- Results could inform retention incentives targeting officers with high-potential career trajectories

**Organizational Equity and Effectiveness**:
- Analysis might identify systemic barriers to advancement for certain demographic groups that need to be addressed
- Findings could help ensure that promotion outcomes align with the Army's strategic talent needs, especially in evolving domains like Cyber
- Results might suggest adjustments to how non-traditional career paths are evaluated by promotion boards

## Sources
[1] [PDF] CMF 12 Career Progression Chart - Army.mil https://api.army.mil/e2/c/downloads/2023/08/09/73f99ae3/cmf-12-board-products-8-aug-23.pdf\
[2] Officer Promotion Boards - Air Reserve Personnel Center https://www.arpc.afrc.af.mil/Services/Officer-Promotion-Boards/\
[3] Understanding The Army Prootion Review Board (PRB) https://www.mcmilitarylaw.com/understanding-the-army-promotion-review-board-prb/\
[4] Career Management for the Army Reserve Officer | Article - Army.mil https://www.army.mil/article/253844/career_management_for_the_army_reserve_officer\
[5] [PDF] 1 Forecasting Army Officer Attrition with Logistic Regression Using ... http://www8.sas.com/scholars/05/PREVIOUS/1999/pdf/072.pdf\
[6] [PDF] Analysis of the Survival Patterns of United States Naval Officers - DTIC https://apps.dtic.mil/sti/tr/pdf/ADA432824.pdf\
[7] [PDF] The Impact of Removing Demographic Indicators from Military ... - IDA https://www.ida.org/-/media/feature/publications/t/th/the-impact-of-removing-demographic-indicators-from-military-promotion-boards/3003198.ashx\
[8] [PDF] The Use of Event-History-Analysis in Career Research https://iisg.nl/publications/moderncareer-03.pdf\
[9] CRAN: Package survival - R Project https://cran.r-project.org/package=survival\
[10] Package mstate - CRAN https://cran.r-project.org/package=mstate\
[11] Introduction to survival analysis — lifelines 0.30.0 documentation https://lifelines.readthedocs.io/en/latest/Survival%20Analysis%20intro.html\
[12] Officer career progression question : r/army - Reddit https://www.reddit.com/r/army/comments/afz6xl/officer_career_progression_question/\
[13] Headquarters RIO > Career Management > Promotions https://www.hqrio.afrc.af.mil/Career-Management/Promotions/\
[14] Promotion Board Approval Process - MyNavyHR https://www.mynavyhr.navy.mil/Career-Management/Boards/General-Board-Info/Promotion-Board-Approval-Process/\
[15] [PDF] career progression and promotion board math https://mccareer.org/wp-content/uploads/2019/06/3-career-progression-and-promotion-board-math.pdf\
[16] Officer Promotions - HRC https://www.hrc.army.mil/content/5789\
[17] Promotion Boards - RAND Corporation https://www.rand.org/paf/projects/dopma-ropma/promotion-and-appointments/promotion-boards.html\
[18] [PDF] An Analysis of Selected Army Promotion Board Results. - DTIC https://apps.dtic.mil/sti/tr/pdf/ADA070262.pdf\
