# Project 02 Proposal: Predicted Opioid Overdose Harm Reduction by Naloxone Distribution Rates in California Counties

**Team members:** Aliyah Cardenas, Gabriel Stomberg-Fannon

See the [Project 02 instructions](https://data385.github.io/project/proj02_wholegame.html) for what goes in each section. Bullet points are great. Put any images in an `img/` folder.

## 1. Problem statement

_Who has the problem, what decision or need it involves, why it matters, and what you expect to find._

- **Who:** California's Department of Health Care Services (DHCS) and county public health departments, which give out free naloxone (Narcan) through the Naloxone Distribution Project since 2018.
- **Decision:** How to split a limited naloxone supply across 58 counties; If the distribution project is worth continuing.
- **Why it matters:** Opioid overdoses, mostly fentanyl, are a leading cause of preventable death in California. Naloxone reverses opioid overdoses, so if it works and reaches the right places, more overdoses should end in survival.
- **What we expect:** Counties with more naloxone per person will have a smaller share of fatal overdoses. 

## 2. Research question

In California counties, is the amount of naloxone distribution per 100k residents associated with a larger drop in the share of fatal opioid overdoses after the Naloxone Distribution Project began?
- **Response:** fatality share = overdose deaths ÷ (overdose deaths + overdose ER visits)
- **Predictors:** naloxone kits per 100k, period (before: 2017–2018, after: 2022–2024)

## 3. Data acquisition

- We intend to gather data from the California Overdose Surveillance Dashboard, the Naloxone Distribution Project, the American Community Survey (Poverty Data Tables), and the US Department of Agriculture (Rural-Urban Continuum Codes)
- All of these are publicly available government datasets with downloadable csv or XLS files.

### a. Confirm viability

_Scraping: summarize the "Before You Scrape" checklist. Downloading: citation, link to the documentation, and how the data were originally collected. Collecting it yourself: how you are collecting it and where you are storing it._

California Overdose Surveillance Dashboard Data:
- Citation: California Overdose Surveillance Dashboard. Prepared by California Department of Public Health (CDPH) - Substance and Addiction Prevention Branch (SAPB). Accessed on 11/18/26. https://skylab.cdph.ca.gov/ODdash/.
- [Data Definitions](https://skylab.cdph.ca.gov/ODdash/?tab=DD)
- [Technical Documentation](https://skylab.cdph.ca.gov/ODdash/?tab=MTH)
- Data was collected from California Department of Public Health 

Naloxone Distribution Project Data:
- Citation: California Department of Health Care Services. (n.d.). Naloxone Distribution Project data. DHCS Opioid Response. Retrieved November 18, 2026, from https://californiaopioidresponse.org/outcomes/naloxone-distribution-project-data/
- Naloxone kits per 100k by county: from [DHCS Naloxone Distribution Project data](https://californiaopioidresponse.org/outcomes/naloxone-distribution-project-data/), [Figure URL](https://datawrapper.dwcdn.net/7e1b4/29/)
- Data was collected by Naloxone Distribution Project

US Census Bureau Poverty Data Tables:
- Poverty rate: Census American Community [Census American Community Survey](https://data.census.gov/)
- [American Community Survey (ACS) Poverty Data Tables](https://www.census.gov/topics/income-poverty/poverty/data/tables/acs.html)
- Data was collected by compiling mandatory household surveys conducted by the U.S. Census Bureau


US Department of Agriculture Rural-Urban Codes: 
- Citation: U.S. Department of Agriculture, Economic Research Service. (January 2024). Rural-Urban Continuum Codes. Accessed on 11/18/26. https://www.ers.usda.gov/data-products/rural-urban-continuum-codes
- [USDA Rural-Urban Continuum Codes](https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/)
- [Documentation](https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/documentation)
- Data was collected by classifying US counties using 2020 Census, 2016–2020 ACS, and 2023 OMB metro data


### b. Variables of interest

_If you do not have the data yet, list the variables you plan to collect and the exact question text. Include 1) the variable name, 2) data type 3) description. Use bullet points._

- Naloxone kits by 100k
- Overdose Rate: Quantitative
- Overdose Count: Quantitative
- Naloxone Distribution Rate by County: Quantitative
- ER Visits: Quantitative
- Stability: Categorical
- Year: Categorical (before/after Naloxone)

## 4. Data example

_Scraping: a URL and an annotated screenshot. Downloading: a link to your rendered `data_management.pdf` with `glimpse()`. Collecting: a screenshot of one example row._

- See data_management.pdf

## 5. EDA

_The techniques and functions you plan to use to import, wrangle, visualize, and explore the data, and why each is needed._

- read_csv and read_xls to import data
- filter() to only keep California counties
- join by county name
- linear_reg to model the relationship
- geom_histogram/geom_point to visualize

## 6. Modeling

_The models you plan to use, your response and predictor variables, and why the models fit your research question._

- Model: simple linear regression: fatality_share ~ naloxone_rate
We expect there to be a mostly linear relationship between fatality share and naloxone distribution rate

- Response: fatality share, quantitative: (overdose deaths ÷ (deaths + ER visits))

- Predictors: naloxone kits per 100k (quantitative), period before/after the program (categorical)

## 7. Communicate

_How you plan to present your results (website, poster, or short slide presentation)._

-Slide show

## 8. LLM disclaimer

_Whether and how you will use AI tools: the specific tool, its use, and your data protection methods. If you won't use any, say so._

-No LLM use
