BIOC461
================
Mik Black & Paul Gardner<BR>Department of Biochemistry
11 April 2024

<!-- The following will produce markdown output that will be viewble on GitHub: -->
<!-- rmarkdown::render('bioc461-lecture1.Rmd', output_format="github_document") -->

## Today’s lecture

1.  Good practice for project organisation

2.  Data organisation (and visualisation) in practice

3.  Statistical testing

4.  P-hacking

## Assessment

10% assessment in class - <font color="red">**THIS COUNTS TOWARDS YOUR
COURSE GRADE**</font>

- Select a small dataset produced in your lab.

- Compare how well the dataset confirms to the practices we discuss
  today.

- How could this dataset be analysed and visualised?

- Prepare a brief (~5mins) presentation for next week.

Further details are on Blackboard.

# Part 1: Project Organisation

## Organising your projects

Based on the papers:

- **Good enough practices in scientific computing**: <BR> Wilson G,
  Bryan J, Cranston K, Kitzes J, Nederbragt L, Teal TK. PLoS Comput
  Biol. 2017 Jun 22;13(6):e1005510.<BR> doi:
  [10.1371/journal.pcbi.1005510](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510)

- **Ten Simple Rules for Reproducible Computational Research** <BR>
  Sandve GK, Nekrutenko A, Taylor J, Hovig E. PLoS Comput Biol. 2013
  Oct;9(10):e1003285. <BR> doi:
  [10.1371/journal.pcbi.1003285](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003285)

## Not just for computational research…

- Yes, both those papers are focused on “computational research”.
- BUT, most research we do contains the same basic elements:
  - experiments
  - data
  - analysis methods
  - results
  - collaboration
- We need to keep all of these components ORGANIZED.

## Overview

Sections (we’ll cover the <span style="color:blue">blue</span> stuff):

- <p style="color:blue">
  Data Management
  </p>

- <p style="color:blue">
  Software
  </p>

- <p style="color:blue">
  Collaboration
  </p>

- <p style="color:blue">
  Project Organization
  </p>

- Keeping Track of Changes

- Manuscripts

- Ten Rules for Reproducible Computational Research

## Reproducibility + Efficiency + Continuity

- For you:
  - recreate results (with ease)
  - reuse code and workflows
  - develop more efficient work habits
- For everyone:
  - ensure reproducibility (and reduce burden)
  - establish workflows
  - enable collaboration
  - build upon existing work

# Quiz time…

## Not really, just some thinking

Spend two minutes thinking about the answers to the following questions:

1.  If you were abducted by aliens in the next 30 seconds, how easy
    would it be for someone else to carry on your research? (after we
    finished mourning your loss, of course).

2.  How much time would you need to spend getting your work to the point
    where another human being *could* carry on with your project? What
    would this involve?

3.  If your laptop/desktop was unexpectedly destroyed by evil
    anti-research forces, what impact would this have on your project?
    (it’s ok, we’ll buy you a shiny new one from our “anti-anti-research
    forces” insurance fund).

# Let’s (briefly) discuss your answers…

## Data management

1.  Save the raw data.
    - preserve raw data - never edit
    - if needed, computationally create modified versions of raw data
      (e.g., data cleaning).
2.  Ensure raw data are backed up in more than one location
    - e.g., Biochem server + ITS High Capacity Storage, Biochem Server +
      Google Drive etc (<b>See Murray Cadzow’s slides on BB</b>)
    - <b>Data sensitivity</b> issues with cloud-based storage providers
3.  Create the data you wish to see in the world
    - non-proprietary (preferably text-based) formats
    - informative variable and file names
    - make it the data set you wish you had received…

## Data management

<ol start=4>
<li>

Create analysis-friendly data

- each column is a variable
- each row is an observation
- tidy data aren’t just for R…

<li>

Record all the steps used to process data.

- if possible, use scripts to capture (and automate) every step of data
  processing and cleaning

