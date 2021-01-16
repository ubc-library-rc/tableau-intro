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
During data import Tableau guesses whether each variable in the dataset represents a _Dimension_ or a _Measure._

- **Dimension.** A categorical or ordinal variable, often used to subdivide or filter the data (e.g. _Labour Force Status_ or _Province_). Dimensions appear at the top of the variable list, above the horizontal line.
- **Measure.** An interval or ratio variable, often used in calculations (e.g. _Statistical weight_ or _Usual Hourly Wages_). Measures are at the bottom of the variable list, below the horizontal line.

Categorical variables whose values are numerical codes are sometimes misinterpreted by Tableau. In this dataset _Sex_ is a categorical variable with values of either "1" (Male) or "2" (Female). It should be a Dimension but Tableau interprets it as a Measure because the categories are encoded as numbers (1 or 2). To fix this you may drag the _Sex_ variable from its current position below the horizontal line and drop it above the line with the other Dimensions. (Another method is to right-click the _Sex_ variable and choose _Convert to Dimension_.)

It is important for variables to be identified correctly, as Dimensions and Measures have different properties and are handled differently by the software.
{: .note}

## Tableau interface tips
A good way to get used to the Tableau interface is to experiment and see what happens. Here are some tips as you get started.

- **Right-click menus.** Many options are available by right-clicking in the Tableau interface. Explore the right-click menus for dimensions and measures (you can also right-click graph elements to hide, group, filter, and format them).
- **Undo**. If you take a wrong turn you can always undo your actions using the back arrow in the menu bar (above the sheet) or _Ctrl+Z_ (_Cmd+Z_ on a Mac)
- **Show Me.** The _Show Me_ button in the top right corner suggests graph types that may work with the dimensions and measures you have added to the sheet.
- **Duplicate.** Right-click your sheet tab (bottom of the screen) and select  _Duplicate_ to create a copy that you can play with while preserving the first one. This can be useful as you build graphs, allowing you to experiment but return quickly to an earlier version if things don't turn out.
