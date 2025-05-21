---
title: Mentorship and Sponsorship Studies for Career Trajectory Analysis
format: latex
---

Mentorship and sponsorship studies represent a powerful approach to understanding how interpersonal developmental relationships shape professional growth and career advancement. This comprehensive report outlines the methodology, applications, and implications of using mentorship and sponsorship frameworks to analyze career trajectories, with specific attention to their potential application in understanding military career paths.

## Approach Description & Goal

Mentorship and sponsorship studies analyze how interpersonal developmental relationships influence career trajectories, mobility patterns, and professional success. This approach distinguishes between different types of supportive relationships—mentorship (providing guidance, advice, and wisdom), sponsorship (advocating and creating opportunities), and coaching (developing specific skills)—and examines their differential impact on career outcomes[17][20]. The primary goal is to understand how these structured relationships affect career development across various dimensions including advancement rates, professional identity formation, skill acquisition, networking opportunities, and long-term career satisfaction[6][2]. This approach recognizes that careers are rarely solo journeys but are shaped by a portfolio of relationships that provide different forms of support at critical junctures[12]. By mapping these developmental networks and understanding their structure and function, researchers can identify patterns that lead to more successful career outcomes and design interventions to enhance career development systems within organizations[17].

## Critical Variables

Mentorship and sponsorship studies typically incorporate several categories of variables to comprehensively analyze career trajectories:

### Relationship Characteristics
These variables capture the nature of developmental relationships including type (mentor, sponsor, or coach), duration, formality (formal programs versus informal relationships), frequency of interaction, and relationship quality[17][20]. The content of support provided is also measured, typically divided into career functions (advocacy, coaching, challenging assignments) and psychosocial functions (role modeling, counseling, acceptance)[12][2].

### Network Structure
These variables examine the composition of an individual's entire developmental network, including network size (number of developers), diversity (range of social systems represented), strength of ties, and density (interconnections among developers)[12][5]. These structural characteristics help understand how different network configurations affect career outcomes.

### Career Outcomes
These variables measure the impact of developmental relationships on career progression, including promotion rates, job satisfaction, career opportunities, recognition and visibility, retention, and perceived career success[6][2]. Both objective measures (salary, position) and subjective measures (satisfaction, identity clarity) are typically included to capture the multidimensional nature of career success.

### Individual Characteristics
These variables account for personal factors that may influence both the formation of developmental relationships and career outcomes, including demographics (gender, race/ethnicity), career stage, prior experience, personality traits, and social capital[16][17]. These variables help identify how mentorship and sponsorship dynamics may differ across diverse populations.

### Organizational Context
These variables capture the environmental factors that shape developmental relationships, including organizational culture, formal mentoring programs, reward structures, and industry characteristics[17][20]. These contextual factors help explain variations in mentorship and sponsorship patterns across different settings.

## Key Overviews

"Does Mentoring Matter? A Multidisciplinary Meta-Analysis Comparing Mentored and Non-Mentored Individuals" presents a comprehensive meta-analysis examining mentoring outcomes across youth, academic, and workplace domains. The study analyzes whether mentoring relationships produce meaningful benefits and how these benefits vary across contexts. The findings demonstrate that mentoring is associated with numerous favorable outcomes, including behavioral, attitudinal, health-related, relational, motivational, and career benefits, though effect sizes are generally small. Notably, the research found larger positive effects for academic and workplace mentoring compared to youth mentoring. This landmark study addresses the fragmentation of mentoring research across disciplinary silos, providing a holistic view of mentoring's impact and establishing a foundation for more targeted investigations of mentoring's role in career development[6].

