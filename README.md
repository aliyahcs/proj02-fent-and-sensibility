# Project 02 Proposal: <your project title>

**Team members:** Aliyah Cardenas, Gabriel Stomberg-Fannon

See the [Project 02 instructions](https://data385.github.io/project/proj02_wholegame.html) for what goes in each section. Bullet points are great. Put any images in an `img/` folder.

## 1. Problem statement

_Who has the problem, what decision or need it involves, why it matters, and what you expect to find._

- **Who:** California's Department of Health Care Services (DHCS) and county public health departments, which give out free naloxone (Narcan) through the Naloxone Distribution Project since 2018.
- **Decision:** How to split a limited naloxone supply across 58 counties
- **Why it matters:** Opioid overdoses, mostly fentanyl, are a leading cause of preventable death in California. Naloxone reverses opioid overdoses, so if it works and reaches the right places, more overdoses should end in survival.
- **What we expect:** Counties with more naloxone per person will have a smaller share of fatal overdoses. The effect may be weak since naloxone is typically sent where overdoses rates are already high, and COVID drastically changed overdose patterns shortly after the Naloxone Distribution Project began.

## 2. Research question

In California counties, is naloxone distribution per 100,000 residents associated with a larger drop in the share of fatal opioid overdoses after the Naloxone Distribution Project began?
- **Response:** fatality share = overdose deaths ÷ (overdose deaths + overdose ER visits)
- **Predictors:** naloxone kits per 100k, period (before: 2017–2018, after: 2022–2024), and their interaction

## 3. Data acquisition

All sources are public government data, joined by county and year

- Opioid overdose deaths, ER visits, and buprenorphine prescriptions (main addiction treatment drug to consider; may influence rate of fatal overdoses as well) by county and year (2017–2024): downloaded as CSVs from the [CDPH Overdose Surveillance Dashboard](https://skylab.cdph.ca.gov/ODdash/)
- Naloxone kits per 100k by county: from [DHCS Naloxone Distribution Project data](https://californiaopioidresponse.org/outcomes/naloxone-distribution-project-data/)
- Poverty rate (as a control): [Census American Community Survey](https://data.census.gov/) 
- Rural/urban codes (also as a control): [USDA Rural-Urban Continuum Codes](https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/)


### a. Confirm viability

_Scraping: summarize the "Before You Scrape" checklist. Downloading: citation, link to the documentation, and how the data were originally collected. Collecting it yourself: how you are collecting it and where you are storing it._


### b. Variables of interest

_If you do not have the data yet, list the variables you plan to collect and the exact question text. Include 1) the variable name, 2) data type 3) description. Use bullet points._


## 4. Data example

_Scraping: a URL and an annotated screenshot. Downloading: a link to your rendered `data_management.pdf` with `glimpse()`. Collecting: a screenshot of one example row._


## 5. EDA

_The techniques and functions you plan to use to import, wrangle, visualize, and explore the data, and why each is needed._


## 6. Modeling

_The models you plan to use, your response and predictor variables, and why the models fit your research question._


## 7. Communicate

_How you plan to present your results (website, poster, or short slide presentation)._


## 8. LLM disclaimer

_Whether and how you will use AI tools: the specific tool, its use, and your data protection methods. If you won't use any, say so._

