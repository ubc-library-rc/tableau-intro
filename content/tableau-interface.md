---
layout: default
title: Introducing the Tableau interface
nav_order: 7
parent: Workshop content
---
# Introducing the Tableau interface

## Connecting to the data
Open _Tableau Public_ or _Tableau Desktop_ and select _Text file_ from the _Connect_ menu. On the next screen click _Update Now_ to preview the data. If it imports correctly click _Sheet1_ near the bottom of the screen to create a graph or table. 

<video controls="controls" width="100%" name="import data" src="images/import_data.mp4">
</video>

## The Tableau Sheet
Like Excel, Tableau can have multiple _Sheets_ represented by tabs at the bottom of the screen. Each sheet is a space to create a graph. Here's a new sheet with the sample dataset.

<video controls="controls" width="100%" name="the Tableau sheet" src="images/sheet.mp4">
</video>

- dataset variables are listed on the left
- variables can be dragged onto the _Rows_ and _Columns_ shelves to add them to the display
- use the _Show me_ button to select a graph type
- adjust color, size, and labels using the _Marks_ cards

## Dimensions and measures
During data import Tableau guesses whether each variable in the dataset represents a "Dimension" or a "Measure."

- **Dimension.** A categorical or ordinal variable, often used to subdivide or filter the data (e.g. "Labour Force Status" or "Province"). Dimensions appear at the top of the variable list, above the horizontal line.
- **Measure.** An interval or ratio variable, often used in calculations (e.g. "Statistical weight" or "Usual Hourly Wages"). Measures are at the bottom of the variable list, below the horizontal line.

Dimensions appear at the top of the list of variables and measures are listed at the bottom, below the horizontal line. Categorical variables whose values are numerical codes are sometimes misinterpreted by Tableau. In this dataset "Sex" is a categorical variable with values of either "1" (Male) or "2" (Female). It should be a Dimension, but Tableau lists it as a Measure. To fix this you may drag it from the current position below the horizontal line and drop it above the line with the other Dimension. (Another method is to right-click and choose _Convert to Dimension_.)

It is important for variables to be identified correctly, as Dimensions and Measures have different properties and are handled differently by the software.
{: .note}

## Tableau interface tips
A good way to get used to the Tableau interface is to experiment and see what happens. Here are some tips as you get started.

- Many options are available from **right-click** menus. Right-click a variable in the left menu and explore.
- If you take a wrong turn, **Undo** your actions using the top menu or CTRL+Z (CMD+Z on a Mac)
- The _Show Me_ button suggests graph types that may work with the dimensions and measures you have added to the sheet.
- Right-click your sheet tab (bottom of the screen) and _Duplicate_ to create a copy that you can play with while preserving the previous state.

