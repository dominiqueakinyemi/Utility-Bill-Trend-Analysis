# Utility Bill Trend Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview

I live in an apartment building that pools utility usage and charges each resident their share according to a rate based on occupancy. Previous bills have varied greatly, making it difficult to accurately budget each month. This project will use Excel to analyze data from historical bill statements, identify trends, and predict future bill costs. I will make recommendations for myself and for members of my apartment community to budget for monthly bills properly and to reduce utility costs.

### Skills
- Data cleaning
- Statistical analysis
- Data visualization
- Trend analysis
- Forecasting

### Tools
- Excel

### Data Sources

Data was obtained from billing statements from 9/25/2022 (apartment move-in) to 6/14/2024 (most recent statement period end). The data set contains the following information: statement date, bill period start date, bill period end date, number of billing days in period, charges for trash, charges for sewer, charges for water, and the rate used for calculations. I created a column to add the specific charges, calculating the total utility bill cost.

### Data Cleaning and Preparation

I performed the following tasks:
1. Entered raw data from billing statements
2. Coverted raw data range to a table
3. Standardized column data types and formatting
4. Removed the 9/25/22 statement period, as it was an outlier (shorter length due to end-of-month move-in date)
5. Added a "Cost Per Day" calculated column
   - Formulated by dividing the total bill by billing days `=I2/D2`
   - This calculation is helpful because it shows the variation between billing periods using a metric that factors in the number of days in each period.
6. Removed the following columns from the table: statement date, bill period end
   - I want to work with the “Bill Period Start” column rather than “Statement Date,” as the former represents the actual period.
   - Each statement period lasts from the 14th of one month until the 14th of the next. All I need is the period start date.
7. Sorted data by period start date in ascending order

### Exploratory Data Analysis

In the initial phase of my analysis, I began by exploring the data's statistics. 

I asked and answered the following questions:

What is the average monthly total bill cost? Are there any significant observations from viewing the data's statistics?
- Average bill is around $70
- All median values are lower than their corresponding averages, suggesting the data’s distribution is positively skewed.
- Used `=AVERAGE`, `=MEDIAN`, =`RANGE`, and `=STDEV.S` functions

Are outliers present in the data? How is the data distributed?
- As suggested by the statistics, the total bill's distribution is skewed right by two high values ($88.19 and 105.02). Since there is no obvious reason for the outliers, I will keep them in my data set and analysis.
- Used `=STDEV.S` and histograms
  
Which months have the highest and lowest total bills?
- December 2023 had the highest bill (one of the outliers, at $105.02). October 2022 had the lowest bill (first full month after move-in).
- Used `=MIN`, `=MAX`, and `=XLOOKUP` functions

How much does each type of utility contribute to the overall bill? How do they correlate with one another?
- Water contributes almost half of the total bill. Sewer and Trash make up the remaining amount, usually equally split.
- Water and Sewer charges appear highly positively correlated with the total bill, while Trash charges show only a slight positive correlation.
- Used tables, pie charts, `=SUM` function, and scatter plots

Which months have the lowest and highest costs per day?
- The highest cost per day was December 2023 and the lowest cost per day was October 2022, the same months as the highest/lowest total bills.
- Used `=MIN` and `=MAX` functions, conditional formatting (color scales)
  
Is there a correlation between the rate and the total bill cost? Between the length of the period and the total bill cost?
- Visually, the cost per day and total bill trends are similar. This suggests billing days is not a significant predictor of costs.
- When outliers for billing days (28 or 29 days for February) are filtered out, billing period length and bill cost have little correlation.
- Rate and bill total have a slightly positive correlation.
- Used line charts, scatter plots, filters

### Data Analysis

Next, I focused on understanding trends, determining potential factors affecting bill cost, and predicting future bills. 

I asked the following questions:

What is the overall trend in total bill costs?
- Total bill costs are **increasing!**
- Used line charts, trendlines, conditional formatting (color scales), and percent change calculations

Are there seasonal trends in the data? 
- No clear seasonal trends year to year.
- Cost increases during the fall and winter and decrease
- Used conditional formatting (color scales), line charts, trendlines

Do trends in specific charges correlate with trends in the overall bill?
-
- Used scatter plots, line charts

Based on the historical data, what utility costs can I expect to pay over the next year?
-
- Used moving averages, forecast trendlines,`=FORECAST` and `=TREND` functions, exponential smoothing


### Results and Findings

The following is a summary of my analysis findings:
1. Since the days in each period vary by month length, I can expect to pay more for longer months.
2. Write
3. Write

### Recommendations

Based on this analysis, I recommend the following actions:
- Budget appropriately for the following utility costs during the upcoming year
- (Efforts can other residents and I make to reduce utility charges during high-cost months?)
- Write here.

### Limitations

The following considerations factored into this analysis:
- **Excluded statement period:** The initial statement period was removed from the dataset during cleaning as this shortened period (pro-rated after move-in) skewed the data analysis process.
- **Small sample size:** Data is only available for 20 statement periods, 19 of which were used in analysis. While this amount of data is smaller than desired, it is comprehensive enough for analysis. I was still able to generate meaningful insights and predictions.
- **Access to bill cost and rate, not utility usage:** This analysis focuses solely on analyzing the utility charges billed each month, since statements do not give specific information on building usage. Charges may include taxes and other fees, as determined by utility management company and apartment complex management. This means it is not possible, with the information available, to distinguish if trends are due to rising costs or rising usage.

### References

1. [Link name.](Link.com)
