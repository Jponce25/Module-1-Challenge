# Kickstarting with Excel

## Overview of Project

We have a dataset of past Kickstarter campaigns with a total of 4115 rows, we want to analyze how similar Luise´s campaigns performed in relation to the launch date and the goal objective, for this analisys we have to look the Goal column refers to the amount of money each campaign needs, while the launch date column refers to the start date of the campaign. We want to know how the different campaigns fared in relation to their launch dates and their founding goals. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

First we must determine the launch month of each campaign, for this we create a column called Years, to calculate the value of that column we use the `YEAR()` function.

Then a pivot table is built that filters the successful, failed and canceled campaigns per month. To obtain the filter by month it is necessary to eliminate the filters by year and semester.

![](https://github.com/Jponce25/kickstarter-analysis/blob/d17dfe4eaebafb5b6607eb76df45564b17bf6887/images/AnalysisLaunchDate1.png)

For this exercise it is required to filter the category "theater", at first glance it can be seen that May and June are the months where more than half of the projects were satisfactory even there are the months with most projects. It is also observed that in general the month with the fewest projects was December.

![](https://github.com/Jponce25/kickstarter-analysis/blob/d17dfe4eaebafb5b6607eb76df45564b17bf6887/images/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

For the second analysis based on goals, we first define the ranges in which we will group the campaigns based on their goal ammount. Then we count using the `COUNTIFS ()` function the number of successful, failed and canceled projects, we also filter the subcategory by "plays". To make the data easier to read, we calculate the percentages of successful, failed, or canceled projects.

![](https://github.com/Jponce25/kickstarter-analysis/blob/d17dfe4eaebafb5b6607eb76df45564b17bf6887/images/AnalysisGoals1.png)

The projects with the highest percentage of success are those with goals less than 4,999, and a percentage of 100% of failure for goals between 45000 to 49999. It can also be identified that for the subcategory "plays" there are no canceled projects. 

![](https://github.com/Jponce25/kickstarter-analysis/blob/d17dfe4eaebafb5b6607eb76df45564b17bf6887/images/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

For the Outcomes Based on Goals analysis, there could be difficulties when filtering the data to obtain the number of successful, failed and canceled projects due to the fact that several filters are used to obtain the final number. It is necessary to take special care in the ranges and in the use of the symbols > and < in the function.

## Results

- What are two conclusions you can draw about the Theater Outcomes based on Launch Date?

It can be concluded that in this sample the months from May to July the successful projects add up to more than 80 for each month, with the highest peak in the month of May.

Additionally, it can be concluded that the number of canceled projects does not vary much during the months of the year, in the same way, failed projects behave very stable throughout the year with small peaks in May and October.

- What can you conclude about the Outcomes based on Goals?

Generally there is a higher percentage of success for projects with goals less than 1,000, and a higher percentage of failure for goals greater than 45,000. However, there is a range between 35,000 and 44,999 where the percentage of successful projects increases again.

- What are some limitations of this dataset?

One of the main limitations of the database is that we do not consider the difference in the totals for each month, that is, there are months where there are fewer projects and therefore the number of successful, failed and canceled projects will naturally be less.

- What are some other possible tables and/or graphs that we could create?

In the Analysis of Outcomes Based on Launch Date we could calculate the percentages of successful, failed and canceled projects to have a more visual analysis of the data, finally we could use the data from the column "Date Ended Conversion" to calculate the lifetime of each project to be included in our analysis, since having only the start date does not give us an accurate result.

While, in the Analysis of Outcomes Based on Goals we could generate an analysis of quantiles  to better determine the ranges trying to ensure that they do not have a Right skew.
