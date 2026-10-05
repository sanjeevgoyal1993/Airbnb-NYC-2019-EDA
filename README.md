# Airbnb NYC 2019 – Exploratory Data Analysis

An exploratory data analysis of 48,895 Airbnb listings in New York City (2019): where the supply is, what drives the nightly price, which listings, hosts and areas attract guests, and what Airbnb could do with these insights.

- **Notebook:** [Airbnb_NYC_2019_EDA_Capstone.ipynb](Airbnb_NYC_2019_EDA_Capstone.ipynb)
- **Colab (view only):** [open the notebook in Google Colab](https://colab.research.google.com/drive/1eK6Rcac2WAxa5YQ1zBIqu6ehtt4QOQzK). To run it, use File → Save a copy in Drive, then Runtime → Run all.
- **Author:** Sanjeev Goyal. EDA capstone project, AlmaBetter.

## Dataset

Airbnb NYC 2019 listings: 48,895 rows × 16 columns covering the host, borough and neighbourhood, latitude/longitude, room type, nightly price, minimum nights, reviews and availability over the next 365 days. The notebook reads a public CSV copy of the course file, so it runs end to end without mounting Google Drive.

## Approach

1. **Know the data:** data types, duplicates (none) and missing values (all structural: listings that were never reviewed).
2. **Understand the variables:** descriptions, summary statistics and unique values.
3. **Data wrangling:** fill the structural gaps, convert dates, and drop 25 invalid rows (\$0 prices, minimum stays over a year). New features: price band, host portfolio size, stay type, availability band, review recency and a likely-dormant flag. Sanity checks then stop the notebook if the cleaned data breaks an assumption.
4. **25 charts following the UBM rule:** 9 univariate, 11 bivariate (numerical–categorical, numerical–numerical, categorical–categorical) and 5 multivariate. Each chart answers why it was chosen, what it shows and the business impact.
5. **Recommendations and conclusion.**

## Key findings

- **Supply is concentrated.** Manhattan (44.3%) and Brooklyn (41.1%) hold 85% of listings, and ten of 221 neighbourhoods hold 48%.
- **Location and room type set the price.** The median listing costs \$150 a night in Manhattan against \$65 in the Bronx, and an entire home costs over twice a private room (\$160 vs \$70).
- **Price does not buy demand.** Price and review count are almost uncorrelated (r = −0.05). Listings at \$500+ average 11 reviews, against about 25 for listings under \$200.
- **About a quarter of listings look dormant:** no open dates in the next year and no review in the last 12 months.
- **The outer boroughs are under-served.** Staten Island, the Bronx and Queens get about twice the reviews per month of Manhattan and Brooklyn.

## Run locally

```bash
pip install -r requirements.txt
jupyter notebook Airbnb_NYC_2019_EDA_Capstone.ipynb
```

Tested with pandas 2.2 and 3.0, NumPy 2.x, Matplotlib 3.10+ and Seaborn 0.13.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn
