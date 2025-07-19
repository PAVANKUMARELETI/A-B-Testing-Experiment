# 📊 Marketing A/B Testing: Conversion Optimization Case Study

## 🏢 About the Project

This project explores a real-world marketing A/B testing scenario, where a company tests two variations of a web page (Control vs Treatment) to understand which version leads to higher user conversions. Using statistical testing, the goal is to determine if observed differences in conversion rates are significant enough to influence a business decision.

---

## 📌 Problem Statement

The marketing team suspects that a new version of the webpage might improve conversion rates. They randomly split users into two groups — control and treatment — and record their conversion behavior.

---
# A/B Test Analysis Report

## 1. Introduction

This report summarizes the results of an A/B test conducted to determine if a new page design (represented by the 'ad' test group) leads to a statistically significant increase in conversion rate compared to the existing page design (represented by the 'psa' test group).

## 2. Hypothesis

The hypothesis being tested is:

*   **Null Hypothesis (H₀):** There is no statistically significant difference in conversion rates between the new page design ('ad' group) and the existing page design ('psa' group).
*   **Alternative Hypothesis (H₁):** There is a statistically significant difference in conversion rates between the new page design ('ad' group) and the existing page design ('psa' group).

## 3. Data and Methodology

The analysis was performed using the "marketing-ab-testing" dataset obtained from Kaggle. The dataset contains information on user interactions, including which test group they belonged to ('ad' or 'psa') and whether they converted.

The methodology followed includes:

*   **Data Loading and Initial Exploration:** The dataset was loaded into a pandas DataFrame. Initial checks were performed to understand the data structure, identify missing values, and confirm the presence of both test groups.
*   **Data Cleaning:** Missing values were inspected. No critical missing values were found in the essential columns ('test group', 'converted').
*   **Conversion Rate Calculation:** The conversion rate for each test group was calculated as the proportion of users in that group who converted.
*   **Statistical Significance Test:** A Chi-squared test for independence was conducted on a contingency table of 'test group' and 'converted' status to determine if the observed difference in conversion rates was statistically significant. A significance level (alpha) of 0.05 was used.
*   **Other Group Analysis:** Additional exploration was performed on the distribution of 'total ads', 'most ads day', and 'most ads hour' for each group to understand other behavioral characteristics.
*   **Revenue Estimation:** An estimate of potential revenue from the 'ad' campaign was calculated based on the number of conversions and an assumed revenue per conversion.

## 4. Results

### Conversion Rates

The conversion rates for each test group were calculated as follows:

*   **'ad' group (New Page):** 2.5547%
*   **'psa' group (Existing Page):** 1.7854%

The 'ad' group showed a higher conversion rate compared to the 'psa' group.

### Statistical Test Results

A Chi-squared test was performed to assess the statistical significance of the observed difference.

*   **Chi-squared Statistic:** 54.0058
*   **P-value:** 0.0000
*   **Degrees of Freedom:** 1

Using a significance level of 0.05, the p-value obtained from the Chi-squared test (0.0000) is less than 0.05.

### Estimated Revenue

Based on 14423 conversions in the 'ad' group and an assumed average revenue of $10 per conversion:

*   **Estimated Total Revenue from 'ad' campaign:** $144230.00

**Note:** This is an estimate based on an assumption. Actual revenue data per conversion would be needed for a precise calculation.

### Other Group Analysis Findings

Analysis of 'total ads', 'most ads day', and 'most ads hour' between the 'ad' and 'psa' groups indicated that the distribution of these characteristics was broadly similar across both groups. This suggests that the groups were comparable in terms of general ad exposure patterns.

## 5. Conclusion

Based on the statistical analysis, we **reject the null hypothesis**.

The observed difference in conversion rates between the 'ad' group (new page design) and the 'psa' group (existing page design) is **statistically significant**. The 'ad' group had a conversion rate of 2.5547%, which is 0.7692% higher than the 'psa' group's conversion rate of 1.7854%.

While other explored user characteristics like 'total ads', 'most ads day', and 'most ads hour' were similar between the groups, the significant difference in conversion rate strongly suggests that the new page design itself had a positive impact on conversions.

**Recommendation:** Given the statistically significant increase in conversion rate and the estimated potential revenue gains, it is recommended to launch the new page design to all users. Further analysis with actual revenue data and potential follow-up tests could provide even more refined insights.

## 6. Code

The Python code used for this analysis is available in the accompanying notebook. The key steps included data loading, data exploration, calculation of conversion rates using pandas, performing the chi-squared test using `scipy.stats.chi2_contingency`, and basic analysis of other user interaction features.

