---
title: "Exploring Statistics"
subtitle: ""
description: ""
excerpt: ""
date: 2022-09-01
author: "Aitor Gutierrez Valero"
image: ""
published: true
tags:
  - ["rstudio", "r", "Foundation"]
URL: "2022/09/01/Exploring-Statistics"
categories: ["Learning"]
---

# Foundational Concepts

------------------------------------------------------------------------

## Population, Sample, and Sample Size

A population is a defined set of individuals, and a sample is a randomly
selected sub-set of a population. For example: As of 2022, Spain has
[4.7M](https://www.ine.es/dyngs/INEbase/es/operacion.htm?c=Estadistica_C&cid=1254736176951&menu=ultiDatos&idp=1254735572981)
people. A sample of the Spanish population would be a random selection
of 1 - to - 4.69M people in Spain.

Sample size determines the accuracy of any data calculated from a
sample. This accuracy can be split into two concepts:

**Confidence Level -**

    Certainty that our sample represents the population

**Error Margin -**

    Certainty that our statistics reflect the population

To elaborate: We find that the average weight of all Spaniards is 70 kg
with an error margin of 10% and a confidence level of 95%. The error
margin means that the weight is actually somewhere between 63 and 77 kg,
and the confidence level means that we are 95% sure that the average is
between 63 and 77 kg.

Below is a table comparing the error margin and confidence level for
different sample sizes of a population of 1 million people.

<table>
<thead>
<tr class="header">
<th style="text-align: right;">Sample Size</th>
<th style="text-align: right;">Error Margin</th>
<th style="text-align: right;">Confidence Level</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: right;">31</td>
<td style="text-align: right;">15</td>
<td style="text-align: right;">90</td>
</tr>
<tr class="even">
<td style="text-align: right;">97</td>
<td style="text-align: right;">10</td>
<td style="text-align: right;">95</td>
</tr>
<tr class="odd">
<td style="text-align: right;">664</td>
<td style="text-align: right;">5</td>
<td style="text-align: right;">99</td>
</tr>
<tr class="even">
<td style="text-align: right;">16317</td>
<td style="text-align: right;">1</td>
<td style="text-align: right;">99</td>
</tr>
</tbody>
</table>

------------------------------------------------------------------------

## Statistics vs. Parameters

**Statistics -**

    The calculated values from a sample

**Parameters -**

    The true values from a population (Calculable if your sample is the population)

------------------------------------------------------------------------

## Variable Types used in Statistics (Types of data)

#### Qualitative (Categorical)

**Ordinal -**

    An ordered set of variables: Always, frequently, sometimes, etc.

**Nominal -**

    An unordered variable: Gender, Colour, Country, etc.

#### Quantitative

**Continuous -**

    Numerical: Infinite values like height and weight

**Discrete -**

    Numerical: Countable values like number of people or flowers

------------------------------------------------------------------------

## Three Types of Statistical Analysis

Statistics analysis is used to interpret, represent, and extrapolate
data and its various trends.

### 1. Bias

Defines how error influences the final results.

**Random Error -**

     Uncontrollable error in measurement that varies randomly
     For example: A cup's length is between the smallest increment on your ruler; you round up or down

**Systematic Error -**

    Error in measurement that skews values consistently
    For example: Scale consistently measures too high by 1 kg.

### 2. Descriptive Statistics

Provides an idea of the differences or similarities between data by
defining averages and spread.

Below is a data set of numbers for which we will calculate descriptive
statistics. First are the averages, next is the spread.

    -7, 1, 2, 2, 3, 4, 5, 5, 6, 22

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 39%" />
<col style="width: 29%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Type</th>
<th style="text-align: left;">Mean</th>
<th style="text-align: left;">Median</th>
<th style="text-align: left;">Mode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Description</td>
<td style="text-align: left;">Sum of all of the numbers divided by the
number of numbers</td>
<td style="text-align: left;">Value separating the upper and lower
halves</td>
<td style="text-align: left;">Most frequent value in a dataset</td>
</tr>
<tr class="even">
<td style="text-align: left;">Example</td>
<td style="text-align: left;">(-7 + 1 + 2 + … + 22)/10</td>
<td style="text-align: left;">Mean of 3 and 4</td>
<td style="text-align: left;">Bimodal</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Result</td>
<td style="text-align: left;">4.3</td>
<td style="text-align: left;">3.5</td>
<td style="text-align: left;">2 and 5</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 7%" />
<col style="width: 32%" />
<col style="width: 22%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Type</th>
<th style="text-align: left;">Range</th>
<th style="text-align: left;">Standard_Deviation</th>
<th style="text-align: left;">Interquartile_Range</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Description</td>
<td style="text-align: left;">Difference between the highest and lowest
numbers</td>
<td style="text-align: left;">Amount of dispersion from the mean</td>
<td style="text-align: left;">Difference between the 25th (Q1) and 75th
(Q3) percentiles</td>
</tr>
<tr class="even">
<td style="text-align: left;">Example</td>
<td style="text-align: left;">22 - (-7)</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Q1 = 2 Q3 = 5</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Result</td>
<td style="text-align: left;">29</td>
<td style="text-align: left;">6.84</td>
<td style="text-align: left;">3</td>
</tr>
</tbody>
</table>

### 3. Inferential Statistics

After exploring data using descriptive statistics, the relationships
between variables (eg. height vs. weight) and their consistency can be
determined using inferential statistics. To understand how these
relationships are tested, the null hypothesis and alternative hypothesis
are defined. After which, statistical tests are performed.

**Null Hypothesis**

    The expected idea based on current knowledge: Population 1 is equivalent to Population 2.

**Alternative Hypothesis**

    A new idea which could nullify the null hypothesis: Population 1 is different from Population 2

#### Statistical Tests

Every statistical test produces:

    A test statistic that indicates how closely the data match the null hypothesis

    and

    A P value for the probability of obtaining said result if the null hypothesis is true

Every parametric statistical test assumes:

    1. Independence of observations:
       Many measurements of one test subject are not independent,
       while measurements of many different test subjects are independent
       
    2. Homogeneity of variance:
       That variance within each group is similar

    3. Normality of data:
       That quantitative data follows a normal distribution
       

Choosing a test for parametric data can be done by following the steps
in the image below. Credit to Scribbr.

![](https://cdn.scribbr.com/wp-content/uploads//2020/01/flowchart-for-choosing-a-statistical-test.png)
