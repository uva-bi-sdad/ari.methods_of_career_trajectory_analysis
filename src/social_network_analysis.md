---
title: Social Network Analysis as a Method for Analyzing Career Trajectories
format: latex
---

Social Network Analysis (SNA) provides powerful analytical tools for understanding the complex patterns that shape career paths. By mapping the interconnections between individuals, positions, and organizations, researchers can gain valuable insights into career mobility, identify influential factors in professional development, and understand the structural aspects of career trajectories. This report examines SNA methodology specifically in the context of analyzing career paths, including its theoretical foundations, practical applications, limitations, and implementation strategies.

## 1. Approach Description & Goal

Social Network Analysis is a methodological approach that investigates social structures through the application of network and graph theory principles. SNA characterizes systems as networks composed of nodes (individual actors, positions, or organizations) and the ties or edges (relationships or interactions) that connect them[9]. When applied to career trajectory analysis, SNA transforms individual work histories into structured networks that reveal patterns of job transitions, professional relationships, and career mobility pathways that might otherwise remain hidden in conventional analyses.

The primary goals of SNA in career research include: identifying common career pathways within professions; understanding how relationships facilitate career advancement; recognizing "gateway" positions that enable access to higher-level roles; quantifying career mobility potential across different entry points; and developing evidence-based career guidance by mapping the universe of likely career paths available from specific starting positions[13]. By visualizing and analyzing career networks, researchers can identify structural barriers to advancement, discover high-potential career paths, and uncover the relationships between skills acquisition and career mobility across different demographic groups.

## 2. Critical Variables

Social Network Analysis of career trajectories typically incorporates several categories of variables:

### Network Structure Variables
- **Nodes/Vertices**: Representing individuals, job positions, occupations, or organizations[9]
- **Edges/Ties**: Representing job transitions, mentoring relationships, collaborations, or other professional connections between nodes[9]
- **Network Density**: The proportion of potential connections that are actually present in the network
- **Clustering Coefficient**: Measures how nodes tend to cluster together in the network

### Node Attribute Variables
- **Demographic Data**: Age, gender, race/ethnicity, and educational background
- **Professional Characteristics**: Skills, credentials, tenure, and performance metrics
- **Position Attributes**: Salary level, hierarchical rank, department, functional area
- **Industry-Specific Variables**: In military contexts, these might include rank, branch, deployment history

### Edge Attribute Variables
- **Tie Strength**: Frequency or duration of relationships
- **Directionality**: Whether transitions or relationships are one-way or reciprocal
- **Temporal Data**: When transitions or relationships occurred
- **Transition Type**: Lateral moves, promotions, demotions, or cross-industry shifts[2]

### Centrality Measures
- **Degree Centrality**: Number of direct connections a node has
- **Betweenness Centrality**: How often a node lies on shortest paths between other nodes
- **Closeness Centrality**: Average distance from a node to all other nodes
- **Eigenvector Centrality**: Measure of influence based on connections to other influential nodes[4]

### Mobility Indicators
- **Career Velocity**: Rate of upward movement through positions
- **Path Diversity**: Number of distinct career pathways identified
- **Structural Holes**: Gaps between different career clusters that may represent barriers or opportunities[1]
- **Social Networking Potential (SNP)**: A numeric coefficient representing both network size and influence capacity[9]

## 3. Key Overviews

**Wasserman and Faust (1994) "Social Network Analysis: Methods and Applications"** represents a foundational text in the field of social network analysis. The authors provide comprehensive coverage of SNA methodology, starting with basic concepts and progressing to advanced analytical techniques. The book systematically addresses network data collection, representation through matrices and graphs, measurement of centrality and prestige, identification of cohesive subgroups, structural equivalence, blockmodels, and statistical analysis of social networks. Particularly valuable are the chapters on dyadic and triadic analysis, which help researchers understand the building blocks of larger network structures. The authors also include numerous practical examples and applications across various disciplines, making this text essential reading for understanding the theoretical foundations and methodological approach of SNA[11][14].

