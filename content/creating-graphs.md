---
layout: default
title: Creating graphs
nav_order: 8
parent: Workshop content
---
# Creating graphs

## Bar graph: unemployment rate
The data in the sample dataset is the same used to produce Statistics Canada table 14-10-0017-02, [Labour force characteristics by province, monthly, unadjusted for seasonality](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1410001702). We can use Tableau to reproduce the figures in that table and present them visually.

### Steps (to be refined before workshop)
1. Go to _Worksheet -> New Worksheet_
1. Drag _Labour Force Status_ to _Rows_
1. Drag _Statistical weight_ to _Columns_
1. In the _Marks_ card, click _Label_ then put a check next to _Show mark labels_

We now have a bar graph showing the number of people in each Labour Force Status category. But this number is too high because our data includes four months. To see the number of unemployed people in a single month, limit the display to January survey responses in one of two ways:

- Right-click _Survey month_ and select _Show Filter_, **or**
- Drag _Survey month_ onto the _Filters_ card

By default the graph show us the SUM of the _Statistical Weight_ measure, representing the entire population of Canada aged 15 and over. To show percentages instead of sums:

- Right-click the green _Statistical Weight_ pill in the _Columns_ shelf and select _Quick Table Calculation -> Percent of Total_

The labels now show the percentage of the population in January that fell into each Labour Force Status. The unemployed row shows 3.77%, but this is not actually correct since the unemployment rate calculations should exclude people "Not in labour force". 

Take a moment to explore and see if you can solve this problem. What is the actual unemployment rate for January 2020?

<details>
<summary>Click here for solutions</summary>
<br>
- **Solution 1:** on the bar graph, right click the label "Not in labour force" and select _Exclude_
- **Solution 2:** drag the _Labour Force Survey_ dimension from the left menu to the _Filters_ card and exclude "Not in labour force"
</details>

The January unemployment rate was 5.84%.

## Map: unemployment rate by month
