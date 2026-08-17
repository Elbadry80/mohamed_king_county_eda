# King County Housing EDA

## Project Overview

This project presents an Exploratory Data Analysis (EDA) of the King County housing market in and around Seattle, Washington.

The objective is to transform housing sales data into practical insights and recommendations for a specific client.

---

## Client – Nicole Johnson

Nicole is looking to buy a house in the Seattle area.

Her main priorities are:

- A relatively central location
- A middle price range
- A good balance between living space and affordability
- Flexibility regarding the timing of the purchase

The main goal of the analysis is therefore to answer:

**Where, when, and what size of house should Nicole consider?**

---

## Dataset

The analysis is based on the King County Housing dataset.

The dataset contains:

- **21,597 house sales**
- Sales from **May 2014 to May 2015**
- Property and location information for houses in King County

The main variables used in the analysis include:

- `price` – sale price
- `date` – sale date
- `sqft_living` – living space
- `zipcode` – ZIP code
- `lat` – latitude
- `long` – longitude

The original data was stored in two PostgreSQL tables and combined using an SQL JOIN.

---

## Assumptions

Some of Nicole's requirements are not directly defined in the dataset. Therefore, the following analytical assumptions were used.

### Middle Price Range

The middle price range is defined as the middle 50% of house prices:

**$322,000 – $645,000**

This corresponds to the 25th and 75th percentiles of the price distribution.

### Central Location

Central Seattle was used as the geographical reference point.

For the client-specific analysis, properties within **15 km of Central Seattle** were considered relatively central.

### Lively Neighborhood

The dataset does not directly measure whether a neighborhood is lively.

Therefore, this requirement cannot be directly tested with the available data.

---

## Hypotheses

### H1 – Location

**Houses located closer to Central Seattle tend to be more expensive than houses farther away from the city center.**

### H2 – Timing

**House prices vary depending on the time of year, which may create better buying opportunities in certain months.**

### H3 – Size vs. Affordability

**Smaller houses in central locations are more likely to fall within the middle price range than larger houses in the same area.**

---

## Exploratory Data Analysis

The analysis included:

- Inspection of the dataset structure
- Data type validation
- Missing-value analysis
- Duplicate checks
- Identification of potential outliers
- Date conversion and feature engineering
- Definition of the middle price range
- Calculation of distance from Central Seattle
- Correlation analysis
- Grouped price comparisons
- Client-specific filtering
- Data visualization

---

## Key Findings

### H1 – Location

House prices generally decrease as distance from Central Seattle increases.

The median house price was approximately:

- **$638k** within 0–5 km
- **$537k** within 5–10 km
- **$467k** within 10–15 km
- **$310k** beyond 30 km

The **5–15 km range** provides an interesting balance between proximity to Central Seattle and affordability.

---

### H2 – Timing

House prices and the number of available properties vary throughout the year.

For Nicole's relevant market segment — properties within 15 km of Central Seattle and within the target price range:

- **November** had the lowest observed median price at approximately **$453,000**
- **May** had the largest selection with **569 suitable properties**

This indicates a trade-off between price and choice.

---

### H3 – Size vs. Affordability

Living space and house price show a strong positive correlation:

**Correlation = 0.793**

For central properties, the share of houses within Nicole's target price range was:

| Living Space | Share Within Target Price Range |
|---|---:|
| ≤ 1,500 sqft | 63.6% |
| 1,501–2,000 sqft | 67.1% |
| 2,001–2,500 sqft | 47.3% |
| > 2,500 sqft | 14.8% |

Homes between **1,501 and 2,000 sqft** provide a particularly strong balance between living space and the target price range.

---

## Recommendations for Nicole

Based on the analysis:

1. **Location:** Focus primarily on properties within **5–15 km of Central Seattle** to balance centrality and affordability.

2. **Timing:** If price is the main priority, pay particular attention to late-year opportunities such as **November**. If having more properties to choose from is more important, **May** may offer a larger selection.

3. **Living Space:** Prioritize homes around **1,500–2,000 sqft**, where the largest share of central properties falls within the target price range.

The overall recommendation is to consider **location, timing, living space, and price together** rather than optimizing only one factor.

---

## Tools & Technologies

- Python
- pandas
- NumPy
- Matplotlib
- PostgreSQL
- SQLAlchemy
- Jupyter Notebook
- VS Code
- Git & GitHub

---

## Repository Structure

| File / Folder | Description |
|---|---|
| `01_assignment.md` | Original project assignment |
| `02_workflow.md` | Recommended EDA workflow |
| `03_fetching_the_data_eda.ipynb` | Data extraction and SQL JOIN |
| `04_eda.ipynb` | Main exploratory data analysis |
| `column_names.md` | Data dictionary |
| `data/` | Local data directory |
| `README.md` | Project documentation |

---

## Author

**Mohamed Elbadry**

Data Science & AI – Exploratory Data Analysis Project