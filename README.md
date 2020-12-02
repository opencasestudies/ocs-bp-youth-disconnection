<!-- README.md is generated from README.Rmd. Please edit that file -->

Open Case Studies
=================

<!-- badges: start -->

[![render-README](https://github.com/opencasestudies/ocs-bp-youth-disconnection/workflows/render-README/badge.svg)](https://github.com/opencasestudies/ocs-bp-youth-disconnection/actions)
[![render-index](https://github.com/opencasestudies/ocs-bp-youth-disconnection/workflows/render-index/badge.svg)](https://github.com/opencasestudies/ocs-bp-youth-disconnection/actions)
<!-- badges: end -->

### Important links

-   HTML:
    <a href="https://www.opencasestudies.org/ocs-bp-youth-disconnection" class="uri">https://www.opencasestudies.org/ocs-bp-youth-disconnection</a>
-   GitHub:
    <a href="https://github.com/opencasestudies/ocs-bp-youth-disconnection" class="uri">https://github.com/opencasestudies/ocs-bp-youth-disconnection</a>
-   Bloomberg American Health Initiative:
    <a href="https://americanhealth.jhu.edu/open-case-studies" class="uri">https://americanhealth.jhu.edu/open-case-studies</a>

### Disclaimer

The purpose of the [Open Case Studies](https://www.opencasestudies.org)
project is **to demonstrate the use of various data science methods,
tools, and software in the context of messy, real-world data**. A given
case study does not cover all aspects of the research process, is not
claiming to be the most appropriate way to analyze a given dataset, and
should not be used in the context of making policy decisions without
external consultation from scientific experts.

### License

This case study is part of the [Open Case
Studies](https://www.opencasestudies.org) project. This work is licensed
under the Creative Commons Attribution-NonCommercial 3.0 ([CC BY-NC
3.0](https://creativecommons.org/licenses/by-nc/3.0/us/)) United States
License.

### Citation

To cite this case study:

Wright, Carrie and Ontiveros, Michael and Jager, Leah and Taub, Margaret
and Hicks, Stephanie C. (2020).
<https://github.com/opencasestudies/ocs-youth-disconnection-case-study>.
Disparities in Youth Disconnection.

### Acknowledgements

We would like to acknowledge [Tamar
Mendelson](https://www.jhsph.edu/faculty/directory/profile/1770/tamar-mendelson)
for assisting in framing the major direction of the case study.

We would also like to acknowledge the [Bloomberg American Health
Initiative](https://americanhealth.jhu.edu/) for funding this work.

### Title

Disparities in Youth Disconnection

### Motivation

According to this
[report](https://ssrc-static.s3.amazonaws.com/moa/Making%20the%20Connection.pdf)
youth disconnection (defined as “young people between the ages of **16
and 24** who are **neither working nor in school**” according to the
[Measure of America](https://www.ssrc.org/programs/view/moa/) (a
nonpartisan project) although generally showing decreasing trends for
the past 7 years, shows **racial and ethnic disparities**, where some
groups are showing increased rates of disconnection.

Thus in this case study we aim to look further at youth disconnection
rates among gender and racial and ethnic subgroups to identify groups
that may be particularly vulnerable.

### Motivating questions

1.  How have youth disconnection rates in American youth changed since
    2008?  
2.  In particular, how has this changed for different gender and ethnic
    groups? Are any groups particularly disconnected?

### Data

In this case study we will be using data related to youth disconnection
from the two following reports from the [Measure of
America](https://www.ssrc.org/programs/view/moa/) project:

> Measure of America is a nonpartisan project of the nonprofit [Social
> Science Research Council](https://www.ssrc.org/) founded in 2007 to
> create easy-to-use yet methodologically sound tools for understanding
> well-being and opportunity in America. Through reports, interactive
> apps, and custom-built dashboards, Measure of America works with
> partners to breathe life into numbers, using data to identify areas of
> highest need, pinpoint levers for change, and track progress over
> time.

1.  Lewis, Kristen. [Making the Connection: Transportation and Youth
    Disconnection](https://ssrc-static.s3.amazonaws.com/moa/Making%20the%20Connection.pdf).
    New York: Measure of America, Social Science Research Council, 2019.
    (Data up to 2017)
2.  : Lewis, Kristen. [A Decade Undone: Youth Disconnection in the Age
    of
    Coronavirus](https://ssrc-static.s3.amazonaws.com/moa/ADecadeUndone.pdf).
    New York: Measure of America, Social Science Research Council, 2020.
    (Data up to 2018)

These reports use data from the [American Community Survey
(ASC)](https://www.census.gov/programs-surveys/acs).

#### Learning Objectives

The skills, methods, and concepts that students will be familiar with by
the end of this case study are:

<u>**Data Science Learning Objectives:**</u>

1.  Importing text from PDF files using images and the `magick`
    package  
2.  Apply action verbs in `dplyr` for data wrangling  
3.  How to reshape data by pivoting between “long” and “wide” formats
    and separating columns into additional columns (`tidyr`)  
4.  How to fill in data based on previous values (`tidyr`)
5.  How to create data visualizations with `ggplot2` that are in a
    similar style to an existing image  
6.  How to add images to plots using `cowplot`
7.  How to create effective bar plots to for multiple comparisons,
    including adding gaps between bars in bar plots, adding figure
    legends to the plot area, and adding comparison lines (`ggplot2`)

<u>**Statistical Learning Objectives:**</u>

1.  Implementation of the Mann-Kendall trend test  
2.  Interpretation of the Mann-Kendall trend test
3.  Difference between linear regression and Mann-Kendall trend test

#### Data import

Data is imported from several tables within two PDF documents by taking
screenshots of the tables of interest and using the `magick` package to
import the text from the screenshots.

#### Data wrangling

This case study particularly focuses on renaming variables, modifying
variables, creating new variables, and modifying the shape of the data
using functions such as as: `pivot_longer()`, and `pivot_wider()`, as
well as modifying specific variables using the `mutate()` and `across()`
functions of the `dplyr` package.  
This case study also covers combining data with `bind_rows()` and
`add_rows()` functions of the `dplyr` package.

We also cover removing NA values with the `drop_na()` function of the
`tidyr` package, separating one column into multiple columns using the
`separate()` function of the `tidyr` package, filling in `NA` values
based on previous values using the `fill()` and replacing `NA` values
with the `replace_na()` function, both of the `tidyr` package, as well
as arranging levels of factors using the `forcats` package.

Finally, this case study also covers many of the `stringr` functions to
manipulate character strings, including `str_extract()`,
`str_to_title()`, `str_replace()`, `str_remove()`.

#### Data Visualization

We include an example of creating a plot to match the style of a plot in
an existing report. We also demonstrate how to make effective bar plots,
by demonstrating details such as creating gaps between groups, taking
advantage of these gaps to move the legend to within the plot area, and
to use horizontal lines to allow for additional comparisons among
groups. We also demonstrate how to add images to plots and combine plots
using the `patchwork` package.

### Analysis

The analysis in this case study covers some basics about probability and
hypothesis testing, as well as the Mann-Kendall trend test and the
difference between this test and simple linear regression. In this
analysis we use the Mann-Kendall to test if there has been a trend
within the disconnection rates of particular groups of youths over time.

### Other notes and resources

<a href="https://rstudio.com/products/rstudio/features/" target="_blank">RStudio</a>  
<a href="https://github.com/rstudio/cheatsheets/raw/master/rstudio-ide.pdf" target="_blank">Cheatsheet on RStuido IDE</a>  
<a href="https://rstudio.com/resources/cheatsheets/" target="_blank">Other RStudio cheatsheets</a>  
<a href="https://www.tidyverse.org/" target="_blank">Tidyverse</a>

[Response bias](https://en.wikipedia.org/wiki/Response_bias)  
[Cross-Sectional
data](https://en.wikipedia.org/wiki/Cross-sectional_data?oldformat=true)
[Population](https://en.wikipedia.org/wiki/Population?oldformat=true)
[Sample](https://en.wikipedia.org/wiki/Sampling_(statistics)?oldformat=true)
<a href="https://en.wikipedia.org/wiki/Sampling_(statistics)?oldformat=true" target="_blank">Sampling methods</a>
[Inference](https://www.britannica.com/science/inference-statistics)

[American Community Survey
(ASC)](https://www.census.gov/programs-surveys/acs)

See [here](https://en.wikipedia.org/wiki/American_Community_Survey) for
more detailed information about the survey  
[Measure of America](https://www.ssrc.org/programs/view/moa/)  
[Social Science Research Council](https://www.ssrc.org/)

<a href="https://cran.r-project.org/web/packages/magrittr/vignettes/magrittr.html" target="_blank">Piping in R</a>  
[Writing functions](https://r4ds.had.co.nz/functions.html)  
Also see
<a href="https://www.opencasestudies.org/ocs-bp-vaping-case-study/" target="_blank">this case study</a>
for more information on writing functions.  
<a href="https://rstudio.com/resources/cheatsheets/" target="_blank">String manipulation cheatsheet</a>  
<a href="https://en.wikipedia.org/wiki/Wide_and_narrow_data" target="_blank">Table formats</a>

[Regression](https://lindeloev.github.io/tests-as-linear/)  
[simple linear
regression](https://en.wikipedia.org/wiki/Simple_linear_regression)  
[monotonic
association](https://www.statisticshowto.com/monotonic-relationship/)  
[Kendall rank correlation
coefficient](https://en.wikipedia.org/wiki/Kendall_rank_correlation_coefficient?oldformat=true)  
[Null hypothesis](https://en.wikipedia.org/wiki/Null_hypothesis)  
[Alternative
hypothesis](https://en.wikipedia.org/wiki/Alternative_hypothesis)  
[Probability](https://en.wikipedia.org/wiki/Probability)  
[one-sided and two-sided
hypotheses](https://en.wikipedia.org/wiki/One-_and_two-tailed_tests)  
[Nonparametric](https://en.wikipedia.org/wiki/Nonparametric_statistics)
[Parametric](https://en.wikipedia.org/wiki/Parametric_statistics)
[significance
threshold](https://en.wikipedia.org/wiki/Statistical_significance)  
[Z score](https://en.wikipedia.org/wiki/Standard_score)  
[Z score
table](https://socratic.org/questions/5986a3e1b72cff6fd48a5408)  
[Z score to p-value
calculator](https://www.socscistatistics.com/pvalues/normaldistribution.aspx)

<a href="http://ggplot2.tidyverse.org" target="_blank"><code>ggplot2</code> package</a>  
Please see [this case
study](https://www.opencasestudies.org/ocs-bp-co2-emissions/) for more
details on using `ggplot2`  
<a href="http://vita.had.co.nz/papers/layered-grammar.html" target="_blank">grammar of graphics</a>  
<a href="https://ggplot2.tidyverse.org/reference/ggtheme.html" target="_blank"><code>ggplot2</code> themes</a>  
<a href="http://directlabels.r-forge.r-project.org/docs/index.html" target="_blank"><code>directlabels</code> package methods</a>  
[Hmong people](https://en.wikipedia.org/wiki/Hmong_people)  
[Intersections](https://www.vox.com/the-highlight/2019/5/20/18542843/intersectionality-conservatism-law-race-gender-discrimination)

[Motivating article for this case study about youth
disconnection/opportunity
youth](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6243446/)

To learn more about importing and wrangling PDFs using the `pdftools`
package see this [case
study](https://www.opencasestudies.org/ocs-bp-rural-and-urban-obesity/).

To learn more about what you can do with the `magick` package see this
[vingette](https://cran.r-project.org/web/packages/magick/vignettes/intro.html).

To learn more about the **Mann-Kendall trend test** see
[here](https://www.statisticshowto.com/mann-kendall-trend-test/) and
[here](https://www.statisticshowto.com/wp-content/uploads/2016/08/Mann-Kendall-Analysis-1.pdf).

To learn more about hypothesis testing, see this [case
study](https://www.opencasestudies.org/ocs-bp-rural-and-urban-obesity/).

<u>**Packages used in this case study:** </u>

<table>
<colgroup>
<col style="width: 43%" />
<col style="width: 56%" />
</colgroup>
<thead>
<tr class="header">
<th>Package</th>
<th>Use in this case study</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="https://github.com/jennybc/here_here" target="_blank">here</a></td>
<td>to easily load and save data</td>
</tr>
<tr class="even">
<td><a href="https://readr.tidyverse.org/">pdftools</a></td>
<td>to import PDF documents</td>
</tr>
<tr class="odd">
<td><a href="https://cran.r-project.org/web/packages/magick/vignettes/intro.html#Kernel_convolution">magick</a></td>
<td>for importing images and extracting text from images</td>
</tr>
<tr class="even">
<td><a href="https://cran.r-project.org/web/packages/tesseract/vignettes/intro.html">tesseract</a></td>
<td>for extracting text from images with <code>magick</code></td>
</tr>
<tr class="odd">
<td><a href="https://yihui.org/knitr/">knitr</a></td>
<td>for showing images in reports</td>
</tr>
<tr class="even">
<td><a href="https://dplyr.tidyverse.org/" target="_blank">dplyr</a></td>
<td>to filter, subset, join, add rows to, and modify the data</td>
</tr>
<tr class="odd">
<td><a href="https://stringr.tidyverse.org/" target="_blank">stringr</a></td>
<td>to manipulate strings</td>
</tr>
<tr class="even">
<td><a href="https://magrittr.tidyverse.org/" target="_blank">magrittr</a></td>
<td>to pipe sequential commands</td>
</tr>
<tr class="odd">
<td><a href="https://tidyr.tidyverse.org/" target="_blank">tidyr</a></td>
<td>to change the shape or format of tibbles to wide and long, to drop rows with <code>NA</code> values, to separate a column into additional columns, and to fill out values based on previous values</td>
</tr>
<tr class="even">
<td><a href="https://tibble.tidyverse.org/" target="_blank">tibble</a></td>
<td>to create tibbles</td>
</tr>
<tr class="odd">
<td><a href="https://ggplot2.tidyverse.org/" target="_blank">ggplot2</a></td>
<td>to create plots</td>
</tr>
<tr class="even">
<td><a href="http://directlabels.r-forge.r-project.org/docs/index.html" target="_blank">directlabels</a></td>
<td>to add labels directly to lines in plots</td>
</tr>
<tr class="odd">
<td><a href="https://cran.r-project.org/web/packages/cowplot/vignettes/introduction.html" target="_blank">cowplot</a></td>
<td>to add images to plots</td>
</tr>
<tr class="even">
<td><a href="https://forcats.tidyverse.org/" target="_blank">forcats</a></td>
<td>to reorder factor for plot</td>
</tr>
<tr class="odd">
<td><a href="https://cran.r-project.org/web/packages/Kendall/Kendall.pdf">kendall</a></td>
<td>to implement the Mann-Kendall trend test in R</td>
</tr>
<tr class="even">
<td><a href="https://github.com/thomasp85/patchwork">patchwork</a></td>
<td>to combine plots</td>
</tr>
<tr class="odd">
<td><a href="https://cran.r-project.org/web/packages/DT/index.html">DT</a></td>
<td>Interactive tables</td>
</tr>
</tbody>
</table>

#### For instructors

Instructors can start at the Data Visualization or Data Analysis
sections. Instructors can also skip the *Subgroup plots* section if they
don’t wish to instruct students about making bar plots in depth.

#### Target audience

This case study is appropriate for those new to R programming and new to
statistics. It is also appropriate for more advanced R users who are new
to the Tidyverse. This particular case study may require some
fundamental knowledge of statistics.

#### Suggested homework

-   For the Asian and Latinx subgroup bar plots made across year, modify
    these plots to consider gender differences (instead of across time).
-   Taking the plot you made above, modify the plot to facet across
    years.
-   Find another table in one of the reports to import using the
    `magick` package (for example perhaps the data about different
    states over time in the 2019 report called [Making the
    Connection](https://ssrc-static.s3.amazonaws.com/moa/Making%20the%20Connection.pdf)).
    Look for differences between groups by plotting the data and
    evaluating with the Mann-Kendall test.
