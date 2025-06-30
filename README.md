# A/B Testing on Marketing Campaign Performance

This project applies **A/B testing** to evaluate the effectiveness of two marketing campaigns — a _Control_ campaign and a _Test_ campaign — in influencing customer engagement and conversion. The analysis investigates **statistically significant differences** across key performance metrics.

## Dataset Description

The dataset contains records from two distinct advertising campaigns, with the following features:

- **Campaign Name**: Identifies whether the row belongs to the _Control_ or _Test_ group  
- **Date**: Date of each record  
- **Spend**: Amount spent on the campaign (AUD)  
- **# of Impressions**: Number of times the ad was shown  
- **Reach**: Number of unique users reached by the ad  
- **# of Website Clicks**: Number of clicks to the website  
- **# of Searches**: Number of users who searched the website  
- **# of View Content**: Number of users who viewed product content  
- **# of Add to Cart**: Number of users who added items to the cart  
- **# of Purchase**: Number of completed purchases  

## Objective

To assess whether the _Test_ campaign outperforms the _Control_ campaign in key marketing metrics, using **independent t-tests**.

"# of Impressions": Number of times the ad was shown

Reach: Number of unique users reached by the ad

"# of Website Clicks": Number of clicks to the website

"# of Searches": Number of users who searched the website

"# of View Content": Number of users who viewed product content

"# of Add to Cart": Number of users who added items to the cart

"# of Purchase": Number of completed purchases

Objective
To assess whether the Test campaign outperforms the Control campaign in key marketing metrics, using independent t-tests.

Methodology
Data Cleaning

### 1. Data Cleaning
Rows containing missing values were dropped due to the relatively small sample size, to preserve data integrity.

### 2. Group Separation
Data was split into _Control_ and _Test_ groups for comparison.

### 3. Statistical Testing
Welch’s t-tests were used to compare group means for each metric at a 95% confidence level (**α = 0.05**).

### 4. Interpretation
Statistical significance was determined based on _p-values_ and _critical t-values_.

## Key Results

| Metric                 | T-Statistic | P-Value | Statistically Significant? |
|------------------------|-------------|---------|-----------------------------|
| # of Impressions       | 4.9161      | 0.0000  | Yes                         |
| Reach                  | 5.3251      | 0.0000  | Yes                         |
| # of Website Clicks    | -1.5761     | 0.1205  | No                          |
| # of Searches          | -1.1244     | 0.2678  | No                          |
| # of View Content      | 0.4740      | 0.6374  | No                          |
| # of Add to Cart       | 4.2375      | 0.0001  | Yes                         |

## Conclusion

Key Results
Metric	T-Statistic	P-Value	Statistically Significant?
"# of Impressions"	4.9161	0.0000	Yes
Reach	5.3251	0.0000	Yes
"# of Website Clicks"	-1.5761	0.1205	No
"# of Searches"	-1.1244	0.2678	No
"# of View Content"	0.4740	0.6374	No
"# of Add to Cart"	4.2375	0.0001	Yes

## Requirements

- Python 3.8 or higher  
- pandas  
- numpy  
- scipy  
- matplotlib _(optional, for visualisation)_

## How to Run

1. Clone this repository  
2. Open the Jupyter Notebook  
3. Run all cells in order to reproduce the analysis
