# tree_canopy


# Background:
With climate change getting worse, we are seeing more of its negative effects, particularly with the formation of urban heat islands, and reduced air quality in urban environments. These two factors have been linked to increased incidences of asthma, and cardiovascular disease mortality. There are also studies and reports that show that there are certain communities, usually lower income, that are worse off than others in the same city with regards to the same problems. This highlights a need for urban planning solutions that can tackle the problems cities face with equitable solutions. A reduction in negative health outcomes has the effect of increasing quality of life, particularly in at-risk communities, and reducing financial, and physical strain on the public health care system. Trees have been linked in prior studies to myriad positive health outcomes: longer life spans, lower levels of stress, better air quality and lower rates of cardiac disease” (Anderson et al, 2019). Furthermore, a study by University of Exeter concluded that, “People living in polluted urban areas are far less likely to be admitted to hospital with asthma when there are lots of trees in their neighbourhood”, and “suggest[s] that tree planting could play a role in reducing the effects of air pollution (Science Daily, 2017).
Urban Tree Canopy & Health Equity in Denver

# Overview

This project investigates the relationship between tree canopy coverage and health outcomes in the City and County of Denver. Drawing on public data sources from city and state health departments, the analysis seeks to explore whether increasing urban greenery could equitably improve public health—particularly in lower-income neighborhoods affected by heat islands and poor air quality.

# Goals

Analyze whether tree canopy coverage correlates with better health outcomes (e.g., lower asthma rates).

Explore the distribution of tree coverage in relation to socioeconomic factors like income and poverty.

Identify census tracts that may benefit most from urban forestry efforts.

# Key Questions

Is there a relationship between tree canopy coverage and asthma or heart disease outcomes in Denver?

Are lower-income areas systematically disadvantaged in terms of urban tree coverage?

Can we identify a threshold of tree coverage associated with improved health outcomes?

# Data Sources

All data is from 2013 to align across datasets:

Tree Canopy Assessment – City and County of Denver (2013)

Income & Poverty Estimates – CDPHE & U.S. Census ACS (2013-2017)

Asthma Hospitalization & Adult Asthma Prevalence – CDPHE (2013-2017)

Cardiovascular Disease Mortality – CDPHE Vital Records (2013-2017)

Census Tract Boundaries – U.S. Census Bureau and Denver Open Data

# Data Strategy

Normalize and load all datasets into a PostgreSQL database.

Join data across census tracts using FIPS codes.

Query and extract a unified dataset into a Pandas DataFrame via psycopg2.

Analytical Phases

# Phase 1: EDA

Visualize distributions of tree canopy, income, asthma rates, and mortality.

# Phase 2: Correlation Analysis

Use Pearson’s r to assess relationships between tree canopy and:

Asthma hospitalization

Adult asthma prevalence

Cardiovascular disease mortality

Mean household income

# Phase 3: Regression Analysis

Fit linear and non-linear models (Random Forest)

Evaluate predictive value of tree canopy on health outcomes

Investigate where coverage thresholds may imply policy action

# Results Summary

Correlation analysis showed weak or no significant linear relationship between tree canopy and health outcomes.

Regression modeling with Random Forest yielded poor performance (R² = -0.16; MAPE ~35%), indicating that tree canopy alone does not predict asthma hospitalization.

Feature importance analysis showed tree canopy was a weak predictor relative to other factors.

# Interpretation & Next Steps

While the project did not find predictive power in tree canopy alone, it surfaces several critical insights:

Urban greenery’s health impacts are likely mediated through complex, multi-factor dynamics (pollution, healthcare access, housing).

Additional data on air quality, healthcare access, and demographics would strengthen future models.

Geospatial mapping and clustering could provide further granularity to policy suggestions.

# Tools Used

Python (pandas, matplotlib, seaborn, scikit-learn)

PostgreSQL + pgAdmin 4

Jupyter Notebook

SQL (DDL + complex JOIN queries)

### Author

#### Toni Diebolt