"Celebrating Mentoring! A Developmental Network Perspective" by Monica Higgins introduces an innovative framework that reconceptualizes mentoring beyond traditional dyadic relationships. The presentation argues that rather than relying on a single mentor, individuals benefit from cultivating a diverse "developmental network" or "personal board of directors" comprising multiple supportive relationships. Higgins distinguishes between traditional mentoring approaches (hierarchical, single relationships, intra-organizational) and developmental network perspectives (multilevel, multiple networked relationships, both internal and external to organizations). The framework categorizes mentoring benefits into "soft" outcomes (work satisfaction, professional identity clarity, self-efficacy) and "hard" outcomes (career opportunities, recognition, promotion rates), while differentiating between career help (advocacy, coaching, challenging assignments) and psychosocial help (role modeling, counseling, friendship). This reconceptualization expands our understanding of how diverse developmental relationships collectively influence career trajectories[12].

"How to Sponsor, Coach, and Mentor: A Qualitative Study With Faculty" examines how sponsoring, coaching, and mentoring (SCM) function as distinct faculty development tools. Through qualitative interviews with 20 family medicine department chairs, the researchers identify specific actions associated with each role. Sponsors perform six main actions: identifying opportunities, recognizing strengths, encouraging opportunity-seeking, offering tangible support, optimizing candidacy, and nominating candidates. Coaches perform seven actions: clarifying, advising, providing resources, critical appraisal, giving feedback, reflecting, and scaffolding. Mentors engage in checking in, listening, sharing wisdom, directing, supporting, and collaborating. The study emphasizes that these functions should be performed intentionally and can be evaluated for effectiveness. By clarifying these distinct yet complementary roles, the research provides a framework for understanding how different types of developmental relationships serve specific career advancement functions[17].

"Mentorship, Sponsorship, and Coaching for Trainee Career Development" provides a practical overview of the three main forms of professional relationships for career advancement in academic medicine. The article defines mentorship as sharing wisdom and advice based on personal experience, either through traditional hierarchical relationships or newer "mosaic mentorship" networks. Sponsorship is described as influential professionals providing episodic public support to advance careers, such as nominating for awards or opportunities. Coaching focuses on developing concrete technical skills through periodic, iterative instruction. For each relationship type, the article details how to secure these relationships, their specific benefits, characteristics of successful relationships, and potential pitfalls. This comprehensive framework demonstrates how different developmental relationships serve complementary functions across career stages and contexts, offering practical guidance for both those seeking support and those in positions to provide it[20].

## Mathematical Approach

Mentorship and sponsorship studies employ several quantitative methods to analyze the structure and impact of developmental relationships on career trajectories:

### Social Network Analysis (SNA)
SNA examines the structure and patterns of relationships within a network of individuals. In mentorship studies, SNA measures how mentoring ties connect individuals across organizations, departments, or career stages[5]. Key mathematical constructs include:

- **Network Density (D)**: D = 2L/[N(N-1)], where L is the number of observed ties and N is the number of nodes, measuring the proportion of potential connections that are actually present.
- **Centralization**: Measures the extent to which a network revolves around a few central individuals.
- **Components**: Identifies distinct, connected subgroups within the overall network.
- **Centrality Measures**: Including degree centrality (number of connections), betweenness centrality (bridging role), and eigenvector centrality (connection to well-connected others).

These metrics help assess the cohesiveness, hierarchical structure, and connectivity of mentorship networks[5].

### Sequence Analysis
This approach analyzes career patterns by examining the similarity between career sequences and grouping them into typical trajectories. Optimal Matching Analysis (OMA) is commonly used to measure the similarity between two sequences by calculating the "cost" of transforming one sequence into another[16]. The mathematical formula for calculating the distance between sequences A and B is:

d(A,B) = min{∑ c(ai → bj)}, where c represents the cost of substituting, inserting, or deleting elements to transform sequence A into sequence B.

After calculating pairwise distances between all sequences, clustering algorithms (hierarchical, k-means, etc.) group similar sequences into career patterns. This approach captures timing, duration, and transitions between career states, producing a typology of career paths[14][16].

### Stochastic Actor-Oriented Models (SAOM)
For longitudinal analysis of mentorship network dynamics, SAOMs model how individuals make decisions about forming, maintaining, or dissolving relationships over time[11]. The model estimates:

1. **Rate Function**: Determines the frequency of opportunity for change for actor i
2. **Objective Function**: Determines the probability of specific changes, modeled as:
   p(i→j) = exp(fi(β,x))/(∑k exp(fi(β,x))), where fi is the objective function for actor i, β is a vector of parameters, and x represents the current network state.

These models account for both individual attributes and network structural effects, helping disentangle selection and influence processes in mentorship dynamics[11].

### Statistical Analysis
Additional statistical techniques complement these specialized methods:
- **Multinomial Logistic Regression**: To estimate the likelihood of individuals with certain characteristics following particular career patterns[16].
- **Survival Analysis**: To examine how mentorship affects time-to-event outcomes such as promotion or attrition.
- **Multi-level Modeling**: To account for individuals nested within departments, organizations, or industries.

## Example Applications

"The Career Paths Less (or More) Traveled: A Sequence Analysis of IT Career Histories, Mobility Patterns, and Career Success" applies sequence analysis to examine the career trajectories of 500 individuals who had worked in the IT workforce, drawn from the National Longitudinal Survey of Youth. The researchers analyzed career histories to challenge the traditional view of a dual IT career path (technical versus managerial), instead revealing a more complex typology comprising three distinct career paths: IT careers, professional labor market (PLM) careers, and secondary labor market (SLM) careers. Notably, only 173 individuals remained in IT careers, while 327 transitioned to other professional or lower-status jobs. Using sequence analysis to trace these diverse mobility patterns, the study enriched understanding of "boundaryless" careers that span not only organizational but also occupational boundaries. The findings revealed that career success, measured by average pay, did not differ significantly between IT and PLM careers, though individuals in SLM careers achieved the lowest compensation. This application demonstrates how sequence analysis can reveal unexpected career patterns and challenge conventional assumptions about career progression in technical fields[14].

"Mapping career patterns in research: A sequence analysis of career histories of researchers" employs Optimal Matching Analysis to identify and analyze career patterns of researchers across positions and institutions. Based on complete career histories of applicants to the European Research Council frontier research grant schemes, the researchers distinguished five distinct career patterns for both early-career and established researchers. The study used multinomial logit analyses to estimate the relative likelihood of researchers with certain characteristics following each pattern. Their findings revealed successful grant recipients across all career patterns and demonstrated limited evidence of gender differences in research career trajectories—challenging common assumptions about gender disparities in research careers. The authors positioned their methodological approach as a paradigm shift "from causes to events," focusing on describing careers "as they are" rather than imposing predetermined models. This application shows how sequence analysis can identify order in seemingly diverse career paths and inform policy making on career development, research funding, and gender equality initiatives[16].

"Using Social Network Analysis to Assess Mentorship and Collaboration in a Public Health Network" examines the structure of mentorship and collaboration relationships among members of the Healthy Aging Research Network using social network analysis. The researchers invited 97 network members and partners to complete an online social network survey about mentorship and collaboration activities during the previous 12 months. The analysis revealed that 74% of network members were connected through mentorship ties, and all 97 members were connected through at least one form of collaboration. The study computed network-level measures such as density, number of components, and centralization to assess network cohesiveness, finding that mentorship and collaboration ties existed both within and across organizational boundaries. The research demonstrated how SNA can quantitatively assess the structure and extent of mentoring relationships in professional networks, providing insights into how these relationships facilitate knowledge transfer and collaboration. This application illustrates how network analysis can be used to evaluate mentorship programs and inform strategies for strengthening developmental relationships within professional communities[5].

## Critiques

Despite its valuable contributions to understanding career development, the mentorship and sponsorship studies approach has several notable limitations:

### Modest Effect Sizes
Meta-analyses of mentoring outcomes consistently show that while mentoring is associated with positive outcomes, the effect sizes are generally small[6]. This raises questions about the practical significance of mentoring interventions and suggests that mentoring may be necessary but insufficient for substantial career advancement, requiring complementary development approaches.

