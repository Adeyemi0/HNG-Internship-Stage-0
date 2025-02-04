ps://hng.tech/hire)
# Table of Contents
- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Data Dictionary](#data-dictionary)
- [Data Description](#data-description)
- [Observations](#observations)
  - [Data Categories](#data-categories)
  - [Missing Values](#missing-values)
  - [Skewness and Kurtosis](#skewness-and-kurtosis)
  - [Not Normal](#not-normal)
  - [High Variability](#high-variability)
  - [Engagement and Reach Metrics](#engagement-and-reach-metrics)
  - [Interactions (Likes, Comments, Shares)](#interactions-likes-comments-shares)
  - [Impressions by People Who Have Liked Your Page](#impressions-by-people-who-have-liked-your-page)
- [Conclusion](#conclusion)

## Introduction

In this report, we analyze a dataset containing social media post performance metrics. The dataset provides insights into how posts are received by users, including engagement levels, reach, and impressions. Our goal is to identify patterns, trends, and potential areas for improvement in social media strategies.

This document is structured to provide a clear understanding of the dataset, its contents, and key observations derived from the data. Let’s dive in!

---

## Dataset Overview

The dataset comprises 500 rows and 19 columns, with each row representing a post on a social media platform. It captures various metrics related to post performance, such as likes, comments, shares, and impressions. 

Access the dataset [here](https://www.kaggle.com/datasets/masoodanzar/facebook-metrics).

---

## Data Dictionary

Below is a detailed breakdown of the dataset's columns, their descriptions, data types, and categories:

| **Column Name**                          | **Description**                                                                 | **Data Type** | **Data Category**                                      |
|------------------------------------------|---------------------------------------------------------------------------------|---------------|-------------------------------------------------------|
| `Page total likes`                       | Total number of likes on the page                                               | `integer`     | Ratio                                                 |
| `Type`                                   | Type of post (e.g., photo, video, link)                                         | `text`        | Nominal                                               |
| `Category`                               | Numerical representation of the post category                                  | `integer`     | Ordinal                                               |
| `Post Month`                             | Month when the post was made (1-12)                                            | `integer`     | Ordinal                                               |
| `Post Weekday`                           | Day of the week when the post was made (1-7)                                   | `integer`     | Ordinal                                               |
| `Post Hour`                              | Hour of the day when the post was made (0-23)                                  | `integer`     | Interval                                              |
| `Paid`                                   | Whether the post was paid (0 = unpaid, 1 = paid)                               | `decimal`     | Nominal                                               |
| `Lifetime Post Total Reach`              | Total unique people who have seen the post                                     | `integer`     | Ratio                                                 |
| `Lifetime Post Total Impressions`        | Total number of impressions for the post                                       | `integer`     | Ratio                                                 |
| `Lifetime Engaged Users`                 | Total users who engaged with the post (liked, commented, shared)               | `integer`     | Ratio                                                 |
| `Lifetime Post Consumers`                | Number of people who clicked on any post content                               | `integer`     | Ratio                                                 |
| `Lifetime Post Consumptions`             | Number of clicks on the post                                                    | `integer`     | Ratio                                                 |
| `Lifetime Post Impressions by people who have liked your Page` | Impressions by users who liked the page                            | `integer`     | Ratio                                                 |
| `Lifetime Post reach by people who like your Page` | Reach by users who liked the page                             | `integer`     | Ratio                                                 |
| `Lifetime People who have liked your Page and engaged with your post` | Users who liked the page and engaged with the post | `integer`     | Ratio                                                 |
| `comment`                                | Number of comments on the post                                                  | `integer`     | Ratio                                                 |
| `like`                                   | Number of likes on the post                                                     | `decimal`     | Ratio                                                 |
| `share`                                  | Number of shares on the post                                                    | `decimal`     | Ratio                                                 |
| `Total Interactions`                     | Total interactions (likes, shares, comments)                                    | `integer`     | Ratio                                                 |

---

## Data Description

Here’s a statistical summary of key metrics in the dataset:

| Metric                                                | Count | Mean      | Std       | Min   | 25%     | 50%    | 75%     | Max     | Skewness  | Kurtosis    | Normality   |
|------------------------------------------------------|-------|-----------|-----------|-------|---------|--------|---------|---------|-----------|-------------|-------------|
| Lifetime Post Total Reach                            | 500   | 13903.36  | 22740.79  | 238   | 3315.00 | 5281   | 13168   | 180480  | 3.679156  | 16.799927   | Not Normal  |
| Lifetime Post Total Impressions                      | 500   | 29585.95  | 76803.25  | 570   | 5694.75 | 9051   | 22085   | 1110282 | 8.351008  | 94.001955   | Not Normal  |
| Lifetime Engaged Users                               | 500   | 920.34    | 985.02    | 9     | 393.75  | 625.5  | 1062    | 11452   | 4.515920  | 34.111231   | Not Normal  |
| Lifetime Post Consumers                              | 500   | 798.77    | 882.51    | 9     | 332.50  | 551.5  | 955.5   | 11328   | 5.033075  | 44.956253   | Not Normal  |
| Lifetime Post Consumptions                           | 500   | 1415.13   | 2000.59   | 9     | 509.25  | 851    | 1463    | 19779   | 4.817636  | 31.379382   | Not Normal  |
| Lifetime Post Impressions by people who have liked your Page | 500   | 16766.38  | 59791.02  | 567   | 3969.75 | 6255.5 | 14860.5 | 1107833 | 14.723360 | 247.437818  | Not Normal  |
| Lifetime Post reach by people who like your Page     | 500   | 6585.49   | 7682.01   | 236   | 2181.50 | 3417   | 7989    | 51456   | 2.609003  | 8.161768    | Not Normal  |
| Lifetime People who have liked your Page and engaged with your post | 500   | 609.99    | 612.73    | 9     | 291.00  | 412    | 656.25  | 4376    | 2.991649  | 11.347677   | Not Normal  |
| comment                                              | 500   | 7.48      | 21.18     | 0     | 1.00    | 3      | 7       | 372     | 11.767564 | 183.439970  | Not Normal  |
| like                                                 | 499   | 177.95    | 323.40    | 0     | 56.50   | 101    | 187.5   | 5172    | 8.955313  | 119.182444  | Not Normal  |
| share                                                | 496   | 27.27     | 42.61     | 0     | 10.00   | 19     | 32.25   | 790     | 12.161379 | 208.542954  | Not Normal  |
| Total Interactions                                   | 500   | 212.12    | 380.23    | 0     | 71.00   | 123.5  | 228.5   | 6334    | 9.712906  | 138.715780  | Not Normal  |

---

## Observations

### Data Categories

The dataset contains four main categories:
- **Numeric**: 14 columns  
- **Categorical**: 2 columns  
- **Ordinal**: 2 columns  
- **Nominal**: 1 column (`Paid`, indicating whether the post was paid or not)

### Missing Values

Some columns have missing values:
- `Paid`: 1 missing value  
- `Like`: 1 missing value  
- `Share`: 4 missing values  

### Skewness and Kurtosis

Most metrics exhibit high skewness and kurtosis:
- High skewness indicates right-skewed distributions, where a few posts have significantly higher metrics compared to the majority.
- High kurtosis suggests the presence of outliers, likely representing viral posts or exceptional engagement.

### Not Normal

None of the metrics follow a normal distribution. This is typical for social media data, where most posts receive low engagement, but a few generate extraordinarily high interactions.

### High Variability

Standard deviations are much larger than means for most metrics. For example:
- *Lifetime Post Total Impressions*: Mean = 29,585.95; Std = 76,803.25  
This variability highlights the disparity between average and outlier posts.

### Engagement and Reach Metrics

Key metrics like *Lifetime Post Total Reach* and *Lifetime Post Total Impressions* show high values but are heavily skewed. A small subset of posts drives the majority of these metrics.

### Interactions (Likes, Comments, Shares)

Metrics for likes, comments, and shares also display high skewness and kurtosis. Most posts receive minimal interactions, while a few attract significant attention.

### Impressions by People Who Have Liked Your Page

While metrics like *Lifetime Post Impressions by People Who Have Liked Your Page* are high, they remain right-skewed. This suggests that engagement is concentrated among a smaller group of users.

---

## Conclusion

This analysis reveals the inherent variability and non-normality of social media post performance. While most posts receive limited engagement, a select few generate disproportionately high reach, impressions, and interactions. Understanding these patterns can help refine social media strategies, focusing on factors that drive viral success.

Let’s keep exploring and refining our approach! 🚀
