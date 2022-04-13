---
layout: default
title: Resources
nav_order: 25
---
## Resources
### Sample data
The data for this workshop is a recoded subset of the _Labour Force Survey, 2020_ from Statistics Canada. The original monthly Public Use Microdata Files (PUMFs) are available from <https://hdl.handle.net/11272.1/AB2/GGXMM2> under the terms of the [Statistics Canada Open License](https://www.statcan.gc.ca/eng/reference/licence).

The recoded subset consists of the January, April, July, and October 2020 PUMFs combined into one CSV file. The number of observations (rows) is the same as in the source data (360,554), but to make it easier to work with:
- the number of variables was reduced from 60 to 23
- variable names were replaced with human readable labels
- numerical codes were replaced with human readable values

The modifications are documented in an _R Markdown_ script ([LFS_microdata_transform.Rmd](data/LFS_microdata_transform.Rmd)) and can be applied to other Labour Force Survey PUMFs. 

### Books

- Cairo, Alberto. _The truthful art: data, charts, and maps for communication._ New Riders, 2016. UBC Library link (ebook available): <http://resolve.library.ubc.ca/cgi-bin/catsearch?bid=10289859>

- Cairo, Alberto. _How charts lie : getting smarter about visual information._ New York, NY : W. W. Norton & Company, Inc., 2019. UBC Library link: <http://resolve.library.ubc.ca/cgi-bin/catsearch?bid=10081648>

- Few, Stephen. _Show me the numbers: designing tables and graphs to enlighten._ Burlingame, Calif.: Analytics Press, 2012. UBC Library link: <http://resolve.library.ubc.ca/cgi-bin/catsearch?bid=6167222>

- Few, Stephen. _Information dashboard design: the effective visual communication of data._ Cambridge, MA: O'Reilly, 2006. UBC Library link: <http://resolve.library.ubc.ca/cgi-bin/catsearch?bid=5955120>