</ol>
<!-- ## Data management -->
<!-- <ol start=6> -->
<!-- <li> Anticipate the need to use multiple tables, and use a unique identifier for every record. -->
<!--   - e.g., multiple CSV files linked by a common sample ID -->
<!--   - combine data programmatically  -->
<!-- <li> Submit data to a reputable DOI-issuing repository so that others can access and cite it. -->
<!--  - Zenodo: https://zenodo.org -->
<!--  - Dryad: https://datadryad.org -->
<!--  - FigShare: https://figshare.com -->
<!-- <p style="color:red">**But first: CAN you share your data?**</p> -->
<!-- </ol> -->

## Software (scripts, code etc)

1.  Place a brief explanatory comment at the start of every program.

    - explain what the code does, and how to use it.
    - if appropriate, include examples of usage.

2.  Decompose programs into functions.

    - breaks tasks into small (well-documented) chunks
    - digestible =\> understandable

3.  Be ruthless about eliminating duplication.

    - use functions
    - don’t copy and paste code chunks (write a function)

## Software (scripts, code etc)

<ol start=4>
<li>

Always search for well-maintained software libraries that do what you
need.

- don’t reinvent the wheel…

<li>

Test libraries before relying on them.

<li>

Give functions and variables meaningful names.

- use tab completion with informative names

<li>

Make dependencies and requirements explicit.

- can be as simple as adding a `requirements.txt` file.

</ol>
<!-- ## Software (scripts, code etc) -->
<!-- <ol start=8>  -->
<!-- <li> Do not comment and uncomment sections of code to control a program's behaviour. -->
<!--   - error prone -->
<!--   - use `if/else` statements instead -->
<!-- <li> Provide a simple example or test data set. -->
<!--   - also good for you to help with testing -->
<!--   - and great for running workshops! -->
<!-- <li> Submit code to a reputable DOI-issuing repository. -->
<!-- </ol> -->

# Even if you are not working<BR>as part of a team…<BR><BR><BR>

# Even if you are not working<BR> as part of a team…<BR><BR>…YOU ARE!!

## Collaboration

- Your project is very likely to be part of a larger research programme,
  and the work you are doing has the potential to contribute to other
  projects in the future.

- You are also collaborating with yourself: ask “present you” about your
  good friend “future you”.

## Collaboration

1.  Create an overview of your project.

    - `README.txt` or `README.md` in the top-level directory

2.  Create a shared “to-do” list for the project.

    - even if it is just for you…

3.  Decide on communication strategies.

# Quiz Time…

## Whose project folder looks like this?

<!-- <img src="Pics/junk.jpg"> -->
<center>
<img src="Pics/cluttereddesktop.jpg">
</center>