**"Social Network Analysis 101: Ultimate Guide" (2023) by Visible Network Labs** provides an accessible introduction to SNA concepts and applications. The guide covers the theoretical background of SNA, including the "Strength of Weak Ties Theory," which posits that weaker connections often provide more novel information and resources compared to strong ties. It also explores the "Structural Hole Theory," which explains how individuals bridging gaps between different groups in a network gain strategic advantages in controlling information and resource flows. This resource serves as an excellent entry point for those new to network analysis, offering practical explanations of complex network concepts and their applications in understanding social and professional relationships[1].

**"Social Network Analysis: Understanding Centrality Measures" (2020) by Cambridge Intelligence** offers a focused examination of network centrality concepts, which are critical metrics for identifying influential positions in career networks. The article explains different centrality measures—degree, betweenness, closeness, eigenvector centrality, and PageRank—and their interpretations in social contexts. Understanding these measures is particularly important for career trajectory analysis, as they help identify pivotal roles that serve as gateways to career advancement or positions that offer greater access to information and resources. The article presents these complex mathematical concepts in an accessible manner, making it valuable for researchers seeking to apply appropriate centrality measures in their career network analyses[4].

**"Social Network Analysis: A Methodological Introduction" (2008) by Carter T. Butts** provides a comprehensive overview of SNA methodology with particular attention to the mathematical foundations and practical applications. The article covers network representation, centrality concepts, local network structures, and dyadic and triadic analysis. Butts explains the theoretical underpinnings of SNA while connecting them to practical research applications across multiple disciplines. The paper serves as a bridge between theoretical concepts and applied research, offering guidance on methodological decisions in network analysis. The author's discussion of statistical approaches to network data is particularly valuable for researchers looking to move beyond descriptive analysis to inferential testing in career trajectory studies[14].

## 4. Mathematical Approach

Social Network Analysis employs graph theory as its mathematical foundation, representing relationships as mathematical structures composed of nodes (vertices) and edges. In career trajectory analysis, this approach allows researchers to quantify and analyze patterns of movement between positions[9].

### Basic Network Representation

A network is formally represented as a graph G = (V, E), where:
- V is a set of vertices or nodes (representing individuals, positions, or organizations)
- E is a set of edges or ties (representing relationships or transitions between nodes)

Networks can be undirected (edges have no direction) or directed (edges have direction, as in career progressions). In matrix form, networks are typically represented as adjacency matrices where:

$$ A_{ij} = \begin{cases} 
1 & \text{if there is an edge from node } i \text{ to node } j \\
0 & \text{otherwise}
\end{cases} $$

For weighted networks (where ties have varying strengths, such as frequency of transitions):

$$ W_{ij} = \text{weight of tie from node } i \text{ to node } j $$

### Centrality Measures

Several mathematical formulas quantify the importance of nodes in a network[4]:

**Degree Centrality**: For a node i in an undirected graph, degree centrality is:
$$ C_D(i) = \sum_{j \in V} A_{ij} $$

In directed graphs, we distinguish between in-degree and out-degree:
$$ C_{D}^{in}(i) = \sum_{j \in V} A_{ji} $$
$$ C_{D}^{out}(i) = \sum_{j \in V} A_{ij} $$

**Betweenness Centrality**: The proportion of shortest paths between all node pairs that pass through node i:
$$ C_B(i) = \sum_{s \neq i \neq t} \frac{\sigma_{st}(i)}{\sigma_{st}} $$
where σ_st is the total number of shortest paths from node s to node t, and σ_st(i) is the number of those paths that pass through node i.

**Closeness Centrality**: The reciprocal of the sum of the shortest distances to all other nodes:
$$ C_C(i) = \frac{n-1}{\sum_{j \in V} d(i,j)} $$
where d(i,j) is the shortest path distance between nodes i and j.