### Disciplinary Fragmentation
Mentoring research has traditionally been conducted within disciplinary silos, with each field focusing on specific types of mentoring relationships[6]. This fragmentation has hindered the development of comprehensive theoretical frameworks that integrate insights across contexts. While recent multi-disciplinary efforts have begun addressing this limitation, the field still lacks cohesive theories that can explain mentoring effects across different career stages and settings.

### Methodological Constraints
Traditional mentoring research has often relied on cross-sectional designs, self-reported measures, and simplified dyadic models that fail to capture the complexity of developmental relationships[12][5]. The developmental network perspective has emerged to address some of these limitations, but methodological challenges persist in capturing the dynamic, multifaceted nature of these networks over time. Additionally, establishing causality remains difficult, as selection effects may confound the relationship between mentoring and career outcomes.

### Equity and Access Concerns
Research suggests that not all professionals have equal access to quality mentoring and sponsorship, with disparities often falling along lines of gender, race, and socioeconomic status[17][20]. This inequality may perpetuate existing disparities in career advancement rather than mitigating them. Additionally, the effectiveness of mentoring relationships varies significantly based on contextual factors, raising questions about the generalizability of findings across different organizational settings.

### Conceptual Ambiguity
Despite efforts to distinguish between mentorship, sponsorship, and coaching, conceptual ambiguity persists in how these terms are defined and operationalized across studies[17][20]. This ambiguity complicates cross-study comparisons and synthesis of findings. Furthermore, the field lacks consensus on how to measure the quality of these relationships beyond their mere presence or absence.

## Software

### RSiena (R Package)
RSiena is a comprehensive R package designed for the simulation-based estimation of stochastic actor-oriented models (SAOMs) for longitudinal network data collected as panel data. Developed by Tom A.B. Snijders and colleagues, this package enables researchers to analyze how networks evolve over time, including mentorship networks where relationships form, persist, or dissolve. RSiena can handle single or multivariate networks that may be directed, non-directed, or two-mode, along with associated actor variables. The package includes functions for testing parameters and checking goodness of fit, making it valuable for studying how individual characteristics and structural positions influence the development of mentoring relationships. With its foundation in the Boost Graph Library and extensive use of C++ template metaprogramming, RSiena offers high-performance analysis capabilities that are particularly valuable for large-scale network studies of mentoring relationships in organizations[7].

### statnet (R Package)
The statnet suite of R packages provides a comprehensive toolkit for statistical analysis of network data, offering essential functionality for mentorship and sponsorship researchers. This package suite includes tools for network data description, visualization, model estimation, model evaluation, and simulation. At its core is a Markov chain Monte Carlo (MCMC) algorithm optimized for speed and robustness. The statnet framework can represent various relational data types and supports arbitrary vertex, edge, and graph attributes, making it ideal for capturing the multifaceted nature of mentoring relationships. The package is continuously developed and maintained by the statnet development team, with new capabilities being added over time. For mentorship researchers, statnet offers the ability to model how individual attributes (e.g., career stage, gender) influence the formation of mentoring ties, test hypotheses about network structures, and simulate mentoring network evolution under different conditions[8].

### TraMineR (R Package)
TraMineR is a specialized R package for analyzing sequence data that is particularly valuable for studying career trajectories in mentorship and sponsorship research. This package enables researchers to manipulate, describe, visualize, and analyze sequences of states or events, such as career positions, transitions, and developmental relationships. While primarily designed for analyzing longitudinal data in the social sciences (careers, family trajectories, time-use), TraMineR's functionality extends to categorical sequence data more broadly. The package offers tools for handling longitudinal data, converting between sequence formats, creating visual representations (density plots, frequency plots, index plots), and calculating individual sequence characteristics (length, time in each state, entropy, turbulence). For mentorship researchers, TraMineR provides essential capabilities for identifying typical career patterns following different mentorship interventions, measuring dissimilarities between career sequences, and performing ANOVA-like analyses to determine how mentorship factors influence career trajectories[13].

