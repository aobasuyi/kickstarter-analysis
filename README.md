# Kickstarting with Excel
Performing analysis on Kickstarter data to uncover trends

## Overview of Project: 
This project uses Excel to organise, sort and analyze a dataset consisting of over 4,000 crowdfunding projects to uncover hidden trends. The results of the analysis will provide insights in how to plan a fundraising campaign to fund a play estimated to cost about $10,000. The analysis will help to determine whether there are specific factors that make theatrical production fundraising campaigns successful.

### Purpose: 
To determine how theatrical production campaigns fared in relation to their launch dates and their funding goals. This will provide insights that will help in setting goals to mirror successful campaigns in the theatrical productions’ category.

## Analysis and Challenges: 
Data preparation steps taken prior to starting this analysis include sorting, filtering and formatting the Kickstarter dataset to convert data into readable and easy to use formats that will generate more insights [Kickstarter_analysis](https://github.com/aobasuyi/kickstarter-analysis/edit/main/README.md)

### Analysis of Outcomes Based on Launch Date
The first deliverable of this project was to determine if there were certain times of the year when theatrical production campaigns tend to be more successful. Steps taken include
- First, create a pivot table from the KickStarter worksheet and place the pivot table in a new sheet labelled "Theater Outcomes by Launch Date."
- Next, filter the pivot table based on "Parent Category" and "Years."
- Filter the column labels to show only "successful," "failed," and "canceled."
- Filter the "Parent Category" to show only the data for "theater."
- Sort the campaign outcomes in descending order so "successful" is first.
- Finally, create a line chart from the pivot table to visualize the relationship between outcomes and launch month.   *![Outcome Based on Launch Date](path/to/image_name.png)*.

### Analysis of Outcomes Based on Goals
The second deliverable was to visualize the percentage of successful, failed, and canceled plays based on the funding goal amount. 
- First create a new sheet from the KickStarter worksheet and label it "Outcomes Based on Goals." 
- In the new sheet, create the following eight columns to hold the data; “Goal”, “Number Successful”, “Number Failed”, “Number Canceled”, “Total Projects”, “Percentage Successful”. “Percentage Failed”, “Percentage Canceled”.
- In the “Goal” column, create the following dollar-amount ranges so projects can be grouped based on their goal amount
- Use COUNTIFS() functions to populate the "Number Successful," "Number Failed," and "Number Canceled" columns by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges created in Step 3, and on the "Subcategory" column using "plays" as the criteria.
- Calculate the sum of "Total Projects" column with the number of successful, failed, and canceled projects for each row.
- Calculate the percentage of successful, failed, and canceled projects for each row.
- Finally, create a line chart titled "Outcomes Based on Goal" to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on the y-axis. <br /> *[Outcome Based on Goals](path/to/image_name.png)*

### Challenges and Difficulties Encountered
Minor challenges encountered during the project consisted mostly of “errors” when using the COUNTIFS function. The errors were easily fixed by checking that the “criteria” and the “goal amount ranges” in the COUNTIFS formula were entered correctly in the formula bar. 

## Results

**Conclusions about “Outcomes based on Launch Date”:** <br />
The month that launched the most successful theatrical production campaigns was May. However, January, March, September, November and December all had roughly the same number of failed campaigns launched. As well, January has the most canceled campaigns <br />

**Conclusions about the “Outcomes based on Goals”:**<br />
Successful Kickstarter campaigns with fundraising goal amount range of less than $1000 was the most successful and the next successful goal amount range is “1000 to 4999”. Kickstarter campaigns with goal amount range “45000 to 49999 has 100 percent chance of failure <br />

**Some limitations of this dataset:**<br />
The calculation of the "Total Projects" in the “Outcomes Based on Goals” worksheet resulted in a discrepancies between the summed total of 1043 ( in this worksheet) and 1066 (in the Kickstarter worksheet). Using the goal amount range “>50000” instead of “>=50,000” resulted in exclusion of 4 projects in this range, and not including “live” in the outcomes criteria resulted in exclusion of 19 projects. <br />

**Other possible tables and/or graphs that could be created:**
- To consider creating a table/chart comparing the goals and pledges for failed and successful theatrical production campaigns to be able to determine whether there are any trends between the goals and pledges in successful or failed campaigns.
- To create a box plot of identity outliers and consider using filter to eliminate extreme data point not representative of the data we want for the analysis to be able to generate better insights to plan a successful campaign.