**Eigenvector Centrality**: A measure where a node's importance depends on the importance of its neighbors:
$$ C_E(i) = \frac{1}{\lambda} \sum_{j \in V} A_{ij} C_E(j) $$
where λ is the largest eigenvalue of the adjacency matrix A.

### Path Analysis and Connectivity

In career trajectory analysis, paths represent possible career progressions. A path from node v₁ to vₙ is a sequence of edges connecting a sequence of distinct vertices. The path length is the number of edges traversed.

Key metrics include:
- **Average Path Length**: The mean of shortest path lengths between all node pairs
- **Diameter**: The maximum shortest path length in the network
- **Reachability**: Whether a path exists between two nodes

### Community Detection

Career trajectory analysis often involves identifying clusters or communities of positions that are closely connected. Modularity (Q) is a common measure:

$$ Q = \frac{1}{2m} \sum_{ij} \left[ A_{ij} - \frac{k_i k_j}{2m} \right] \delta(c_i, c_j) $$

where m is the number of edges, k_i is the degree of node i, c_i is the community of node i, and δ is the Kronecker delta function.

### Temporal Network Analysis

For analyzing career progressions over time, researchers use temporal network measures including:
- Sequence analysis to identify typical career patterns
- Transition probability matrices to quantify the likelihood of moving between positions
- Career velocity metrics to measure the rate of progression through hierarchical levels[13]

## 5. Example Applications

**"Using Network Analysis of Job Transitions to Inform Career Advice" (2022) by Axelle Clochard** applies SNA to study career mobility patterns using U.S. job transitions data. Clochard constructs a network where nodes represent occupations and edges represent significant flows of workers between jobs. The research focuses on identifying career paths from entry-level or precarious occupations that lead to stable, high-wage employment. The study reveals that although opportunities exist for workers with various educational backgrounds, upward mobility prospects are generally limited for workers without a bachelor's degree. Low-wage or shrinking occupations typically offer restricted access to stable, high-wage employment. However, the analysis also identifies "bright spot" occupations that provide reliable pathways to sustainable employment even for workers starting in lower-wage positions. The research demonstrates how network analysis can inform evidence-based career guidance by mapping the likely universe of career paths available from specific starting points[13].

**"The Road Less Traveled: Analyzing the Career Paths of Women Athletic Directors Utilizing Social Network Analysis" (2025) by Motley, Jensen, Weight, and Bates** employs SNA to analyze career paths of NCAA Division I women athletic directors (ADs) and build a hiring network within intercollegiate athletics. The researchers tracked career changes of current Division I women ADs to identify influential institutions and compare career trajectories between women and men ADs. Their findings reveal that women ADs typically navigate longer career paths within a much sparser network compared to their male counterparts. Women who successfully attained AD positions generally advanced through various positions in college athletics, with certain "hub" institutions serving as accelerators for their careers. The study also found that institutional authorities often hired women at higher positions, frequently at senior executive levels, before they became ADs. This application demonstrates how SNA can illuminate gender differences in career progression and identify influential organizations that serve as critical stepping stones for advancement in specific professional fields[18].

**"Using social network analysis to track career trajectories of women STEM faculty" (2019) by Erin McCullagh et al.** applies SNA to investigate co-authorship networks among STEM faculty, with particular focus on understanding the career paths of women in academia. The researchers mapped faculty publication networks to visualize collaboration patterns and identify influential positions and connections. For individuals, these network maps function as a "GPS system for career navigation," showing faculty members their network positions relative to others and helping them strategize future career moves. The study reveals how network mapping can help faculty identify potential collaborators, understand how to strengthen their academic position, and recognize the impact of their collaboration choices on career trajectories. The research demonstrates the value of SNA in identifying both structural barriers and opportunities for career advancement in academic settings, particularly for underrepresented groups like women in STEM fields[6].

**"Hidden patterns: Using social network analysis to track career trajectories of women STEM faculty" (2019)** applies SNA to investigate the career progression of women faculty in Science, Technology, Engineering, and Mathematics (STEM) disciplines. The researchers used co-authorship networks as proxies for professional relationships and collaboration opportunities, analyzing how these networks influenced career advancement for women academics. The study found that women faculty in STEM fields often have different network structures compared to their male counterparts, with potential implications for promotion, tenure, and research opportunities. By examining publication patterns and collaboration networks, the researchers were able to identify specific structural challenges facing women in academic STEM careers. The study demonstrates how SNA can reveal hidden patterns of gender inequality embedded in professional relationships and suggests interventions to create more equitable academic environments[10].

## 6. Critiques

Despite its analytical power, Social Network Analysis has several limitations when applied to career trajectory research:

**Methodological Limitations**: SNA often sacrifices the rich longitudinal structure of individual career histories to identify broader patterns. While this trade-off enables the discovery of structural trends, it may obscure important details of personal career development. As noted in Clochard's research, "the twin forces of personal preference and structural constraints would have made it difficult to extrapolate any kind of general trend from individual career trajectories," yet these individual variations matter significantly in real career outcomes[13].

**Boundary Specification Problems**: Defining network boundaries appropriately presents significant challenges in career trajectory analysis. Researchers must make critical decisions about which actors to include or exclude and how to demarcate system boundaries. These decisions can significantly impact findings, potentially excluding important influences from outside the defined network. As Wasserman and Faust note, boundary specification and sampling decisions are fundamental methodological challenges in network analysis[11].

**Data Quality and Availability Concerns**: SNA requires comprehensive data about relationships, which may be difficult to obtain accurately. Career transition data often comes from resumes, professional networks, or surveys, all of which have inherent biases and reliability issues. Records may be incomplete, subject to recall bias, or systematically missing certain types of transitions. Moreover, as noted by Clochard, different data sources (like resumes versus government surveys) may capture different populations and transition patterns[13].

**Causality Attribution Problems**: While SNA effectively reveals patterns and correlations in career paths, it often struggles to establish causality. The identification of common pathways does not necessarily explain why these paths exist or what individual factors lead to successful transitions. This limitation makes it challenging to develop prescriptive career advice based solely on network patterns without complementary qualitative or experimental research[10][13].

**Static Representation of Dynamic Processes**: Traditional SNA methods often provide static snapshots of networks, which may inadequately capture the dynamic nature of career development over time. Although temporal network analysis techniques exist, they remain less developed than static approaches. This limitation is particularly problematic for understanding how career networks evolve and how timing affects career transitions[9].

**Homophily and Selection Effects**: Networks often display homophily (the tendency to associate with similar others), which can make it difficult to distinguish between selection effects and genuine influence in career patterns. In career trajectory analysis, this manifests as uncertainty about whether certain career paths result from institutional structures, skill requirements, or social sorting processes based on demographic characteristics[19].

## 7. Software

**UCINET** is one of the most comprehensive and widely used software packages for social network analysis, developed by Analytic Technologies. It provides tools for matrix algebra, multivariate statistics, and graph theory specifically designed for analyzing social network data. UCINET includes functionality for calculating various centrality measures, identifying subgroups, performing role and positional analysis, and statistical testing of network hypotheses. The software can handle networks with thousands of nodes and includes routines for QAP regression, blockmodeling, and multidimensional scaling. For career trajectory analysis, UCINET offers valuable tools for identifying structural patterns in job transition networks and quantifying the positional importance of specific roles. The software is available as a 60-day free trial and includes the NetDraw visualization tool, making it particularly suitable for researchers new to SNA who need a comprehensive analysis platform[14].