### NetworkX (Python Package)
NetworkX is a Python package for creating, manipulating, and studying complex networks, making it a versatile tool for mentorship and sponsorship research. The package provides data structures for graphs, digraphs, and multigraphs along with numerous standard graph algorithms and network structure analysis measures. NetworkX offers robust functionality for generating classic graphs, random graphs, and synthetic networks, which can be useful for modeling mentorship networks and testing hypotheses about their structural properties. A key advantage of NetworkX is its flexibility—nodes can represent various entities (people, positions, organizations) and edges can hold arbitrary data such as relationship types, strength, or duration. Released under an open-source BSD license and thoroughly tested with over 90% code coverage, NetworkX provides researchers with a reliable platform for analyzing how mentorship networks form, evolve, and influence career outcomes. The package's integration with Python's broader ecosystem offers additional benefits for data preprocessing, visualization, and statistical analysis[9].

### graph-tool (Python Module)
Graph-tool is a high-performance Python module for network analysis that offers exceptional efficiency for studying large-scale mentorship networks. Unlike most Python network analysis tools, graph-tool's core data structures and algorithms are implemented in C++, making extensive use of template metaprogramming based on the Boost Graph Library. This design gives graph-tool performance comparable to pure C/C++ libraries in both computation time and memory usage. The software has matured over more than 15 years of development at the forefront of network science and is released under the LGPLv3 license with comprehensive documentation. For mentorship researchers working with large organizational datasets, graph-tool offers unique capabilities including a comprehensive framework for inferential community detection that can identify mentorship clusters within organizations. The module's exceptional speed makes it particularly suitable for analyzing mentorship patterns in extensive longitudinal datasets where Python-only alternatives might become computationally prohibitive[10].

## Example Study Design: Mentorship and Sponsorship Networks in U.S. Army Officer Career Trajectories

### Key Variables

This study would examine how mentorship and sponsorship relationships influence career advancement across four U.S. Army Branch Divisions (Armor, Logistics, Aviation, and Cyber), focusing on several categories of variables:

1. **Mentorship/Sponsorship Network Characteristics**
   - Network size (number of mentors/sponsors)
   - Network diversity (mentors/sponsors from different branches, ranks, backgrounds)
   - Relationship type (formal vs. informal, internal vs. external to unit)
   - Relationship content (career guidance, psychosocial support, advocacy)
   - Relationship duration and frequency

2. **Career Trajectory Indicators**
   - Promotion speed and timing relative to peers
   - Selection for key developmental positions
   - Performance evaluation scores
   - Special assignments and deployments
   - Advanced education opportunities
   - Branch-specific milestones (e.g., command positions, specialized training)

3. **Individual Characteristics**
   - Demographic information (gender, race/ethnicity)
   - Entry pathway (academy, ROTC, OCS)
   - Prior enlisted experience
   - Non-cognitive attributes (leadership style, resilience, adaptability)
   - Technical and tactical proficiency

4. **Organizational Context**
   - Branch culture and norms
   - Unit mentoring programs
   - Command climate
   - Operational tempo and deployment cycles

### Sample & Data Collection

The study would employ a mixed-methods approach to collect comprehensive data on mentorship networks and career trajectories:

1. **Longitudinal Survey**: A cohort of 800 officers (200 from each branch) would be surveyed at three time points over five years. The survey would capture developmental network composition using name generators ("Who has provided you with career guidance?"), relationship characteristics, and perceived career impact of these relationships. This approach aligns with established developmental network research methodologies[12][5].

2. **Administrative Data**: With appropriate permissions, official personnel records would be accessed to track objective career outcomes including promotion timing, assignment history, performance evaluations, and special selections. These records provide unbiased measures of career progression that complement self-reported data[14].

