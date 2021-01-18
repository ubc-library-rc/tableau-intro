## Intro to data visualization with Tableau
### UBC Library Research Commons
Jeremy Buhler, <jeremy.buhler@ubc.ca>
Sarah Parker, <sarah.parker@ubc.ca>

---
## Pre-workshop setup
```note
This workshop includes hands-on practice with Tableau software. To participate fully please do the following **before the workshop**
```
1. _Tableau Public_ or _Tableau Desktop_
2. [Labour Force Survey, 2020 sample dataset](https://drive.google.com/uc?export=download&id=1ke_9HZ9qoOLOPbWC5XhW3cw-70ba9Rua) 
3. [Tableau Public account](https://public.tableau.com/) (optional)

---


## Learning objectives

1. Recognize the characteristics of an effective visualization
2. Format data for visualization
3. Create a simple visualization using Tableau 

---

## Tableau Public 

```note
This workshop uses _Tableau Public_ software to introduce data visualization concepts because it is freely available and accessible to beginners. 

This is not an endorsement of Tableau: there are many options for data visualization and other software may be better in other contexts. While suitable as a teaching tool, _Tableau Public_ imposes limitations that users should be aware of:
```
- Visualizations cannot be saved locally
- Dataset limit of 1M records
- Cannot connect databases

_Tableau Desktop_ is available in the Digital Scholarship Lab (<https://remotelabs.ubc.ca>)
{: .small}

---
```note
Before beginning the workshop, we'd like to acknowledge the indigenous lands where we are located.    
```
<iframe src="https://native-land.ca/api/embed/embed.html?maps=territories&position=49.268264,-123.157480" style="width:100%; height:300px; border:none;"></iframe>

[native-land.ca](https://native-land.ca/) 
{: .small}
---
## Participating online
```note
Active participation enlivens the session with other voices and perspectives. We encourage you to engage with instructors and with each other. Microphones are muted by default to improve audio quality and recording is disabled to preserve participant privacy. The Zoom toolbar provides several ways to be part of the conversation.
```
<img src="images/zoom_toolbar.png" alt="Zoom toolbar" width="510"/>

![Reactions menu](images/reactions.png)

---

```note
Use the _Chat_ window to comment or ask a question at any time. Instructors will do their best to respond, sometimes waiting for a break in the lesson to do so.
The _Chat_ window is a good place to report problems with your audio connection. Instructors may also use it to share links to material mentioned in the session.
```
## Writing on the screen

![Menu with Annotate option](images/open_annotate_toolbar.png)

![The annotation toolbar](images/annotate_toolbar.png)

Drawings and text you add to the screen will be visible to everyone in the session or breakout room.
{: .small}
---
## Outline 

| 0:10 | [Visualization basics](introduction.html)
| 0:25 | [Preparing your data](preparing_data.html)
| 0:30 | [Introducing the Tableau interface](tableau-interface.html)   
| _0:45_ | _Break_
| 0:50 | [Creating graphs](creating-graphs.html)
| 1:20 | [Saving your work](saving.html)

---
```note
In this workshop we begin with a dataset in CSV format containing 360,554 rows of data from Statistics Canada about labour and employment in Canada for selected months in 2020. By the end you will be able to create simple, clear graphs from the data like the ones below..
```

<img src="example1.png" alt="Tableau graph example #1" />
---
<img src="example2.png" alt="Tableau graph example #2" />
---
<img src="example3.png" alt="Tableau graph example #3" />

---
"Data visualization is the graphical display of abstract information for two purposes: sense-making (also called data analysis) and communication."  

   -_Stephen Few, [What is Data Visualization](https://www.perceptualedge.com/blog/?p=2636)_


```note
This workshop emphasizes the role data visualization plays in the two activities identified above. Visualization makes it easier to explore and understand what's going on in our data, fulfilling the **sense-making** purpose. It can also improve the **communication** of our findings by drawing attention to the patterns, relationships, and stories we choose to highlight.

Data visualizations are often attractive, but it isn't primarily their visual appeal that makes them work. A chart or graph that communicates effectively taps into the processes of perception and cognition. To create and recognize good visualizations it will help to understand a few concepts.
```
---
## Preattentive processing
```note
The eye and brain's ability to process certain visual properties almost instantly, without conscious effort. 
```
---

<img src="images/preattentive_attributes.png" />
_Source: Stephen Few, "Tapping the Power of Visual Perception" <http://www.perceptualedge.com/articles/ie/visual_perception.pdf>_

Good graphs take advantage of this perceptual ability to make information almost immediately apparent with little cost to the viewer. This figure shows the preattentive visual attributes that are especially useful when visualizing data.
In the figure above it is easy to spot the differences: some of them pop out almost instantly, with no need to concentrate or look closely. When creating visualizations we can take advantage of these preattentive attributes to encode information, often using more than one attribute in the same graph.

It is also clear from the figure that preattentive attributes have different powers. Some stand out more than others, and some can be used not only to distinguish _between_ things (like shape), but to show differences in _amount_ (like length). All of this may sound obvious, but that is precisely the point: by using visual cues that are obvious to most viewers we make it easier for them to see - and hopefully understand - the messages we want our visualizations to convey.
```
---

Remove unneceassary content to keep the viewer focused
```note
When using visualizations to communicate it is good practice to remove elements that are not required to convey your message. Additional labels, lines, and decimal points compete for the viewers attention and can distract from what matters most in a visual display. It is important to provide enough detail for the viewer to orient themselves and understand the graph, but removing unecessary components provides more breathing room and helps the viewer focus on the content.
In the version on the right, removing redundant text and changing text shading, placement, and size draws attention to the main content: unemployment rates. Unecessary lines are also removed. The light horizontal lines are sometimes helpful when scanning across a graph and were kept, but even these might not be necessary in all cases. 

In your own work review each visual component and ask whether it helps keep the viewer focused. The "less is more" rule often leads to clearer visualizations.
```

<div style="float:left; width:45%; padding:20px 3%">
<img src="images/cluttered.png" style="border-style: none" />
</div>
<div style="float:right; width:45%; padding:20px 3%">
<img src="images/clean.png" class="image" />
</div>

---

## Using color
Use colors intentionally to **encode information**
 
```note
- **Colorblindness**. Avoid encoding important information in colors that may be difficult for some viewers to perceive. See [5 tips on designing colorblind-friendly visualizations](https://www.tableau.com/about/blog/2016/4/examining-data-viz-rules-dont-use-red-green-together-53463).
- **Visual continuity**. A dashboard or report may contain several visualizations based on the same data. If the same category appears in several graphs use the same color scheme to depict it throughout. This will make it easier for viewers see the relationship among your graphs.
- **Meaningful encoding**. The colors on the left below do not encode any new information and add distracting visual complexity to the graph. By not "spending" colors unnecessarily designers can use them to greater effect (e.g. to call attention to a particular value).
```

<div style="float:left; width:50%; padding:20px 3%">
<img src="images/multicolor.png" />
</div>
<div style="float:left; width:50%; padding:20px 3%">
<img src="images/singlecolor.png" />
</div>

---

## Some guiding principles 
1. **Choose clarity over variety**  
2. **Reduce burden on the reader**  
3. **Present data with integrity**  

```note
Visual variety can be appealing, but ensure that it also serves the communicative and sense-making purposes of your visualizations.
The twin graphs above illustrate this point. Avoid distractions and unecessary information and help the reader focus on the content.
We increase the credibility and integrity of our work by citing data sources and avoiding intentionally misleading displays. (For more about this see Alberto Cairo's book [_How charts lie : getting smarter about visual information._](http://resolve.library.ubc.ca/cgi-bin/catsearch?bid=10081648))
```
---
## Preparing your data
```note
This workshop emphasizes the visualization but in many cases your data will need to be manipulated, reformatted, and re-packaged _before_ you feed it to a visualization tool. Tableau (and other visualization tools) have some features to help clean messy data, but here are some general things to consider when preparing your data.
```
---

## Each measure in one column
```note
If you're working with tabular data (e.g. Excel, csv), format it so that each measure appears in one column only. A table like this will be harder to work with and will have fewer visualization options than this table with the same information:
```

|  | march | april | may | june | july |
| --- | :---: | :---: | :---: | :---: | :---: |
| kittens_adopted | 0 | 0 | 1 | 0 | 2 |
| meals_ordered | 8 | 11 | 17 | 13 | 23 |


| month | kittens_adopted | meals_ordered |
| --- | :---: | :---: |
| march | 0 | 8 |
| april | 0 | 11 |
| may | 1 | 17 |
| june | 0 | 13 |
| july | 2 | 23 |
 
---

## Remove non-data content
```note
Excel worksheets often begin with titles and other information, with the actual data starting below. Subtitles and empty lines within the data table may further interfere with visualization software's ability to interpret the contents. Removing extra lines and non-data content is a good general practice, though Tableau can often identify the data elements correctly during import.
```

## Know your dataset
- How is it formatted?
- How many records are there?
- What are the variable labels?
- Is there a user guide or data dictionary?
```note
It's important to know a few things about your data before importing it. How many records are there? What are the variable labels? Knowing this will help you confirm that Tableau imported the data correctly.

The sample dataset for this workshop contains four months of data from the Statistics Canada Labour Force Survey (Jan, Apr, Jul, and Oct 2020). This data and supporting documentation is freely available from UBC Library's [Abacus data repository](https://hdl.handle.net/11272.1/AB2/GGXMM2) under the terms of the [Statistics Canada Open License](https://www.statcan.gc.ca/eng/reference/licence). Statistics Canada's [Guide to the Labour Force Survey](https://www150.statcan.gc.ca/n1/pub/71-543-g/71-543-g2020001-eng.htm) provides information about the survey purpose, methodology, and terms.
```
4 months of data from the Statistics Canada Labour Force Survey (Jan, Apr, Jul, and Oct 2020)

---
## Variables in sample dataset

```note
To make it easier to work with in Tableau the sample dataset is a modified subset of the original data. Some variables were excluded and variable names and values were replaced with descriptive labels (see the [Resources](resources.html) page for details about the changes). The dataset contains 360,554 observations of 23 variables:
```

---

## Checking your work
```note
If you know your data it's easier to spot when something's not quite right, suggesting a setting or calculation is incorrect. The sample dataset is the same one used to generate Statistics Canada table [14-10-0017-02](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1410001702), _Labour force characteristics by province, monthly, unadjusted for seasonality_. As you learn Tableau you may use this table to check your work.
```

<div style="padding:20px 3% 0px 3%">
<h3>Statistics Canada table</h3>
<img src="images/statcan_table.png" />
</div>
<div style="width:50%; padding:30px 3%">
<h3>Graph produced from sample dataset</h3>
<img src="images/clean_highlight.png" />
</div>

Statistics Canada table [14-10-0017-02](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1410001702), _Labour force characteristics by province, monthly, unadjusted for seasonality_.
