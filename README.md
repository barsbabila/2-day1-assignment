# 2-day1-assignment
Day1-assignment

# Group 2 - House Sales: Data Cleaning and EDA

This project explores house sales in King County, Washington, USA. We clean the dataset and examine how price relates to house size, bedrooms, construction quality and location.

## Team members

- Karthikeyan Saravanan
- Emmanuel Marquez
- Bars babila
- Samiha Abeda Nur

## Dataset

We use the **House Sales in King County, USA** dataset from Kaggle, covering sales between May 2014 and May 2015.

- Original dataset: 21,613 rows and 21 columns
- After cleaning: 20,703 rows
- Main variables: price, bedrooms, bathrooms, living area, lot area, floors, condition, grade, construction year and ZIP code

Source: https://www.kaggle.com/datasets/harlfoxem/housesalesprediction

## Data cleaning

We checked the data for duplicate records, missing values and unusual values. We converted the sale date to a datetime format and removed the waterfront and view columns.

We filtered records using the 1st and 99th percentiles of price, living area and bedroom count. This removed 910 records. These thresholds help focus the analysis on typical sales, but may also exclude genuine unusual properties.

For the analysis, we added:

- Living area in square metres
- Price per square foot
- Price per square foot relative to the ZIP code median
- Indicators for basements and recorded renovations
- Construction-period groups


## Exploratory data analysis

The notebook includes:

- Descriptive statistics
- Distributions of prices, sizes and house characteristics
- Comparisons between ZIP codes
- Analysis of grade, basements, renovations, age and condition
- Summary tables using groupby and crosstab
- A Spearman correlation heatmap
- A pair plot of price, living area and bathrooms
- Bedroom and price comparisons across four ZIP codes

## Main findings

- Three- and four-bedroom houses account for most sales.
- Median price generally increases with bedroom count and living area.
- Grade and living area have the strongest correlations with price among the features included in our heatmap: 0.63 and 0.61.
- Prices differ across ZIP codes, even for houses with the same bedroom count.
- Living area, above-ground area and bathrooms contain overlapping information.
- Condition has a weak overall correlation with total price, although patterns may differ within locations.

These findings show associations, not proof of cause and effect.


## Limitations

- The data covers one area in 2014–2015, so the findings may differ elsewhere or today.
- Removing unusual records affects the results.
- Some groups contain fewer sales, making comparisons less reliable.
- Several connected features can affect price at the same time.