[Wikimedia Commons File: Exampleofdigitalhoarding
cluttereddesktop001.jpg](https://commons.wikimedia.org/wiki/File:Exampleofdigitalhoarding_cluttereddesktop001.jpg)

## Find a partner…

- Spend two minutes discussing how you organise your projects.
- Think about:
  - directory structure
  - documentation
  - where different types of files are kept

# This stuff is critical…

## Project Organisation

1.  Put each project in its own directory, which is named after the
    project.

2.  Put text documents associated with the project in the `doc`
    directory.

3.  Put raw data and metadata in a data directory and files generated
    during cleanup and analysis in a results directory.

    - critical to separate input data from derived data
    - don’t be afraid to use subdirectories to impose additional order

## Project Organisation

<ol start=4>
<li>

Put project source code in the src directory.

- Interpreted: R, Python
- Compiled: C++, Fortran, Java
- Shell scripts, SQL snippets

<li>

Put external scripts or compiled programs in the bin directory.

- may not be relevant for some projects (e.g., if not using compiled
  code)
- why external scripts here? So you can make a distinction for edited vs
  non-edited files: binary files and external scripts are not directly
  edited.

<li>

Name all files to reflect their content or function.

</ol>

## Example: project layout

    |-- CITATION
    |-- README
    |-- LICENSE
    |-- requirements.txt
    |-- data
    |    |-- birds_count_table.csv
    |-- doc
    |    |-- notebook.md
    |    |-- manuscript.md
    |    |-- changelog.txt
    |-- results
    |    |-- summarized_results.csv
    |-- src
    |    |-- sightings_analysis.py
    |    |-- runall.py

<font size="2"> Wilson G, Bryan J, Cranston K, Kitzes J, Nederbragt L,
Teal TK. PLoS Comput Biol. 2017 Jun 22;13(6):e1005510.<BR>
[10.1371/journal.pcbi.1005510](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510)
</font>

## Tools and habits

- Tools **enable** reproducible research
  - there are lots of them
  - they are not hard to learn
- Good habits **ensure** reproducible research
  - there are many good habits: each one will improve your work in some
    way
  - these **are** hard to learn (actually, that is not true - it is just
    hard to **unlearn** your bad habits)
- Getting into the habit of using these “good practice tools” as a
  central part of your workflow is critical
- It takes commitment, but it will be hugely beneficial

# Part 2: Data Organisation

## Data organization

- A spreadsheet application (e.g., Microsoft Excel) is often used to
  “organize” data.
  - Excel has the ability to make raw data look very pretty.
  - Statistics applications (e.g., SPSS, R, SAS, Prism) often have
    trouble reading pretty data.
- Try to keep it simple:
  - Samples in rows, variables in columns
  - No blank cells or rows (unless data are missing)

## Example data

We’re going to use some really old data as an example:

<center>
<img src="PNG/toothgrowth-paper-title.png" width="500">
</center>

<BR>

We’ll start by looking at a fairly typical (Excel-based) approach to
data organisation and analysis.

## “Tooth Growth” data set

- Length of odontoblasts (cells responsible for tooth growth) in 60
  guinea pigs
- Guinea pigs exposed to different doses of Vitamin C, via two different
  mechanisms.
- Variables in the data set:
  - len = Tooth length (unit unknown…)
  - supp = Vitamin C Supplement: ascorbic acid (VC) or Orange Juice (OJ)
  - dose = Dose in milligrams/day
- Let’s look at how that data “might” get recorded in a typical study.

## Tooth Growth data

Often the data would be recorded in Excel, using a format somewhat like
this:

<center>
<img src="PNG/toothgrowth-data.png" width="700">
</center>

## Tooth Growth data + summary

Excel makes it easy to add summary dat such as:

- Mean ($\bar x$): `=AVERAGE()`
- Standard Deviation ($s$): `=STDEV()`
- Observations per group ($N$): `=COUNT()`
- Standard error of the mean ($SEM$):
  <font color='black'>`=`$\frac{s}{\sqrt N}$</font>

<center>
<img src="PNG/toothgrowth-data-summary.png" width="700">
</center>

## Summary data

<center>
<img src="PNG/toothgrowth-summary.png" width="300">
</center>

<BR>

Often want to plot this summary data

- bar plot per group
- add error bars

## And Excel lets you!

<center>
<img src="PNG/toothgrowth-excel-chart.png" width="500">
</center>

<BR>

<center>
<img src="PNG/so-pretty.png" width="400">
</center>

## And what’s more…

<font color='black'> <b>YOU CAN MAKE THE PLOT RIGHT IN THE EXCEL
SHEET!</b>

</font>

<BR>
<center>
<img src="PNG/toothgrowth-excel-sheet.png" width="600">
</center>

# Let’s pause…

## Principles of project/data organisation

<br><br><br><br><br><br>
<center>
<font size=12 color='black'> <b>How many did we just break?</b> </font>
</center>

## Principles of project/data organisation

How many did we just break?

- create analysis-friendly data
- non-proprietary format
- preserve raw data - never edit
- record all the steps used to process data
- separate input data from derived data

## How can we fix this?

- Raw data:
  - analysis-friendly data: re-format data
  - non-proprietary format: save as `.csv` file (comma-separated value:
    still opens in Excel, but is text-based, so easy to open elsewhere)
  - preserve raw data: separate the data from the analysis
- Analysis
  - record all the steps: use a script-based language (e.g., R or
    Python)
  - separate input data from derived data: use a script to read raw data
    and produce outputs

## Data format

Each column is a variable, each row is an observation.

<center>
<img src="PNG/toothgrowth-excel-long.png" width="250">
</center>

<BR> Save as a `.csv` file, and store in a separate `Data` folder.

## Analysis

- R (or Python) can be used to process, visualise and analyse the data.
- Let’s have a look at a typical R workflow for this.

``` r
# Read the data
tooth_growth = read.csv('Data/tooth-growth-long-format.csv')

# Look at the first few rows
head(tooth_growth)
```

    ##    len supp dose
    ## 1  4.2   VC  0.5
    ## 2 11.5   VC  0.5
    ## 3  7.3   VC  0.5
    ## 4  5.8   VC  0.5
    ## 5  6.4   VC  0.5
    ## 6 10.0   VC  0.5

## Summarize data

The `dplyr` package for R provides a nice way to generate data
summaries.

``` r
# Load dplyr package
library(dplyr)

# Generate data summary object (tg_summary)
tg_summary = tooth_growth %>% 
  group_by(supp, dose) %>%  
  summarize( MeanLength = mean(len), 
             SD = sd(len), 
             N = n(), 
             SEM = SD / sqrt(N) )
```

## Summarize data

What does this produce?

``` r
# Show the tg_summary object
tg_summary
```

    ## # A tibble: 6 × 6
    ## # Groups:   supp [2]
    ##   supp   dose MeanLength    SD     N   SEM
    ##   <chr> <dbl>      <dbl> <dbl> <int> <dbl>
    ## 1 OJ      0.5      13.2   4.46    10 1.41 
    ## 2 OJ      1        22.7   3.91    10 1.24 
    ## 3 OJ      2        26.1   2.66    10 0.840
    ## 4 VC      0.5       7.98  2.75    10 0.869
    ## 5 VC      1        16.8   2.52    10 0.795
    ## 6 VC      2        26.1   4.80    10 1.52

## R can even make it look pretty(ish)

``` r
tg_summary %>% knitr::kable(., digits=2) 
```

| supp | dose | MeanLength |   SD |   N |  SEM |
|:-----|-----:|-----------:|-----:|----:|-----:|
| OJ   |  0.5 |      13.23 | 4.46 |  10 | 1.41 |
| OJ   |  1.0 |      22.70 | 3.91 |  10 | 1.24 |
| OJ   |  2.0 |      26.06 | 2.66 |  10 | 0.84 |
| VC   |  0.5 |       7.98 | 2.75 |  10 | 0.87 |
| VC   |  1.0 |      16.77 | 2.52 |  10 | 0.80 |
| VC   |  2.0 |      26.14 | 4.80 |  10 | 1.52 |

## How to plot?

- The `ggplot2` package for R has become (by far) the most popular tool
  for producing publication quality figures in R.
- It takes a little bit of effort (and Googling) to learn the syntax,
  but it is an <em>extremely</em> powerful and flexible tool.
- Some handy resources:
  - R for Data Science (2nd edition): <https://r4ds.hadley.nz/>
  - R Graphics Cookbook: <https://r-graphics.org/>
- Let’s have a look at generating a bar plot of our summary data in R.

## Barplot: the code

R code for barplot with `ggplot2`

``` r
# Load the ggplot2 package
library(ggplot2)
# Create a basic bar plot
ggplot(tg_summary, aes(x=as.factor(dose), y=MeanLength, fill=supp)) + 
  geom_bar(stat="identity", position="dodge")
```

Breaking down the code:

- `ggplot` takes the data object (`tg_summary`), converts `dose` to a
  factor, plots `dose` on the x-axis and `MeanLength` on the y-axis, and
  uses `supp` to define colours.
- `geom_bar` generates the barplot, using the values from `tg_sumamry`
  (`identity`) and puts the bars next to each other (`dodge`).

## Barplot: the output

``` r
ggplot(tg_summary, aes(x=as.factor(dose), y=MeanLength, fill=supp)) + 
  geom_bar(stat="identity", position="dodge")
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

## Barplot: without `as.factor`

``` r
ggplot(tg_summary, aes(x=dose, y=MeanLength, fill=supp)) + 
  geom_bar(stat="identity", position="dodge")
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

## Barplot: without `dodge`

``` r
ggplot(tg_summary, aes(x=as.factor(dose), y=MeanLength, fill=supp)) + 
  geom_bar(stat="identity") 
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

## Making it prettier

``` r
ggplot(tg_summary, aes(x=as.factor(dose), y=MeanLength, fill=supp)) + 
  geom_bar(stat="identity", position="dodge") + 
  labs(title="Tooth length per dose", x="Dose (mg)", 
       y = "Mean length", fill='Supplement')
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

## And… error bars

``` r
ggplot(tg_summary, aes(x=as.factor(dose), y=MeanLength, fill=supp)) + 
  geom_bar(stat="identity", position="dodge") + 
  labs(title="Tooth length per dose", x="Dose (mg)", 
       y = "Mean length", fill='Supplement') +
  geom_errorbar(aes(ymin=MeanLength-SEM, ymax=MeanLength+SEM),
                    position=position_dodge(0.9), width=0.2)
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

## Error bars: upper bar only (change plotting order)

``` r
ggplot(tg_summary, aes(x=as.factor(dose), y=MeanLength, fill=supp)) + 
  labs(title="Tooth length per dose", x="Dose (mg)", 
       y = "Mean length", fill='Supplement') +
  geom_errorbar(aes(ymin=MeanLength-SEM, ymax=MeanLength+SEM),
                    position=position_dodge(0.9), width=0.2) +
  geom_bar(stat="identity", position="dodge") 
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

## Aside: why are we plotting the SEM?

- The sample standard deviation, $s$, measures the spread of the sample
  observations around the sample mean
- When we test for differences between the groups, we are testing to see
  if the <em>means</em> are the same.
- To do this we use the standard error of the mean (SEM, or SE):

<center>
$SEM = \frac{s}{\sqrt N}$
</center>

<BR>

- It measures our certainty in our estimate of the population mean, (we
  are assuming that the sample mean, $\bar x$ provides an estimate of
  the true population mean, $\mu$).
- As we increase the sample size, $N$, the SEM gets smaller, because
  with more data, we have a better estimate of $\mu$.

## Aside: a more informative plot?

``` r
ggplot(tooth_growth, aes(x=as.factor(dose), y=len, fill=supp)) + 
  labs(title="Tooth length per dose", x="Dose (mg)", 
       y = "Length", fill='Supplement') +
  geom_boxplot(outlier.alpha = 0) + 
  geom_jitter(position = position_jitterdodge(jitter.width=0.12), alpha=0.7)
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

## Datasaurus: visualise your data!

<center>
<img src="PNG/datasaurus.png" width="600">
</center>

<https://www.autodesk.com/research/publications/same-stats-different-graphs?s=03>

# Part 3 - Statistical Testing

## Two sample test

Let’s start with a smaller data set: just the OJ vs VC data for a dose
of 1mg.

``` r
# Read in a reduced data set
tg_1mg = read.csv('Data/tooth-growth-long-format-dose-1mg.csv')
# Show the first few rows
head(tg_1mg)
```

    ##    len supp
    ## 1 16.5   VC
    ## 2 16.5   VC
    ## 3 15.2   VC
    ## 4 17.3   VC
    ## 5 22.5   VC
    ## 6 17.3   VC

## Plot the data

``` r
ggplot(tg_1mg, aes(x=supp, y=len)) + 
  labs(title="Tooth length vs Supplement (1mg dose)", x="Supplement", y = "Length") +
  geom_boxplot(outlier.alpha = 0, width=0.3) + geom_jitter(width=0.12, alpha=0.7)
```

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-15-1.png)<!-- -->

## Hypothesis testing

- We’d like to formally test for a difference between the means of OJ
  and VC.
- Standard hypothesis testing setup:
  - H<sub>0</sub>: the population means are same
  - H<sub>A</sub>: the population means are different
- Assuming that the data are normally distributed, we can use a t-test
  for this:
  - $T = \frac{\bar x_1 - \bar x_2}{SE(\bar x_1 - \bar x_2)} = \frac{\bar x_1 - \bar x_2}{\sqrt {\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}\ \ \ \ $
    (SE for unequal variance across groups)
  - If H<sub>0</sub> is true (i.e., no difference between the means)
    then $T$ will follow a t-distribution, and we can use this to
    calculate a p-value.

## T-test

In R we can perform a t-test between OJ and VC mean lengths via:

``` r
t.test(len ~ supp, data = tg_1mg)
```

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  len by supp
    ## t = 4.0328, df = 15.358, p-value = 0.001038
    ## alternative hypothesis: true difference in means between group OJ and group VC is not equal to 0
    ## 95 percent confidence interval:
    ##  2.802148 9.057852
    ## sample estimates:
    ## mean in group OJ mean in group VC 
    ##            22.70            16.77

The p-value is 0.00104, which suggests a difference between the means of
this size is unlikely to occur by chance if H<sub>0</sub> is true.

## What if data aren’t normal?

- If the data aren’t normally distributed (e.g., skewed, bimodal etc),
  we can use <em>non-parametric</em> methods.
- Note, it may be hard to determine normality when your sample sizes are
  small.
- The non-parametric analog to the t-test is the Wilcoxon Rank-Sum Test.
  - tests for a difference between the two groups by ranking the
    combined data, and then testing to see if the ranks are distributed
    differently (enough) across the groups.
  - in R this is implemented by the `wilcox.test()` function.

## Rank-based data

Stripcharts of the length distributions for each group:

<center>
<img src="PNG/toothgrowth-length-stripchart.png" width="500">
</center>

Converted to ranks, the data look like this:

<center>
<img src="PNG/toothgrowth-rank-stripchart.png" width="500">
</center>

Wilcoxon test ignores the length distribution, and tests for rank-based
differences.

## Wilcoxon test

``` r
wilcox.test(len ~ supp, data = tg_1mg)
```

    ## Warning in wilcox.test.default(x = DATA[[1L]], y = DATA[[2L]], ...): cannot compute exact p-value with
    ## ties

    ## 
    ##  Wilcoxon rank sum test with continuity correction
    ## 
    ## data:  len by supp
    ## W = 88.5, p-value = 0.00403
    ## alternative hypothesis: true location shift is not equal to 0

P-value (0.004) again suggests there is a significant length difference
between the groups.

NB: the warning just means that an approximation is being used to
calculate the p-value, as there are ties present in the data (same
value).

## Testing more hypotheses

Let’s return to the full tooth length data set.

![](bioc461-lecture1_files/figure-gfm/unnamed-chunk-19-1.png)<!-- -->

- If we wanted to test for VC vs OJ at each dose level, we’d need to
  perform three hypothesis tests.

- Note that there are better statistical ways to perform this analysis,
  but we’ll keep it simple.

## Three hypothesis tests

``` r
# Create empty vector to fill with p-values
pval = c()

# Dose = 0.5
pval[1] = t.test(len ~ supp, data = tooth_growth %>% filter(dose==0.5) )$p.value

# Dose = 1
pval[2] = t.test(len ~ supp, data = tooth_growth %>% filter(dose==1) )$p.value

# Dose = 2
pval[3] = t.test(len ~ supp, data = tooth_growth %>% filter(dose==2) )$p.value

# Show p-values
names(pval) = c("Dose_0.5mg", "Dose_1.0mg", "Dose_2.0mg")
pval
```

    ##  Dose_0.5mg  Dose_1.0mg  Dose_2.0mg 
    ## 0.006358607 0.001038376 0.963851589

## Multiple hypothesis testing

- Based on the three p-values, it looks like there is a difference in
  length at doses 0.5mg and 1.0mg, but not 2.0mg (amusing that p \< 0.05
  indicates significance).
  - By setting a significance at $\alpha$ = 0.05, we are specifying the
    Type I error rate for our tests - also known as the false positive
    rate.
  - For a test where H<sub>0</sub> is true, we will incorrectly detect a
    difference between the means 100$\alpha$% of the time (i.e., 5%).
  - The error probability applies to each test - so we have a 5% chance
    of error for each test that we perform.
- If we are performing a large number of tests (e.g., genome-wide
  testing of 1 million SNP loci), then we can expect to make a large
  number of errors (on average, 0.05 x 1,000,000 = 50,000) in a
  situation where H<sub>0</sub> is true for most tests.

## Multiple testing corrections

- To prevent large numbers of false positives when testing many
  hypotheses, we employ <b>multiple testing correction</b>. Two ways to
  think about it:

  - make the p-values BIGGER, and use the same threshold
  - make the threshold SMALLER, and use the same p-values

- In Genome-Wide Association Studies (GWAS), the latter approach is
  generally used: typical genome-wide significance is set at
  5x10<sup>-8</sup>.

  - Bonferroni Correction:
    $\alpha^{*} = \frac{\alpha}{\mathrm{number~of~tests}} = \frac{0.05}{1000000} = 5\times10^{-8}$
  - P-value \< 5x10<sup>-8</sup> is required for significance.
  - Alternatively, could multiply each p-value by 1,000,000 and use a
    threshold of 0.05 (first approach, above).

- This controls the Family-wise Error Rate (FWER) so that P(Type I
  error) \< 0.05 across <em>all tests being performed</em>.

## Types of error rate control

- - FWER: the <b>Holm</b> method is slightly more powerful than
    Bonferroni.
  - False Discovery Rate (FDR) control provides more liberal p-value
    adjustment (i.e., more power), but at the cost of a higher Type I
    error rate (i.e., more false positives).

|            |   RawP |    FDR |   Holm | Bonferroni |
|:-----------|-------:|-------:|-------:|-----------:|
| Dose_0.5mg | 0.0064 | 0.0095 | 0.0127 |     0.0191 |
| Dose_1.0mg | 0.0010 | 0.0031 | 0.0031 |     0.0031 |
| Dose_2.0mg | 0.9639 | 0.9639 | 0.9639 |     1.0000 |

## Multiple testing correction in R: `p.adjust`

``` r
# Bonferroni
p.adjust(pval, method="bonferroni")
```

    ##  Dose_0.5mg  Dose_1.0mg  Dose_2.0mg 
    ## 0.019075820 0.003115128 1.000000000

``` r
# Holm (default for p.adjust)
p.adjust(pval, method="holm")
```

    ##  Dose_0.5mg  Dose_1.0mg  Dose_2.0mg 
    ## 0.012717214 0.003115128 0.963851589

``` r
# FDR
p.adjust(pval, method="fdr")
```

    ##  Dose_0.5mg  Dose_1.0mg  Dose_2.0mg 
    ## 0.009537910 0.003115128 0.963851589

## Impact

- In this case, it hasn’t changed our conclusions (differences between
  OJ and VC for 0.5mg and 1.0mg, but not for 2.0mg)
- <b>BUT</b> when you’ve tested multiple hypotheses, and your “best”
  p-values are between 0.01 and 0.05, then performing multiple testing
  correction will likely make your results non-significant.
- <b>THIS IS A GOOD THING!</b>
  - it is telling you that you could have gotten these results by chance
  - either there is no difference, or your need to perform additional
    experimentation (i.e., increase the sample size) to be more certain.

# Part 4 - P-hacking

## P-hacking

<center>
<img src="PNG/20-sided-dice.png" width="400">
</center>

## What is P-hacking?

- Also called “data dredging”, is the misuse of data analysis methods to
  identify statistically significant results, which increases the risk
  of false positive findings.

- There are two principle causes of publication bias:

  1.  The “file drawer effect”: non-significant results are
      under-reported

  2.  And “P-hacking”: selective reporting of only significant results

  Wikipedia page: [Data
  dredging](https://en.wikipedia.org/wiki/Data_dredging)

## A demonstration

- Generate 2 randomly sampled datasets in R

``` r
      n<-20
      (x<-rnorm(n))
```

    ##  [1] -1.10046318  0.02529056 -0.04056675 -0.40604664 -0.36866740 -0.60687701  1.53673564  0.61337127
    ##  [9]  0.98121187 -0.34543891 -1.09747692  1.43288348 -0.07026218  0.68418713 -0.09599613  0.02601053
    ## [17] -0.83350737 -0.09255006 -0.33174189 -1.15277058

``` r
      (y<-rnorm(n))
```

    ##  [1]  1.02981998 -0.96175799 -0.22813434 -0.04979861 -1.38914557  0.27453250  0.66056829 -1.43888329
    ##  [9]  0.21182993 -0.26030028  0.56916976 -1.04937126  1.08157050  0.39207608 -1.61430792 -0.98693402
    ## [17]  0.55726636  0.71190768  1.04284361 -0.72556065

## A demonstration – test for a significant difference

``` r
t.test(x, y)
```

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  x and y
    ## t = 0.17542, df = 37.291, p-value = 0.8617
    ## alternative hypothesis: true difference in means is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.4904117  0.5834052
    ## sample estimates:
    ##   mean of x   mean of y 
    ## -0.06213373 -0.10863046

## A demonstration – another test for a significant difference

``` r
t.test(x, y, alternative = "less")
```

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  x and y
    ## t = 0.17542, df = 37.291, p-value = 0.5692
    ## alternative hypothesis: true difference in means is less than 0
    ## 95 percent confidence interval:
    ##       -Inf 0.4935776
    ## sample estimates:
    ##   mean of x   mean of y 
    ## -0.06213373 -0.10863046

## A demonstration – another test for a significant difference

``` r
t.test(x, y, alternative = "greater")
```

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  x and y
    ## t = 0.17542, df = 37.291, p-value = 0.4308
    ## alternative hypothesis: true difference in means is greater than 0
    ## 95 percent confidence interval:
    ##  -0.4005842        Inf
    ## sample estimates:
    ##   mean of x   mean of y 
    ## -0.06213373 -0.10863046

## A demonstration – another test for a significant difference

``` r
wilcox.test(x,y)
```

    ## 
    ##  Wilcoxon rank sum exact test
    ## 
    ## data:  x and y
    ## W = 195, p-value = 0.9042
    ## alternative hypothesis: true location shift is not equal to 0

## A demonstration – lots of other tests

- cor.test

- ks.test

- kruskal.test

- var.test

- anova

- chisq.test

- shapiro.test

## My unethical employer needs “significance”

- Keep resampling/adding data until you get the desired result:

``` r
 for (l in 1:100){
      y  <- rnorm(50)
      x  <- rnorm(50) 
      p <- t.test(x, y)$p.value
      if(p < 0.05){
           cat("Test [", l, "] is significant (p=", p, "). You can publish this one!\n")
      }
}
```

    ## Test [ 6 ] is significant (p= 0.005105923 ). You can publish this one!
    ## Test [ 23 ] is significant (p= 0.02846843 ). You can publish this one!
    ## Test [ 30 ] is significant (p= 0.01170927 ). You can publish this one!
    ## Test [ 43 ] is significant (p= 0.02037359 ). You can publish this one!
    ## Test [ 72 ] is significant (p= 0.04605469 ). You can publish this one!
    ## Test [ 87 ] is significant (p= 0.04739283 ). You can publish this one!
    ## Test [ 89 ] is significant (p= 0.0450149 ). You can publish this one!

## How can we know if this is a real problem?

- P-curves may tell us a lot:

<center>
<img src="PNG/p-curve.png" width="400">
</center>

- **A peculiar prevalence of p values just below .05**: <BR> Masicampo
  EJ, Lalande DR. Quarterly journal of experimental psychology. 2012
  Nov;65(11):2271-9. <BR> doi:
  [10.1080/17470218.2012.711335](https://doi.org/10.1080/17470218.2012.711335)

## Spurious correlations

- Website: <https://www.tylervigen.com/spurious-correlations>

<center>
<img src="PNG/spurious.png" width="700">
</center>

## Solutions?

## 

<center>
<img src="Pics/albatross.png" width="1000">
</center>
