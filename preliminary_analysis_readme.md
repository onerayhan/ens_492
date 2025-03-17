# Preliminary Analysis


## Concept Analysis in Review Articles

### Overview

Concepts have been extracted from the dataset, and their occurrences have been counted to identify dominant themes.Total Number of 40487 unique concepts have been found. Three main visualizations and some additional data have been produced:

1. A **bar chart** showing the top 20 most frequently mentioned concepts.
![alt text](image.png)   
2. A **line chart** depicting the yearly trend of the top five concepts.
   ![alt text](image-1.png)
3. A *retrospective line chart* signifiyng the number of distinct concepts per year.
![alt text](image-7.png)
4. Another *retrospective line chart* siginfiying the number of distinct concepts per year but this time distinct concepts are weighted by their citation counts and normalized using average citation per year in order not to penalize recent years
![alt text](image-8.png)
5. An *occurence chart* For the R^2 values of the linear regression fitted for each concepts occurence over time weighted by their citation counts and normalized using average citations per year.(1.0 R^2 values represent concepts with 2 data points)
![alt text](image-9.png)  
1. Concept Co-Occurence pairs are generated to see frequently used concepts among top 100 concepts.
 

---

### Interpretation of Findings

#### 1. Distribution of Concepts

The top 20 concepts indicate that review articles are predominantly concentrated in **Natural Sciences**, particularly in the **Medical and Biological fields**. **Medicine** has an overwhelming dominance, significantly outnumbering other concepts, followed by **Computer Science, Political Science, Law, and Biology**. 

Key observations:
- **Medical and Biological Sciences Dominate**: Fields such as **Medicine, Internal Medicine, Pathology, Surgery, Biology, and Psychology** rank among the most frequent. This could indicate a higher demand for systematic reviews and meta-analyses in these disciplines, possibly due to clinical and pharmaceutical research requiring synthesis of prior knowledge.
- **Social Sciences are Represented but Less Frequent**: **Political Science, Law, Sociology, Economics, and Philosophy** appear among the top 20, though at lower frequencies compared to natural sciences.
- **Computer Science and AI Presence**: **Computer Science and Artificial Intelligence** are among the most frequent concepts, highlighting the growth of research synthesis in technological and computational fields.
- **Emergence of AI and Programming Languages**: While **Artificial Intelligence** and **Programming Languages** appear in the list, their relatively lower counts compared to Medicine suggest that AI-driven research synthesis is still emerging.

This extreme concentration of review articles in biological sciences may suggest a pattern of **review article dumping**, where a high volume of review articles is produced to meet publication demands.

---

#### 2. Trend of Top 5 Concepts Over Time

The second visualization tracks how the most frequent concepts have evolved over time.

- **Steady Growth Across Fields**: All five top concepts (**Medicine, Computer Science, Political Science, Law, and Biology**) exhibit an upward trend, indicating an increasing volume of review articles across disciplines.
- **Explosive Growth in Medicine and Computer Science**: While all top concepts are growing, **Medicine** and **Computer Science** show particularly rapid increases, especially after 2018. This suggests a surge in demand for medical reviews, possibly influenced by global health events such as the COVID-19 pandemic.
- **Political Science and Law Remain Stable but Grow**: These fields exhibit a more gradual increase compared to the exponential rise in Medicine and Computer Science.
- **Biology Shows a More Modest Increase**: Compared to Medicine, Biology’s review article growth is more stable and gradual.

#### 3. TOP 10 concept pairs(co-occurence) among top 100 concepts
- Law - Political science: 41652
- Internal medicine - Medicine: 31216
- Medicine - Pathology: 24760
- Computer science - Political science: 21768
- Computer science - Law: 19898
- Medicine - Political science: 19464
- Medicine - Surgery: 19376
- Law - Medicine: 18307
- Computer science - Engineering: 17567
- Law - MEDLINE: 17286
#### 4. Linear Regression fitted to the distinct concept usages per year


Total unique concepts: 40487
Total concept occurrences: 2119183
Average #concept occurrences per paper: 13.26
- Fitted 28887 concepts with >=2 data points for regression.

- Mean slope: 0.5071 | median slope: 0.0218

- Min slope: -108.6911| max slope: 531.0926

- Mean R^2:  0.4345 | median R^2: 0.3130


---
## Affiliation Analysis in Review Articles

### Overview

This section examines the distribution of affiliations contributing to review articles and their citation impact. The analysis includes:

- The number of unique affiliations.
- The top 10 affiliations based on the number of papers contributed.
- A **histogram** of the number of articles per affiliation (log-scaled).
  ![alt text](image-2.png)
