# Table of Contents
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

## Dataset Overview

This dataset consists of 500 rows and 19 columns, with each row representing a post on a social media page. It includes various metrics related to the post's performance. This is just a quick overview of the dataset.

The dataset can be accessed [here](https://www.kaggle.com/datasets/masoodanzar/facebook-metrics).

## Data Dictionary

| **Column Name**                                                   | **Description**                                                                 | **Data Type** | **Data Category**                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------|
| `Page total likes`                                                 | Total number of likes on the page                                               | `integer`       | Ratio (numeric, with meaningful zero and differences between values)             |
| `Type`                                                             | Type of post (e.g., photo, video, link)                                         | `text`      | Nominal (categorical, no inherent order)                                         |
| `Category`                                                         | Category of post (numerical representation)                                     | `integer`       | Ordinal (categorical with meaningful order)                                      |
| `Post Month`                                                       | Month when the post was made (1-12)                                             | `integer`       | Ordinal (categorical with meaningful order)                                      |
| `Post Weekday`                                                     | Day of the week when the post was made (1-7)                                    | `integer`       | Ordinal (categorical with meaningful order)                                      |
| `Post Hour`                                                        | Hour of the day when the post was made (0-23)                                   | `integer`       | Interval (numeric, no true zero but differences are meaningful)                  |
| `Paid`                                                             | Whether the post was paid (0 = unpaid, 1 = paid)                                | `decimal`     | Nominal (categorical, no inherent order)                                         |
| `Lifetime Post Total Reach`                                        | Total number of unique people who have seen the post                            | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime Post Total Impressions`                                  | Total number of impressions for the post                                        | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime Engaged Users`                                           | Total number of users who engaged with the post (liked, commented, shared)      | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime Post Consumers`                                          | Number of people who clicked on any post content                                | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime Post Consumptions`                                       | Number of clicks on the post                                                    | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime Post Impressions by people who have liked your Page`     | Impressions by users who have liked the page                                    | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime Post reach by people who like your Page`                 | Reach by users who have liked the page                                          | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `Lifetime People who have liked your Page and engaged with your post` | Users who liked the page and engaged with the post                              | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `comment`                                                          | Number of comments on the post                                                  | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |
| `like`                                                             | Number of likes on the post                                                     | `decimal`     | Ratio (numeric, meaningful zero, differences between values)                     |
| `share`                                                            | Number of shares on the post                                                    | `decimal`     | Ratio (numeric, meaningful zero, differences between values)                     |
| `Total Interactions`                                               | Total number of interactions (likes, shares, comments)                          | `integer`       | Ratio (numeric, meaningful zero, differences between values)                     |


## Data Description

| Metric                                                                 | Count | Mean      | Std          | Min   | 25%     | 50%   | 75%    | Max     | Skewness  | Kurtosis    | Normality   |
|------------------------------------------------------------------------|-------|-----------|--------------|-------|---------|-------|--------|---------|-----------|-------------|-------------|
| Lifetime Post Total Reach                                              | 500   | 13903.36  | 22740.79     | 238   | 3315.00 | 5281  | 13168  | 180480  | 3.679156  | 16.799927   | Not Normal  |
| Lifetime Post Total Impressions                                         | 500   | 29585.95  | 76803.25     | 570   | 5694.75 | 9051  | 22085  | 1110282 | 8.351008  | 94.001955   | Not Normal  |
| Lifetime Engaged Users                                                 | 500   | 920.34    | 985.02       | 9     | 393.75  | 625.5 | 1062   | 11452   | 4.515920  | 34.111231   | Not Normal  |
| Lifetime Post Consumers                                                | 500   | 798.77    | 882.51       | 9     | 332.50  | 551.5 | 955.5  | 11328   | 5.033075  | 44.956253   | Not Normal  |
| Lifetime Post Consumptions                                             | 500   | 1415.13   | 2000.59      | 9     | 509.25  | 851   | 1463   | 19779   | 4.817636  | 31.379382   | Not Normal  |
| Lifetime Post Impressions by people who have liked your Page            | 500   | 16766.38  | 59791.02     | 567   | 3969.75 | 6255.5| 14860.5| 1107833 | 14.723360 | 247.437818  | Not Normal  |
| Lifetime Post reach by people who like your Page                       | 500   | 6585.49   | 7682.01      | 236   | 2181.50 | 3417  | 7989   | 51456   | 2.609003  | 8.161768    | Not Normal  |
| Lifetime People who have liked your Page and engaged with your post     | 500   | 609.99    | 612.73       | 9     | 291.00  | 412   | 656.25 | 4376    | 2.991649  | 11.347677   | Not Normal  |
| comment                                                                | 500   | 7.48      | 21.18        | 0     | 1.00    | 3     | 7      | 372     | 11.767564 | 183.439970  | Not Normal  |
| like                                                                   | 499   | 177.95    | 323.40       | 0     | 56.50   | 101   | 187.5  | 5172    | 8.955313  | 119.182444  | Not Normal  |
| share                                                                  | 496   | 27.27     | 42.61        | 0     | 10.00   | 19    | 32.25  | 790     | 12.161379 | 208.542954  | Not Normal  |
| Total Interactions                                                     | 500   | 212.12    | 380.23       | 0     | 71.00   | 123.5 | 228.5  | 6334    | 9.712906  | 138.715780  | Not Normal  |

## Observations

### Data Categories

As shown in the data dictionary table above there are four data categories in the dataset:

- **Numeric**: 14 columns
- **Categorical**: 2 columns
- **Ordinal**: 2 columns
- **Nominal**: 1 column (Paid, as it indicates whether the post was paid or not)

### Missing Values

- The **Paid** and **Likes** columns each have 1 missing value.
- The **Share** column has 4 missing values.

### Skewness and Kurtosis

- **Skewness** is high across most metrics, with values far greater than 1, indicating a strong right-skewed (positive skew) distribution. This means there are a few posts that have significantly higher metrics compared to the majority. This could indicate viral posts or outliers.
- **Kurtosis** is also very high for most metrics (above 10 for many), which suggests that the data is highly peaked with outliers (extreme values). These outliers likely represent posts with exceptional engagement, reach, or impressions.

### Not Normal

- The **Normality** column indicates that none of the metrics follow a normal distribution. All metrics exhibit signs of being highly skewed or having heavy tails, as evidenced by the high skewness and kurtosis. This is a typical behavior for social media data, where most posts have low interactions, but a few have extraordinarily high engagement, impressions, or reach.

### High Variability

- The **Standard Deviation (Std)** is very high for most metrics compared to the mean. This shows significant variation in the data. For example, the standard deviation of *Lifetime Post Total Impressions* (76803.25) is much higher than the mean (29585.95), implying that most posts have relatively lower impressions, but a few posts have very high impressions.

### Engagement and Reach Metrics

- *Lifetime Post Total Reach* and *Lifetime Post Total Impressions* show very high values (mean values of 13903 and 29585, respectively), but their standard deviations are much larger than their means, indicating that a few posts significantly contribute to the total reach and impressions.
- The metrics related to *Lifetime Engaged Users*, *Lifetime Post Consumers*, and *Lifetime Post Consumptions* have similarly high standard deviations, suggesting a small number of posts are driving the majority of engagement.

### Interactions (Likes, Comments, Shares)

- **Likes**, **Comments**, and **Shares** exhibit extremely high skewness and kurtosis, suggesting that these actions are concentrated in a small number of posts, while most posts receive very few interactions. For example, *like* has a mean of 177.95 but a standard deviation of 323.40, indicating that some posts receive far more likes than the majority.

### Impressions by People Who Have Liked Your Page

- Metrics like *Lifetime Post Impressions by People Who Have Liked Your Page* and *Lifetime Post Reach by People Who Like Your Page* show high values, but these are still right-skewed, indicating that while some people who like the page may drive a lot of impressions, most interactions are less concentrated.

## Conclusion

This dataset provides valuable insights into the performance of social media posts, highlighting key metrics such as reach, impressions, engagement, and interactions. The data reveals a high degree of variability across posts, with a few posts driving the majority of the metrics, while most posts exhibit lower engagement. The skewness and kurtosis across various metrics suggest that certain posts experience viral-like engagement, significantly outperforming others.

The presence of missing values in some columns suggests that some data points may require further attention before in-depth analysis. The high standard deviations compared to the mean indicate that many of the metrics, such as likes, comments, and impressions, have extreme outliers that could be explored further for understanding the factors driving these outliers.

It is crucial for future analysis to focus on these outliers and variability to uncover deeper insights into user engagement and content strategies.

---

To hire a qualified tech or data analyst, click any of the following links:

- [Hire Data Analysts](https://hng.tech/hire/data-analysts)
- [Hire Tech Professionals](https://hng.tech/hire)
