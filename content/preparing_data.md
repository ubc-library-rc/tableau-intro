---
layout: default
title: Preparing your data
nav_order: 5
parent: Workshop content
---
# Preparing your data
This workshop emphasizes the visualization but in many cases your data will need to be manipulated, reformatted, and re-packaged _before_ you feed it to a visualization tool. Tableau (and other visualization tools) have some features to help clean messy data, but here are some general things to consider when preparing your data.

## Each measure in one column
If you're working with tabular data (e.g. Excel, csv), format it so that each measure appears in one column only. A table like this...

|  | march | april | may | june | july |
| --- | :---: | :---: | :---: | :---: | :---: |
| kittens_adopted | 0 | 0 | 1 | 0 | 2 |
| meals_ordered | 8 | 11 | 17 | 13 | 23 |

...will be harder to work with and will have fewer visualization options in Tableau than a table like this with the same information:

| month | kittens_adopted | meals_ordered |
| --- | :---: | :---: |
| march | 0 | 8 |
| april | 0 | 11 |
| may | 1 | 17 |
| june | 0 | 13 |
| july | 2 | 23 |
 

## Remove non-data content
Excel worksheets often begin with titles and other information, with the actual data table starting below. Titles and empty lines added to a spreadsheet for formatting reasons may interfere with visualization software's ability to read the contents. Removing extra lines and content is usually a good idea. 

## Know your dataset
It's important to know a few things about your data before importing it. How many records are there? What are the variable labels? Knowing this will help you confirm that Tableau imported the data correctly.

The sample dataset contains four months of data from the Statistics Canada Labour Force Survey (Jan, Apr, Jul, and Oct 2020). This data is freely available from UBC Library's [Abacus data repository](https://hdl.handle.net/11272.1/AB2/GGXMM2). To make it easier to work with in Tableau the original variable names and values were replaced with descriptive labels (see the [Resources](../resources.html) page for recoding details). The dataset contains 360,554 observations of 23 variables: each observation represents an individual response to the Labour Force Survey.

### Variables in the sample data

- Actual hours worked/wk at main job
- Age group
- Census metropolitan area
- Class of worker (main job)
- Duration of unemployment
- Flows into unemployment
- Highest educational attainment
- Job permanency (employees only)
- Labour force status
- Occupation at main job
- Province
- Reason for leaving job
- Reason for part time work
- Record number
- Sex
- Single or multiple jobholder
- Statistical Weight
- Student status
- Survey month
- Survey year
- Type of work (main job)
- Usual hourly wages (employees only)
- Usual hours worked/wk at main job