3. **Semi-structured Interviews**: A subset of 80 officers (20 from each branch) representing diverse career trajectories would participate in in-depth interviews exploring the quality and impact of their mentorship/sponsorship relationships. These interviews would provide rich contextual understanding of how developmental relationships function within military culture[17].

4. **Social Network Census**: In selected units, complete network data would be collected to map formal and informal mentoring relationships, allowing for analysis of mentorship network structures within organizational contexts[5].

### Analysis Approach

The analysis would employ multiple complementary methods to understand how mentorship and sponsorship shape officer career trajectories:

1. **Social Network Analysis**: Using statnet[8] and RSiena[7], we would analyze the structure of mentorship networks, including density, centralization, and clustering patterns. Longitudinal analysis would examine how these networks evolve over time and identify structural factors that facilitate or hinder effective mentoring relationships. Stochastic actor-oriented models would help distinguish selection effects (who forms mentoring relationships with whom) from influence effects (how mentoring relationships shape career decisions).

2. **Sequence Analysis**: Using TraMineR[13], we would analyze career trajectories as sequences of positions and assignments, identifying typical career patterns within each branch. Optimal matching analysis would calculate the similarity between career sequences and cluster them into distinct trajectory types. This approach would reveal how different mentorship configurations correlate with specific career pathways.

3. **Statistical Modeling**: Regression analyses would examine how mentorship network characteristics predict career outcomes, controlling for individual attributes and organizational factors. Multilevel models would account for the nested structure of the data (officers within units within branches). Survival analysis would examine how mentorship affects time-to-promotion and retention.

4. **Qualitative Analysis**: Interview data would be coded and analyzed to identify themes in how officers experience and leverage mentorship relationships. This analysis would provide interpretive context for the quantitative findings and identify branch-specific mentorship dynamics not captured in the survey data.

### Potential Findings

The analysis is likely to reveal several key patterns in how mentorship and sponsorship influence Army officer career trajectories:

1. **Branch-Specific Mentorship Patterns**: Each branch may exhibit distinct mentorship structures and dynamics, with technical branches like Cyber potentially showing more specialized, expertise-focused mentoring compared to leadership-oriented mentoring in combat arms branches like Armor. Aviation may demonstrate mentorship patterns that balance technical expertise with leadership development.

2. **Developmental Network Diversity Effects**: Officers with more diverse developmental networks (spanning different branches, ranks, and functional areas) may show greater career mobility and adaptability, particularly during transitions between operational and staff assignments. This diversity effect may be especially pronounced in Logistics, where cross-functional coordination is essential.

3. **Sponsorship and Key Assignments**: The presence of senior sponsors may strongly predict selection for career-enhancing opportunities like command positions and specialized schools, with sponsorship potentially having a stronger effect than mentorship on these high-visibility outcomes. This effect may be particularly evident in competitive selection processes for prestigious commands.

4. **Gender and Racial Differences**: Female and minority officers may show different mentorship network structures and potentially require stronger sponsorship to achieve similar career outcomes as their majority counterparts. These differences may vary by branch, with potentially smaller gaps in newer branches like Cyber.

5. **Formal vs. Informal Mentoring**: The relative effectiveness of formal mentoring programs versus informal mentoring relationships may vary by branch culture and career stage, with formal programs potentially showing stronger effects early in officers' careers and informal relationships becoming more influential at higher ranks.

### Potential Implications

The findings from this study would have significant implications for Army leadership development and talent management:

1. **Tailored Mentorship Programs**: Evidence of branch-specific mentorship patterns would suggest the need for tailored mentorship programs that address the unique developmental needs of officers in different branches rather than one-size-fits-all approaches.

2. **Developmental Network Training**: Training programs could be developed to help officers intentionally build and maintain diverse developmental networks throughout their careers, emphasizing the importance of both mentorship (guidance) and sponsorship (advocacy) relationships.