- A **scatter plot** showing the relationship between paper count and average citations per affiliation.
![alt text](image-3.png)
---

### Findings


#### 1. Distribution of Affiliations

- A total of **28,005 unique affiliations** have been identified across nearly **200,000 papers**.
- The top affiliations contributing to review articles are primarily large research institutions, including:
  - **University of Toronto** (898 papers)
  - **University College London** (826 papers)
  - **University of Oxford** (717 papers)
  - **Universidade de São Paulo** (588 papers)
  - **Harvard University** (569 papers)

- The histogram of articles per affiliation suggests a **highly skewed distribution**, where most affiliations contribute very few papers, while a small subset of institutions dominate the publication landscape for the review articles.

---

#### 2. Citation Impact of Affiliations

- The top five affiliations with the highest **average citation counts** per paper include:
  - **Alliance for Health Policy and Systems Research** (7489.67 citations per paper out of 3 papers)
  - **Southern California Reproductive Center** (6963.67 citations per paper out of 3 papers)
  - **Mario Negri Institute for Pharmacological Research** (4979.59 citations per paper out of 17 papers)
  - **Royal College of Physicians and Surgeons of Canada** (2541.11 citations per paper out of 9 papers)
  - **Fraunhofer Austria** (2103.00 citations per paper out of 1 paper)

- These institutions have **published a small number of highly cited papers**, suggesting that either:
  1. **Frequent publishers** tend to have **lower average citation counts** due to a mix of highly cited and less impactful papers.
  2. Institutions with fewer but highly cited papers specialize in **landmark studies** that receive exceptional attention.

---

### Visual Insights

- The histogram shows that the majority of affiliations contribute **fewer than 10 papers**, indicating a **potential power-law distribution** in publication counts.
- The scatter plot of **paper count vs. average citations** (both log-scaled) shows a **high variance**, with no clear trend indicating that producing more papers leads to higher average citations.

## Retrospective Citation Analysis

### Overview

This section examines how citation counts evolve over time as papers age. The analysis focuses on:

- The relationship between a paper's age and its mean annual citations.
![alt text](image-4.png)
- The typical citation trajectory for older versus newer papers.
- Identifying potential patterns in citation accumulation.

---

### Findings

- **Older papers tend to accumulate more citations**, as expected, since they have had more time to be referenced.
- **A peak is observed around the 11th year (around 2011)**, which might indicate a particularly productive academic year, but further investigation is required.
- **After the initial surge, citation growth stabilizes**, with fluctuations in later years possibly influenced by field-specific trends or rediscoveries of older work.

## Retrospective Paper Count Analysis

### Overview

**Number of Review Articles by year have steadily increased between 2003 and 2023** with an exponential looking increase(retrospective analysis of Concepts might be performed to compare the increease in unique concepts vs increase in papers) : ![alt text](image-5.png)



## Zero Citation Analysis

### Overview

- **Across all dataset** the ratio of zero cited papers are **36%** of the total number of papers. 
- **Interesting lack of trend**: Fraction of zero cited papers go down until 2013 and then it increased steadily until 2023.
![alt text](image-6.png)

### Findings

While the total amount of papers published by year grows exponentially, zero-cited papers in the dataset shows a chaotic pattern. This might be caused by improper filtering of the zero-cited papers or late published papers are getting more attention with the amount of papers increasing 


## Co-Authorship Network Analysis

### Overview

Predatory Journal's in the dataset are marked according to the beall's list, then a Coauthorship network is created among the predatory journal's subgraph, then it is compared with two types of random network

1. A random network that all authors are selected at random
2. A random network that All authors are selected from random journals
### Findings

- Comparing the Predatory journals netrwork with random journal network no significant difference between community sizes and average degrees have been found using Louivain community detection

- Hovewer, Comparing the network with randomly selected authors from any journal, A significant differenece betwen the community sizes and Average degree has been found meaning, People that have been publisihng review articles from the same journals have a higher chance of Publishing a paper together.

#### Co-Author Network Analysis 

Co-author network => Nodes: 395786 Edges: 1296746

Average degree: 6.55

Pred sub => 8197 nodes, 25866 edges

Random sub => 8197 nodes, 572 edges

--- LOUVAIN (PREDATORY AUTHORS) ---

Louvain found 1823 communities.

Mean size = 4.43, std = 6.26

Top community sizes: [150, 133, 131, 106, 78]

--- LOUVAIN (RANDOM AUTHORS) ---

Louvain found 7661 communities.

Top community sizes: [5, 5, 4, 4, 4]

--- LOUVAIN (RANDOM JOURNALS)

Count of communities = 926

Mean size = 4.82, std = 6.23

Top 5 sizes: [126, 83, 71, 38, 35]