# House-Price-Analysis
This repository contains a detailed analysis of house prices per square foot in Bangalore. The dataset used is `house_price.csv`, which includes property prices and other relevant information.

## Introduction

This project aims to analyze house prices in Bangalore by examining the price per square foot. The analysis includes detecting and removing outliers using various statistical methods, checking data normality, and performing correlation analysis.

1.Basic Exploratory Data Analysis (EDA)

2.Outlier Detection and Removal using various methods

3.Box Plot Analysis to determine the best outlier removal method

4.Histogram and Normality Check with Transformations

5.Correlation Analysis with Heatmap

6.Scatter Plot Analysis to check the correlation between variables


## Project Structure

- `house_price.csv`: Dataset containing house prices and other details.
- ### Dataset : https://drive.google.com/file/d/1UlWRYU0UglE2ex3iFse0J6eCLEU8g98P/view?usp=sharing
- `analysis.ipynb`: Jupyter notebook containing the code and analysis.
- `README.md`: Project overview and documentation.

## Exploratory Data Analysis (EDA)

The EDA involves understanding the basic characteristics of the dataset, including:

- Data types and missing values
- Descriptive statistics
- Distribution of the price per square foot

## Outlier Detection and Removal

### Mean and Standard Deviation Method

Outliers are identified as values that are more than three standard deviations away from the mean.
This method helps in identifying extreme values in the dataset. By removing these outliers, the data becomes less spread out, allowing for a more accurate analysis.

### Percentile Method
Outliers are values outside the 5th and 95th percentiles.
By trimming the extreme 5% of data on both ends, we ensure that our analysis focuses on the central 90% of the data, reducing the influence of extreme values.


### IQR Method
Outliers are values outside the range defined by 1.5 times the interquartile range (IQR).
This method is robust to extreme values and helps to remove data points that deviate significantly from the middle 50% of the data. It effectively reduces the influence of outliers without being too aggressive.

### Z Score Method
The Z-score method standardizes the data and identifies values that are unusually high or low compared to the rest of the data. By focusing on data points within three standard deviations of the mean, this method helps in normalizing the dataset.

### Which Method is Better for Removing Outliers?
Mean and Standard Deviation Method: This method is effective if the data is normally distributed, but it can be sensitive to extreme values. Percentile Method: This method is more robust to extreme outliers as it trims the extreme 5% from both ends. IQR Method: This method is robust and works well for skewed data, as it removes values beyond 1.5 times the IQR from the first and third quartiles. Z-Score Method: Keeps data with z-scores between -3 and 3.other data is removed Generally, the IQR Method and Percentile Method are often more robust and preferred for skewed distributions or data with extreme outliers. consider these data IQR and percentile method is more effective to remove outliers
However, the best method depends on the specific characteristics and requirements of your dataset.

## Correlation Analysis
The correlation between numerical columns is analyzed and visualized using a heatmap.

## Scatter Plot Analysis
Scatter plots are created to check the correlation between variables.

## Conclusion
The analysis provides insights into the distribution and relationships of house prices in Bangalore. Outlier removal methods and transformations help in normalizing the data and improving the analysis.