3. **Equity Interventions**: If findings reveal disparities in mentorship access or effectiveness across demographic groups, targeted interventions could be implemented to ensure equitable career development opportunities for all officers, particularly in branches with historical underrepresentation.

4. **Cross-Branch Development**: Evidence that diverse networks enhance career success could inform talent management policies that encourage cross-branch experiences and relationships, potentially through formal rotation programs or joint assignments.

5. **Leadership Accountability**: Findings on the impact of sponsorship could inform efforts to make senior leaders more accountable for developing junior talent, potentially by incorporating sponsorship behaviors into leadership evaluation criteria.

6. **Knowledge Management**: Understanding how mentorship facilitates knowledge transfer across generations of officers could inform knowledge management strategies, particularly in technical branches like Cyber where rapid technological change requires continuous learning.

## Sources
[1] How to Sponsor, Coach, and Mentor: A Qualitative Study With ... https://journals.stfm.org/familymedicine/2023/march/alachkar-2021-0622/\
[2] Mentoring Programs: Purpose, Benefits + How to Get Your ... https://www.togetherplatform.com/blog/what-is-the-purpose-of-mentoring\
[3] What's a Sponsor and How Do You Get One at Work? https://www.thehbcucareercenter.com/blog/whats-a-sponsor-and-how-do-you-get-one-at-work\
[4] Mentorship vs. Sponsorship: How to Choose the Right Approach for ... https://nextbridgeconsulting.com/mentorship-vs-sponsorship-how-to-choose-the-right-approach-for-your-team/\
[5] Using Social Network Analysis to Assess Mentorship and ... - CDC https://www.cdc.gov/pcd/issues/2015/15_0103.htm\
[6] Does Mentoring Matter? A Multidisciplinary Meta-Analysis ... https://pmc.ncbi.nlm.nih.gov/articles/PMC2352144/\
[7] CRAN: Package RSiena - R Project https://cran.r-project.org/package=RSiena\
[8] [PDF] statnet: Software Tools for the Statistical Analysis of Network Data https://cran.r-project.org/web/packages/statnet/statnet.pdf\
[9] NetworkX — NetworkX documentation https://networkx.org\
[10] graph-tool: Efficient network analysis with Python https://graph-tool.skewed.de\
[11] [PDF] An Introduction to Stochastic Actor Oriented Models - statistics https://www.stats.ox.ac.uk/~snijders/siena/IntroSAOM_h.pdf\
[12] Celebrating Mentoring! - Massachusetts General Hospital https://www.massgeneral.org/assets/mgh/pdf/faculty-development/mentoring/20230125MentoringPresentation-Higgins.pdf\
[13] TraMineR: Sequence Analysis https://traminer.unige.ch\
[14] The Career Paths Less (or More) Traveled: A Sequence Analysis of ... https://misq.umn.edu/the-career-paths-less-or-more-traveled-a-sequence-analysis-of-it-career-histories-mobility-patterns-and-career-success.html\
[15] Mentors and Sponsors Make the Difference - Gallup.com https://www.gallup.com/workplace/473999/mentors-sponsors-difference.aspx\
[16] Mapping career patterns in research: A sequence analysis of career ... https://pmc.ncbi.nlm.nih.gov/articles/PMC7390397/\
[17] How to Sponsor, Coach, and Mentor: A Qualitative Study With ... https://pmc.ncbi.nlm.nih.gov/articles/PMC10622011/\
[18] Why Mentorship and Sponsorship are Critical to Women's Success https://www.pce.uw.edu/news-features/articles/mentorship-sponsorship-critical-womens-success\
[19] Mentor & Sponsor: Understanding the Key Differences - Mentorink https://www.mentorink.com/blog/mentor-sponsor-understanding-the-key-differences/\
[20] Mentorship, Sponsorship, and Coaching for Trainee Career ... https://pubs.rsna.org/doi/full/10.1148/rg.2021210085\
