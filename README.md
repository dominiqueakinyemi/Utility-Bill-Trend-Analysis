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

I live in an apartment building that pools utility usage and charges each resident their share according to a rate based on occupancy. Previous bills have varied greatly, making it difficult to accurately budget each month. This project will use Excel to analyze data from historical bill statements, identify trends, and predict future bill costs. I will make recommendations for myself and for members of my apartment community to properly budget for monthly bills and to reduce utility costs. I hypothesize that I should expect to pay higher water charges during June, July, and August, as residents may use more water during the summer.

### Skills
- Data cleaning
- Statistical analysis
- Data visualization
- Trend analysis
- Forecasting

### Tools
- Excel (for cleaning, analysis, and visualization)

### Data Sources

Data was obtained from billing statements from 9/25/2022 (apartment move-in) to 5/14/2024 (most recent statement period end). The data set contains the following information: statement date, bill period start date, bill period end date, number of billing days in period, charges for trash, charges for sewer, charges for water, and the rate used for calculations. I created a column to add the specific charges, calculating the total utility bill cost.

### Data Cleaning and Preparation

I performed the following tasks:
1. Entered raw data from billing statements
2. Coverted raw data range to a table
3. Standardized column data types and formatting
4. Removed 9/25/22 statement period, as it was an outlier (shorter length due to move-in date)
5. Added a "Cost Per Day" calculated column:
   - Formulated by dividing the total bill by billing days `=I2/D2`
   - This calculation is helpful because it shows the variation between billing periods using a metric that factors in the number of days in each period.
6. Removed the following columns from table: statement date, bill period end
   - I want to work with the “Bill Period Start” column rather than “Statement Date,” as the former represents the actual period.
   - Each statement period lasts from the 14th of one month until the 14th of the next. All I need is the period start date.
7. Sorted data by period start date in ascending order

### Exploratory Data Analysis

In the initial phase of my analysis, I began by exploring the data's statistics. I aimed to answer the following questions:

What is the average monthly total bill cost? How much do bills vary from the average?
- Used `=AVERAGE`, `=MEDIAN`, =`RANGE`, and `=STDEV.S` functions

Which months have the highest and lowest total bills?
- Used `=MIN` and `=MAX` functions

How much does each type of utility contribute to the overall bill?
- Used tables, pie charts, `=SUM` function

What is the overall trend in monthly total bill costs?
- Used line charts, linear trend lines, conditional formatting 

### Data Analysis

Digging deeper, I asked the following questions:
1. Are there seasonal trends in the data? Do they validate my hypothesis?

   
2. Based on this historical data, what projected utility costs can I expect to pay over the next year?

   


### Results and Findings

The following is a summary of my analysis findings:
1. Since the days in each period vary by month length, I can expect to pay more for longer months.
2. (answer - seasonal patterns)
3. (answer - Do trends in specific charges correlate with trends in the overall bill?)

### Recommendations

Based on this analysis, I recommend the following actions:
- Write here.
- Write here.

### Limitations

The following considerations factored into this analysis:
- **Excluded statement period:** The initial statement period was removed from the dataset during cleaning as this shortened period (pro-rated after move-in) skewed the data analysis process.
- **Small sample size:** Data is only available for 20 statement periods, 19 of which were used in analysis. While this amount of data is smaller than desired, it is comprehensive enough for analysis. I was still able to generate meaningful insights and predictions.
- **Access to bill cost and rate, not utility usage:** This analysis focuses solely on analyzing the utility charges billed each month, since statements do not give specific information on building usage. Charges may include taxes and other fees, as determined by utility management company and apartment complex management. This means it is not possible, with the information available, to distinguish if trends are due to rising costs or rising usage.

### References

1. [Link name.](Link.com)