**NetworkX** is a Python package that provides robust tools for creating, manipulating, and studying the structure, dynamics, and functions of complex networks. It supports various network types (directed, undirected, multi-graphs) and includes implementations of many standard graph algorithms. NetworkX's strengths include its integration with the broader Python data science ecosystem (including pandas, NumPy, and matplotlib), allowing for seamless workflow with other data analysis tools. For career trajectory research, NetworkX excels at handling large-scale networks and implementing custom metrics relevant to career path analysis. The package supports temporal networks, making it suitable for analyzing career transitions over time. Its open-source nature, extensive documentation, and active development community make it an excellent choice for researchers with programming experience who need flexibility in their analysis approach.

**igraph** is available as both an R package and a Python library, providing powerful tools for network analysis with an emphasis on efficiency, portability, and ease of use. The package is particularly strong for large-scale network analysis thanks to its C core implementation, which enables fast computation of complex network metrics. The igraph package includes comprehensive functionality for community detection, which is valuable for identifying clusters of related positions or common career paths. For career trajectory analysis, igraph offers excellent performance when dealing with large job transition networks and sophisticated algorithms for path analysis. The package's visualization capabilities are more limited than specialized visualization tools, but it integrates well with plotting libraries in both R and Python, making it a versatile choice for researchers comfortable with programming.

**statnet** is a suite of R packages for network analysis, modeling, and visualization, with particular strengths in statistical modeling of networks. The suite includes packages such as 'network' for data manipulation, 'sna' for descriptive analysis, and 'ergm' for exponential random graph modeling. For career trajectory research, statnet is especially valuable when researchers need to move beyond descriptive analysis to statistical inference and hypothesis testing. The ergm package allows for modeling the probability of career transitions based on individual attributes, structural factors, and their interactions. This capability is particularly useful for understanding what factors predict specific career paths or for testing theories about career mobility barriers. Statnet is open-source, actively maintained, and well-documented, making it an excellent choice for researchers with statistical expertise who need rigorous inferential capabilities.

**Gephi** is an open-source network visualization and exploration platform designed to help researchers intuitively discover patterns and trends in network data. Unlike the programming-based packages, Gephi provides an interactive graphical user interface that allows users to manipulate, analyze, and visualize networks without coding. It features real-time visualization, supports large networks, and offers sophisticated filtering capabilities to focus on specific network segments. For career trajectory analysis, Gephi excels at creating compelling visual representations of career paths and transition patterns that can communicate findings to non-technical audiences. Its dynamic filtering capabilities allow researchers to explore how career networks evolve over time or differ across demographic groups. Gephi also includes standard network metrics and community detection algorithms, making it a good option for researchers who prioritize visualization and interactive exploration over advanced statistical modeling.

**Pajek** is specialized software designed specifically for analysis and visualization of large networks. Its name means "spider" in Slovenian, reflecting its focus on web-like network structures. Pajek is particularly effective for handling very large networks (with millions of nodes) that might be computationally challenging for other software. The program includes implementations of various decomposition, clustering, and blockmodeling algorithms that are valuable for identifying structural patterns in career networks. For career trajectory analysis, Pajek's partitioning capabilities allow researchers to identify hierarchical structures and career clusters efficiently. The software is free for non-commercial use and has a dedicated user community, particularly in academia. While its interface may appear less modern than some alternatives, Pajek remains a powerful tool for researchers dealing with extremely large career networks or those requiring specialized network decomposition techniques[14].

## 8. Example Study Design: Social Network Analysis of U.S. Army Officer Career Trajectories

### Key Variables

