# An Analysis of Kickstarter Campaigns
Analysis on Kickstarter data to reveal trends
![Outcomes Based on Launch Date 630](https://user-images.githubusercontent.com/88383836/131024177-270c3a19-51ce-4e77-a75f-fcaf2b65378b.png)
![Ratings per Category Outcomes Chart 631](https://user-images.githubusercontent.com/88383836/131024207-dac64120-7b62-4f3b-a617-d81e1ffeafa6.png)

# Kickstarter Challenge Analysis

## Overview of Project 
This project provides data and thorough analysis of trends that affect the outcome of theater campaigns. 

### Purpose
Louise wants to know how different theater campaigns fared in relation to their launch dates and their funding goals. The purpose of this analysis is to provide Louise with data to help for future theater campaigns.

## Analysis and Challenges 

### Analysis of Outcomes Based on Launch Date
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/88383836/131701354-29152bf5-8982-4258-aead-c0fd7c8cdca3.png) (A1)

![Theater outcomes based on launch date table](https://user-images.githubusercontent.com/88383836/131717713-922a28e4-ea5d-4d4e-bf5b-e4b0e99f7570.PNG) (A2)

To begin this analysis, I opened the Kickstarter data worksheet, and created a column named Years. The formula used to generate the data for the “Years” column is YEAR(). Inside the argument for this formula is the data from the “Data Created Conversion” column (S Column) (Ex. YEAR(S2)). This gives our analysis the ability to show the start year for each campaign. 

Next step I developed a Pivot Table (A2) to filter the data to produce outcomes based on launch date. The table was created by placing the “parent category” and “years” into filters, placing the “date created conversion” into rows, and placing the “outcomes” into values and Legend. In the columns label section of the table “successful”, “failed”, and “canceled” must be selected. The table now has all the necessary data to create a Pivot Chart. The line graph will provide the best visualization for this data set since there are multiple outcomes being evaluated. The product is the chart A1 and properly displays the outcomes based on launch monthly launch date.


### Analysis of Outcomes Based on Goals 
![Outcomes Based on Goal](https://user-images.githubusercontent.com/88383836/131701374-906d26a2-b796-499a-ac68-7db7b731c56d.png) (B1) 

![Outcomes based on goals chart](https://user-images.githubusercontent.com/88383836/131718716-9df439f9-1862-4c9e-b209-d9d5f8c94d0e.PNG) (B2) 

To begin this analysis, I created a table that consists of the following data Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, and Percentage Canceled of the subcategory “plays”. To produce the values within the Number Successful, Number Failed, Number Canceled columns I used the formula COUNTIFS(). Inside the argument I placed all the criteria needed from the Kickstarter data set to display the corresponding data into each column (Ex. =COUNTIFS(Kickstarter!$D:$D,">1000",Kickstarter!$F:$F,"successful",Kickstarter!$R:$R,"plays")). The example argument shows all the criteria that is evaluated in the formula. The formula was then manipulated to produce the values based on the goal criteria (row) and which outcome type (column).  

From the data provided in the Number Successful, Number Failed, Number Canceled columns I generated the total sum from all categories using SUM() and placed that in the Total Projects column. Subsequently I used the results from each individual outcome column divided by the Total Projects to create the Percentage Successful, Percentage Failed, and Percentage Canceled calculations. These were the steps used to create the B2 table. 

The final step was to produce the line graph to show the Outcomes Based on Goal. I selected my data set then went to the “Insert” tab and in the charts section I selected line graph. I then adjusted the data in the graph to only show the percentage outcomes column (y-axis) to the corresponding goals row (x-axis). The product is the B1 chart and properly displays the outcomes based on goal. 

### Challenge Difficulties Encountered 
Filtering the dataset proved to be the one challenging task in the theater outcomes based on launch date analysis. The A2 table required some additional adjustments to the Rows Labels column in order to only show the months and not the year dates. When you initially place the “date created conversion” into the rows section you have two additional subcategory values that populate which are “quarter” and “year”. Removing those values from the row section then creates a list of months into the data table. 
Another challenging task was creating the initial =COUNTIFS() formula. Attempting to tackle this function the same as a normal =IF() formula created multiple errors for my initial attempt. After finding the solution, I realized the problem I ran into was including an additional comma with added criteria similar to the IF() formula.  

## Results
The theater outcomes based by launch date data in chart A1 shows that most of the theater campaigns are launched between April through August with at least 113 campaigns or more. The months that exhibit the highest number of successful campaigns are in May and June. This analysis shows the months of May and June are the best months to launch a campaign based on the number of successful campaigns to the total number of campaigns in the month. 
The plays outcomes based on goals data in chart B1 shows that the highest percentage of successful plays have a goal of $4,999 or less. The B2 chart shows a further break down that no play with a goal higher the $4,999 dollars and more than 100 total projects has a success percentage higher than 55%. The overall analysis for outcomes based on goals shows that most successful campaigns all have a goal of less than $4,999 and overall failure rate tends to increase proportionally the higher the goal amount. 
Combining the findings of the following analyses the optimal theater campaign is launched in May or June with a goal of $4,999 or less. Additional data and criteria that would prove useful to the purpose of this analysis is to find which months yield the most amount of money pledged for the theater category per month. Establishing this metric would show further analysis into the best time to seek funding for campaigns in order to get a visual on the ability to raise the success rate of campaigns in months that are low. 
