# What Drives GDP per Capita? Insights from 2021 World Bank Data

Economic prosperity varies widely across countries. Using 2021 World Bank development indicators, this analysis explores which factors are most strongly associated with **GDP per capita** and whether these indicators can be used to build a predictive model.

---

## Data and Approach

The dataset consists of country-level development indicators for the year 2021, covering areas such as health, digital access, energy consumption, inflation, trade, and labor markets. After cleaning and reshaping the data into a wide format (one row per country), indicators with excessive missing values were removed, and a small number of countries with extremely sparse data were excluded.  

The analysis follows the **CRISP-DM** framework, combining exploratory data analysis with regression modeling.

---

## Key Patterns in the Data

Several clear patterns emerge from the exploratory analysis:

- **Life expectancy** shows a strong positive relationship with GDP per capita, indicating that countries with better health outcomes tend to be wealthier.
- **Internet usage** is highly correlated with income levels, highlighting the importance of digital connectivity in modern economies.
- **Electricity access** is nearly universal for many countries, revealing a saturation effect: once full access is achieved, further gains are associated with diminishing income differences.
- Macroeconomic indicators such as **inflation** and **unemployment** show weaker and more dispersed relationships with GDP per capita.

Correlation analysis using a log transformation of GDP per capita reinforces these findings, with internet usage and life expectancy exhibiting the strongest positive correlations.

---

## Modeling GDP per Capita

Two models were trained to predict GDP per capita from the remaining indicators:

- **Linear Regression** as a baseline model
- **Random Forest Regressor** to capture non-linear relationships and interactions

The Random Forest model performed substantially better, achieving higher explanatory power and lower prediction errors. This suggests that economic development is influenced by complex, non-linear interactions among indicators rather than simple linear effects.

---

## Feature Importance

Feature importance from the Random Forest model highlights the most influential predictors:

1. Life expectancy at birth  
2. Internet usage (% of population)  
3. Electric power consumption per capita  

These results emphasize the close connection between health, technology adoption, energy use, and economic prosperity.

---

## A “What-If” Scenario

To illustrate the model’s behavior, a hypothetical country with strong health outcomes, high digital connectivity, and near-universal electricity access was evaluated. The model predicts a GDP per capita of approximately **$11,500**, reflecting patterns learned from observed 2021 data. This estimate should be interpreted as illustrative rather than causal or predictive.

---

## Takeaways

- Health and access-related indicators are consistently associated with higher GDP per capita.
- Non-linear models capture cross-country income variation more effectively than simple linear approaches.
- Digital connectivity and infrastructure appear to be central correlates of economic prosperity.

---

## Limitations

This analysis is based on a single-year snapshot and cannot establish causality or long-term trends. Country-level averages also mask within-country inequality, and some indicators exhibit skewness and outliers despite careful preprocessing.

---

**Data source:** World Bank World Development Indicators (2021)
