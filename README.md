# Statistical-Analysis-for-CDC-Dataset
The main objective of our project is to examine the relationship between socio-economic (income, age, and race) versus obesity in the United States. As a secondary objective, we aimed to determine if physical activity correlates to obesity, and if income could correlate to lower levels of physical activity.

Data Source and Preparation 
The data for this project was obtained from the CDC’s opensource database, titled “Nutrition, Physical Activity, and Obesity - Behavioral Risk Factor Surveillance System”. The data was inspected, and empty records were discarded from the analysis. A helper function was used to simplify questions in the dataset into smaller statements (e.g., “Percent of adults aged 18 years and older who have obesity” changed to “% of 18+ are obese”). Several fields were renamed for consistency. Additionally, it was noted that Education and Gender were dropped from the analysis as there were insufficient entries to conduct a thorough analysis. 

The Impact of Income on Obesity
H0 – The mean percentage of adults aged 18 and over with obesity is the same across all income brackets
H1 – The mean percentage of adults aged 18 and over with obesity is not the same across all income brackets

ANOVA testing found that there is a statistical difference in the percentage of adults over 18 that suffer from obesity across the income brackets (p value = 5.56e-171). Specifically, it was found that income groups $35,000 - $49,999 and $50,000 - $74,999 are not statistically different (p value = 0.0162), and the income groups $25,000 - $34,999 and $35,000 - $49,999 are not statistically different (p value = 0.5507). However, all other income groups are statistically different from each other. A linear regression model indicated that as the income bracket increases, the percentage of adults 18 and over with obesity decreases1. A logistic regression was performed as we wanted to test whether this relationship exists in a binary case. This model found that the top two income brackets contributed to a lower number of adults with obesity, and the bottom two contributed to an increased number of adults with obesity.

The Impact of Age on Obesity
H0 – The mean percentage of adults aged 18 and over with obesity is the same across all age groups.
H1 – The mean percentage of adults aged 18 and over with obesity is not the same across all age groups.

ANOVA testing found that there is a statistical difference in the percentage of adults over 18 who suffer from obesity across age groups (p-value = 0.0). Specifically, it was found that age groups “25 – 34” and “65 or older” are not statistically different (p-value = 0.0169), and the age groups “45 – 54” and “55 – 64” are not statistically different (p-value = 0.0113). However, all other age groups are statistically different from one another. A linear regression model indicated there is no strong association between age and obesity (p > 0.05)1, and as such we can conclude that overall, an increase in age does not correlate with an increase in obesity in the population. A logistic regression model found that the age groups “18 – 24”, “25 – 34” and “65 or older” contributed to a lower number of adults with obesity, and the age groups “35 – 44”, “45 – 54” and “55 – 64” contributed to an increased number of adults with obesity.

The Impact of Race on Obesity
H0 – The mean percentage of adults aged 18 and over with obesity is the same across all racial groups.
H1 – The mean percentage of adults aged 18 and over with obesity is not the same across all racial groups.

ANOVA testing found that the percentage of adults with obesity is statistically different between different racial groups. Specifically, the mean percentage of adults with obesity among adults who identified as Hawaiian/Pacific Islander (p-value = 0.0059), non – Hispanic Black (p-value = 0.0001), non–Hispanic White (p-value = 0.0073), and Asian (p-value < 0.05), are statistically different from the rest of the sample population. We were unable to conduct a linear regression or a logistic regression comparing the percentage of adults with obesity within the races as this is nominal data.

The Impact of Physical Activity on Obesity
H0 – The percentage of respondents who are obese has no relationship with the percentage of respondents who chose “No Activity” in the survey.
H1 – The percentage of respondents that are obese does have a relationship with the percentage of respondents that chose “No Activity” in the survey.

Prior to conducting a linear regression, the assumptions were tested. It was found that results from Puerto Rico is considered an outlier and was removed from the model2. The linear regression model indicates that there is a moderate positive correlation between the obesity rate and the “No Activity” response (slope = 1.3, Adj. R-squared = 0.592). 

The Relationship Between Physical Activity and Income
H0 – The percentage of respondents that responded “No Activity” has no relationship with income brackets.
H1 – The percentage of respondents that responded “No Activity” does have a relationship with income brackets.

Prior to conducting a linear regression, the assumptions were tested1. We focused on data from the year 2019. We selected one of the Income categories, Income less than $15,000, to perform a linear regression analysis to see if states with higher respondents in this category experienced a higher percentage of people not exercising. The linear regression model indicates a moderate relationship exists between physical activity and income bracket (slope = 1.2, Adj. R-squared = 0.473). 

Conclusion
Based on the results, we can conclude some socioeconomic factors are related to obesity rates in the United States. Specifically, income bracket was found to be correlated to the percentage of adults aged 18 and over with obesity. Furthermore, it was found that Asians have lower percentages of adults with obesity. Finally, we found that lack of exercise can be related to respondents having lower income which was also found to contribute to higher obesity rates. 