**Node Variables (Officers and Positions)**:
- **Individual Attributes**: Officer IDs, demographics, commissioning source, entry branch
- **Position Attributes**: Rank (O-1 through O-6+), functional branch (Armor, Logistics, Aviation, Cyber), position type (command, staff, broadening, joint)
- **Performance Indicators**: Officer Evaluation Report (OER) ratings, awards received, selection for competitive positions
- **Educational Achievements**: Military education level (Basic Officer Leader Course, Captain's Career Course, Command and General Staff College, War College), civilian education degrees
- **Branch-Specific Indicators**:
  - **Armor**: Combat training center rotation performance, gunnery qualification scores
  - **Logistics**: Maintenance readiness rates, supply discipline metrics
  - **Aviation**: Flight hours, aircraft qualifications, accident-free operations
  - **Cyber**: Technical certifications, technical assessment scores
- **Non-Cognitive Attributes**: Leadership style assessments, cognitive flexibility scores, psychological resilience metrics

**Edge Variables (Career Transitions)**:
- **Transition Type**: Promotion, lateral move, special assignment, branch transfer
- **Timing Variables**: Time in grade, time between transitions, career phase
- **Relationship Variables**: Mentorship connections, superior-subordinate relationships
- **Selection Process**: Competitive vs. non-competitive assignments

### Sample & Data Collection

The study will analyze career trajectory data from a cohort of U.S. Army officers (N=5,000) who were commissioned between 2000-2010, allowing for the tracking of at least 15 years of career progression. The sample will include officers from all four branch divisions (Armor, Logistics, Aviation, and Cyber) with proportional representation based on the actual distribution in the Army. 

Data collection will involve aggregating information from multiple Army personnel databases:
1. **Official Military Personnel Files (OMPF)**: For comprehensive career history including assignments, promotions, and evaluations
2. **Army Training Information System**: For education and qualification records
3. **Army Talent Management System**: For skills inventories and competency assessments
4. **Branch-specific performance databases**: For technical proficiency metrics
5. **Army Mentorship Program records**: To capture formal mentoring relationships

Additionally, a supplementary survey will be administered to a stratified subsample (n=1,000) to collect data on informal mentoring relationships, career satisfaction, and non-cognitive attributes not captured in official records. To ensure data quality, the research team will conduct verification through triangulation of multiple data sources and follow strict data anonymization protocols to protect officer privacy while maintaining analytical integrity.

### Analysis Approach

The analysis will employ a multi-phase SNA approach to comprehensively examine career trajectories:

1. **Network Construction**:
   - Build a primary position transition network where nodes represent specific military positions and directed edges represent officer movements between positions
   - Create a parallel officer network where nodes represent individual officers and edges represent professional relationships (mentorship, command relationships)
   - Develop temporal networks to capture how career paths evolve over different commissioning cohorts

2. **Structural Analysis**:
   - Calculate centrality measures to identify "gateway" positions critical for career advancement
   - Apply community detection algorithms to identify clusters of commonly linked positions within and across branches
   - Analyze structural holes to identify potential mobility barriers between career segments
   - Calculate network density within and between branches to assess cross-branch mobility

3. **Path Analysis**:
   - Identify common career trajectories using sequence analysis of position transitions
   - Calculate transition probabilities between key positions
   - Measure career velocity (rate of promotion/advancement) across different starting points
   - Compare path diversity across branches to identify differing career flexibility

4. **Comparative Analysis**:
   - Compare network structures across the four branches to identify structural differences in career paths
   - Analyze differences in promotion velocity and career ceiling based on branch, commissioning source, and key early career positions
   - Assess the impact of broadening assignments and education on career trajectories
   - Evaluate the influence of mentorship relationships on career outcomes

5. **Predictive Modeling**:
   - Develop exponential random graph models (ERGMs) to identify factors that predict successful transitions to key career positions
   - Use machine learning approaches to identify combinations of factors associated with reaching senior ranks

### Potential Findings

The SNA of U.S. Army officer career trajectories may reveal several important patterns:

1. **Critical Path Positions**: Certain key assignments likely function as "gateways" to senior leadership, with high betweenness centrality in the career network. These might differ significantly across branches, with technical branches like Cyber potentially showing more diverse paths than traditional combat arms like Armor.

2. **Branch Mobility Patterns**: Network analysis may reveal structural differences in career flexibility, with some branches (potentially Aviation and Cyber) displaying greater specialization and others (potentially Logistics) showing more diverse career path options and cross-functional mobility.

3. **Mentorship Impact**: Officers with stronger mentorship connections (higher degree centrality in the officer relationship network) may show accelerated career progression, particularly in transitions to command positions.

4. **Educational Influence**: Advanced civilian education might create alternative pathways to senior positions, particularly in technical branches like Cyber, while traditional military education might remain more critical in Armor and Aviation.

5. **Performance Threshold Effects**: Network analysis may reveal that performance indicators function not as linear predictors but as threshold requirements at critical career junctures, with different thresholds across branches.

6. **Temporal Evolution**: Career networks for newer branches like Cyber likely show more rapid structural evolution over time compared to established branches like Armor with more stable traditional career paths.

7. **Cross-Branch Differences**: Aviation and Cyber branches may demonstrate more specialized and siloed career networks with fewer transitions to general leadership roles, while Armor officers might show greater representation in joint and strategic positions.

### Potential Implications

The findings from this SNA study could have significant implications for Army talent management:

1. **Talent Management System Refinement**: Identified critical pathway positions could be incorporated into career planning tools, helping officers make more informed decisions about assignment preferences and helping the Army optimize officer placement.

2. **Mentorship Program Enhancement**: Understanding the impact of mentorship networks could inform the development of more effective formal mentorship programs, particularly for officers in branches with more technical specialization.

3. **Branch-Specific Development Programs**: Differences in career network structures across branches might suggest the need for customized professional development approaches rather than a one-size-fits-all career management model.

4. **Diversity and Inclusion Strategies**: Network analysis might reveal structural barriers that disproportionately affect certain demographic groups, informing targeted interventions to ensure equitable advancement opportunities.

5. **Cross-Functional Leader Development**: Identifying structural holes between branch communities could highlight opportunities for creating new broadening assignments that build cross-functional capabilities, particularly important as warfare becomes more multi-domain.

6. **Future Force Planning**: Understanding career path evolution over time, particularly in newer branches like Cyber, could help predict future senior leadership composition and identify potential gaps in leadership development pipelines.

7. **Retention Strategy Development**: Network analysis might identify critical career transition points with high attrition, allowing for targeted retention efforts at these junctures.

8. **Educational Investment Allocation**: Findings regarding the impact of various educational experiences on career trajectories could inform more strategic allocation of limited educational opportunity slots and resources.

## Sources
[1] Social Network Analysis 101: Ultimate Guide https://visiblenetworklabs.com/guides/social-network-analysis-101/\
[2] What Is a Career Trajectory? (And How To Create One) | Indeed.com https://www.indeed.com/career-advice/career-development/what-is-career-trajectory\
[3] Variables - Broadcom Tech Docs https://techdocs.broadcom.com/us/en/ca-mainframe-software/performance-and-storage/ca-netmaster-network-automation/12-2/administrating/variables.html\
[4] Social Network Analysis: Understanding Centrality Measures https://cambridge-intelligence.com/keylines-faqs-social-network-analysis/\
[5] SNA Software LLC - Project Management Symposium https://pmsymposium.umd.edu/pm2023/sponsor/sna-software-llc/\
[6] Using social network analysis to track career trajectories of women ... https://www.emerald.com/insight/content/doi/10.1108/edi-09-2017-0183/full/html\
[7] Social Network Analysis - Cambridge University Press https://www.cambridge.org/core/books/social-network-analysis/90030086891EB3491D096034684EFFB8\
[8] [PDF] Leadership Network Analysis - Kellogg School of Management https://www.kellogg.northwestern.edu/faculty/uzzi/ftp/teaching%20materials/Example_std_papers/LeadershipNetworks_EMP70.pdf\
[9] Social network analysis - Wikipedia https://en.wikipedia.org/wiki/Social_network_analysis\
[10] Using social network analysis to track career trajectories of women ... https://researchwith.njit.edu/en/publications/hidden-patterns-using-social-network-analysis-to-track-career-tra\
[11] Social network analysis: methods and applications by Stanley ... https://archive.org/details/SocialnetworkanalysisWassermanFaust1994\
[12] Social Network Analysis - an overview | ScienceDirect Topics https://www.sciencedirect.com/topics/social-sciences/social-network-analysis\
[13] [PDF] Using Network Analysis of Job Transitions to Inform Career Advice https://dspace.mit.edu/bitstream/handle/1721.1/143136/clochard_axellecb_sm_tpp_eecs_2022.pdf?sequence=1&isAllowed=y\
[14] [PDF] Social Network Analysis: An Introduction - ICPSR https://www.icpsr.umich.edu/summerprog/biblio/2012/Social%20Network%20Analysis%20An%20Introduction.pdf\
[15] Social Network Analysis: An Introduction by Orgnet,LLC http://www.orgnet.com/sna.html\
[16] What are some real life use cases of network analysis? - Reddit https://www.reddit.com/r/datascience/comments/wn9ti3/what_are_some_real_life_use_cases_of_network/\
[17] Social Network Analysis https://www.publichealth.columbia.edu/research/population-health-methods/social-network-analysis\
[18] "Women AD Career Paths" by Mary C. Motley, Jonathan A. Jensen ... https://scholarcommons.sc.edu/jiia/vol18/iss1/3/\
[19] International Network for Social Network Analysis | INSNA https://www.insna.org\
[20] Full article: Managers' career paths and interlocal collaboration https://www.tandfonline.com/doi/full/10.1080/14719037.2023.2189902\
[21] There's an SNA review in my children's school. So I have ... - Instagram https://www.instagram.com/reel/DJH9P_BM_Uh/\
[22] Using Network Analysis to Assess Confidence in Research Synthesis http://ischool.illinois.edu/research/projects/career-using-network-analysis-assess-confidence-research-synthesis\
[23] Modeling scientific workforce dynamics using social network analysis https://reporter.nih.gov/project-details/8798219\
[24] Social Network Analysis 1ed by Stanley Wasserman - Books-A-Million https://www.booksamillion.com/p/Social-Network-Analysis/Stanley-Wasserman/9780521387071\
[25] 1 - Social Network Analysis in the Social and Behavioral Sciences https://www.cambridge.org/core/books/social-network-analysis/social-network-analysis-in-the-social-and-behavioral-sciences/3C435D0A16BA2D9F6566FD4A06FC6FAB\
[26] [PDF] Social Network Analysis - Department of Economics Cybernetics https://www.asecib.ase.ro/mps/Social%20Network%20Analysis%20%5B1994%5D.pdf\
[27] Social Network Analysis: Methods and Applications - Google Books https://books.google.com/books?id=CAm2DpIqRUIC&printsec=copyright\
[28] Wasserman, S. and Faust, K. (1994) Social Network Analysis ... https://www.scirp.org/reference/referencespapers\
[29] SNA Review (Mainstream) – National Council for Special Education https://ncse.ie/sna-review-mainstream\
[30] The SNA review: main points and recommendations http://forsatradeunion.newsweaver.com/designtest/1p1kqgvjncj\
[31] Collaborative Strength & Needs Assessment (SNA) - Etio Global https://blog.etioglobal.org/blog/collaborative-strength-needs-assessment-sna-gaining-insight-through-problems-of-practice\
[32] Readers react to SNA criticism - FoodService Director https://www.foodservicedirector.com/foodservice-operations/readers-react-to-sna-criticism\
[33] Several key issues outlined for SNA contract review http://forsatradeunion.newsweaver.com/designtest/1in1eybwdzh\
[34] SNA review mustn't rob Peter to pay Paul - Forsa https://www.forsa.ie/sna-review-mustnt-rob-peter-to-pay-paul/\
