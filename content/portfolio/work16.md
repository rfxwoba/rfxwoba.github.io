+++
draft = false
image = "img/result/feat_imp.png"
date = "2019-12-12"
title = "Feature Importances"
categories = [ "Results"]
weight = 2
+++

Using a model trained on all complete data

<!--more-->

The table below displays $10$ players who had at least $100$ plate appearances in consecutive years from the data set with *wOBA*, *rfxwOBA*, and *bsxwOBA* values from one season and the following season.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Batter Name </th>
   <th style="text-align:right;"> PA </th>
   <th style="text-align:right;"> PA Next Season </th>
   <th style="text-align:right;"> wOBA </th>
   <th style="text-align:right;"> wOBA Next Season </th>
   <th style="text-align:right;"> rfxwOBA </th>
   <th style="text-align:right;"> rfxwOBA Next Season </th>
   <th style="text-align:right;"> bsxwOBA </th>
   <th style="text-align:right;"> bsxwOBA Next Season </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> J.D. Martinez </td>
   <td style="text-align:right;"> 481 </td>
   <td style="text-align:right;"> 638 </td>
   <td style="text-align:right;"> 0.437 </td>
   <td style="text-align:right;"> 0.430 </td>
   <td style="text-align:right;"> 0.410 </td>
   <td style="text-align:right;"> 0.422 </td>
   <td style="text-align:right;"> 0.432 </td>
   <td style="text-align:right;"> 0.418 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mike Trout </td>
   <td style="text-align:right;"> 492 </td>
   <td style="text-align:right;"> 582 </td>
   <td style="text-align:right;"> 0.443 </td>
   <td style="text-align:right;"> 0.449 </td>
   <td style="text-align:right;"> 0.427 </td>
   <td style="text-align:right;"> 0.438 </td>
   <td style="text-align:right;"> 0.421 </td>
   <td style="text-align:right;"> 0.427 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Luke Voit </td>
   <td style="text-align:right;"> 124 </td>
   <td style="text-align:right;"> 161 </td>
   <td style="text-align:right;"> 0.321 </td>
   <td style="text-align:right;"> 0.449 </td>
   <td style="text-align:right;"> 0.351 </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:right;"> 0.343 </td>
   <td style="text-align:right;"> 0.441 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mookie Betts </td>
   <td style="text-align:right;"> 703 </td>
   <td style="text-align:right;"> 606 </td>
   <td style="text-align:right;"> 0.345 </td>
   <td style="text-align:right;"> 0.452 </td>
   <td style="text-align:right;"> 0.363 </td>
   <td style="text-align:right;"> 0.448 </td>
   <td style="text-align:right;"> 0.343 </td>
   <td style="text-align:right;"> 0.429 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Howie Kendrick </td>
   <td style="text-align:right;"> 159 </td>
   <td style="text-align:right;"> 369 </td>
   <td style="text-align:right;"> 0.345 </td>
   <td style="text-align:right;"> 0.412 </td>
   <td style="text-align:right;"> 0.339 </td>
   <td style="text-align:right;"> 0.429 </td>
   <td style="text-align:right;"> 0.316 </td>
   <td style="text-align:right;"> 0.420 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Nelson Cruz </td>
   <td style="text-align:right;"> 586 </td>
   <td style="text-align:right;"> 512 </td>
   <td style="text-align:right;"> 0.362 </td>
   <td style="text-align:right;"> 0.429 </td>
   <td style="text-align:right;"> 0.398 </td>
   <td style="text-align:right;"> 0.413 </td>
   <td style="text-align:right;"> 0.395 </td>
   <td style="text-align:right;"> 0.419 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Anthony Rendon </td>
   <td style="text-align:right;"> 592 </td>
   <td style="text-align:right;"> 638 </td>
   <td style="text-align:right;"> 0.386 </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:right;"> 0.408 </td>
   <td style="text-align:right;"> 0.429 </td>
   <td style="text-align:right;"> 0.387 </td>
   <td style="text-align:right;"> 0.408 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mike Trout </td>
   <td style="text-align:right;"> 582 </td>
   <td style="text-align:right;"> 586 </td>
   <td style="text-align:right;"> 0.449 </td>
   <td style="text-align:right;"> 0.447 </td>
   <td style="text-align:right;"> 0.438 </td>
   <td style="text-align:right;"> 0.455 </td>
   <td style="text-align:right;"> 0.427 </td>
   <td style="text-align:right;"> 0.451 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Christian Yelich </td>
   <td style="text-align:right;"> 649 </td>
   <td style="text-align:right;"> 564 </td>
   <td style="text-align:right;"> 0.425 </td>
   <td style="text-align:right;"> 0.454 </td>
   <td style="text-align:right;"> 0.419 </td>
   <td style="text-align:right;"> 0.423 </td>
   <td style="text-align:right;"> 0.404 </td>
   <td style="text-align:right;"> 0.417 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Cody Bellinger </td>
   <td style="text-align:right;"> 623 </td>
   <td style="text-align:right;"> 640 </td>
   <td style="text-align:right;"> 0.348 </td>
   <td style="text-align:right;"> 0.426 </td>
   <td style="text-align:right;"> 0.345 </td>
   <td style="text-align:right;"> 0.431 </td>
   <td style="text-align:right;"> 0.320 </td>
   <td style="text-align:right;"> 0.422 </td>
  </tr>
</tbody>
</table>


The following table displays correlation of each metric to the following season's *wOBA* with $95\%$ confidence intervals.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Metric </th>
   <th style="text-align:right;"> Correlation to Next Season wOBA </th>
   <th style="text-align:left;"> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> wOBA </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:left;"> [0.36, 0.483] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> rfxwOBA </td>
   <td style="text-align:right;"> 0.492 </td>
   <td style="text-align:left;"> [0.433, 0.547] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> bsxwOBA </td>
   <td style="text-align:right;"> 0.445 </td>
   <td style="text-align:left;"> [0.383, 0.503] </td>
  </tr>
</tbody>
</table>


The following table displays correlation of each metric to itself in the following season with $95\%$ confidence intervals.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Metric </th>
   <th style="text-align:right;"> Correlation to Itself Next Season </th>
   <th style="text-align:left;"> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> wOBA </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:left;"> [0.36, 0.483] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> rfxwOBA </td>
   <td style="text-align:right;"> 0.616 </td>
   <td style="text-align:left;"> [0.568, 0.661] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> bsxwOBA </td>
   <td style="text-align:right;"> 0.625 </td>
   <td style="text-align:left;"> [0.577, 0.669] </td>
  </tr>
</tbody>
</table>

Using models trained with one year held out at a time

We repeated the analysis above, but calculated $rfxWOBA$ for each year in a different way: to calculate $rfxWOBA$ for a given year, we trained the $SPORF$ only on the other two years, out of concern for bias arising from redundant data usage. This procedure left the results nearly identical. (We believe this is due to the fact that year was not included as a predictor, and the probability distributions governing the outcomes and predictors are roughly equal from year to year.)

The table below displays $10$ players who had at least $100$ plate appearances in consecutive years from the data set with *wOBA*, *rfxwOBA*, and *bsxwOBA* values from one season and the following season.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Batter Name </th>
   <th style="text-align:right;"> PA </th>
   <th style="text-align:right;"> PA Next Season </th>
   <th style="text-align:right;"> wOBA </th>
   <th style="text-align:right;"> wOBA Next Season </th>
   <th style="text-align:right;"> rfxwOBA </th>
   <th style="text-align:right;"> rfxwOBA Next Season </th>
   <th style="text-align:right;"> bsxwOBA </th>
   <th style="text-align:right;"> bsxwOBA Next Season </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> J.D. Martinez </td>
   <td style="text-align:right;"> 481 </td>
   <td style="text-align:right;"> 638 </td>
   <td style="text-align:right;"> 0.437 </td>
   <td style="text-align:right;"> 0.430 </td>
   <td style="text-align:right;"> 0.411 </td>
   <td style="text-align:right;"> 0.427 </td>
   <td style="text-align:right;"> 0.432 </td>
   <td style="text-align:right;"> 0.418 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mike Trout </td>
   <td style="text-align:right;"> 492 </td>
   <td style="text-align:right;"> 582 </td>
   <td style="text-align:right;"> 0.443 </td>
   <td style="text-align:right;"> 0.449 </td>
   <td style="text-align:right;"> 0.431 </td>
   <td style="text-align:right;"> 0.443 </td>
   <td style="text-align:right;"> 0.421 </td>
   <td style="text-align:right;"> 0.427 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Luke Voit </td>
   <td style="text-align:right;"> 124 </td>
   <td style="text-align:right;"> 161 </td>
   <td style="text-align:right;"> 0.321 </td>
   <td style="text-align:right;"> 0.449 </td>
   <td style="text-align:right;"> 0.359 </td>
   <td style="text-align:right;"> 0.429 </td>
   <td style="text-align:right;"> 0.343 </td>
   <td style="text-align:right;"> 0.441 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mookie Betts </td>
   <td style="text-align:right;"> 703 </td>
   <td style="text-align:right;"> 606 </td>
   <td style="text-align:right;"> 0.345 </td>
   <td style="text-align:right;"> 0.452 </td>
   <td style="text-align:right;"> 0.372 </td>
   <td style="text-align:right;"> 0.454 </td>
   <td style="text-align:right;"> 0.343 </td>
   <td style="text-align:right;"> 0.429 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Howie Kendrick </td>
   <td style="text-align:right;"> 159 </td>
   <td style="text-align:right;"> 369 </td>
   <td style="text-align:right;"> 0.345 </td>
   <td style="text-align:right;"> 0.412 </td>
   <td style="text-align:right;"> 0.344 </td>
   <td style="text-align:right;"> 0.426 </td>
   <td style="text-align:right;"> 0.316 </td>
   <td style="text-align:right;"> 0.420 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Nelson Cruz </td>
   <td style="text-align:right;"> 586 </td>
   <td style="text-align:right;"> 512 </td>
   <td style="text-align:right;"> 0.362 </td>
   <td style="text-align:right;"> 0.429 </td>
   <td style="text-align:right;"> 0.403 </td>
   <td style="text-align:right;"> 0.409 </td>
   <td style="text-align:right;"> 0.395 </td>
   <td style="text-align:right;"> 0.419 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Anthony Rendon </td>
   <td style="text-align:right;"> 592 </td>
   <td style="text-align:right;"> 638 </td>
   <td style="text-align:right;"> 0.386 </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:right;"> 0.413 </td>
   <td style="text-align:right;"> 0.426 </td>
   <td style="text-align:right;"> 0.387 </td>
   <td style="text-align:right;"> 0.408 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Mike Trout </td>
   <td style="text-align:right;"> 582 </td>
   <td style="text-align:right;"> 586 </td>
   <td style="text-align:right;"> 0.449 </td>
   <td style="text-align:right;"> 0.447 </td>
   <td style="text-align:right;"> 0.443 </td>
   <td style="text-align:right;"> 0.451 </td>
   <td style="text-align:right;"> 0.427 </td>
   <td style="text-align:right;"> 0.451 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Christian Yelich </td>
   <td style="text-align:right;"> 649 </td>
   <td style="text-align:right;"> 564 </td>
   <td style="text-align:right;"> 0.425 </td>
   <td style="text-align:right;"> 0.454 </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:right;"> 0.420 </td>
   <td style="text-align:right;"> 0.404 </td>
   <td style="text-align:right;"> 0.417 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Cody Bellinger </td>
   <td style="text-align:right;"> 623 </td>
   <td style="text-align:right;"> 640 </td>
   <td style="text-align:right;"> 0.348 </td>
   <td style="text-align:right;"> 0.426 </td>
   <td style="text-align:right;"> 0.350 </td>
   <td style="text-align:right;"> 0.428 </td>
   <td style="text-align:right;"> 0.320 </td>
   <td style="text-align:right;"> 0.422 </td>
  </tr>
</tbody>
</table>



The following table displays correlation of each metric to the following season's *wOBA* with $95\%$ confidence intervals.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Metric </th>
   <th style="text-align:right;"> Correlation to Next Season wOBA </th>
   <th style="text-align:left;"> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> wOBA </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:left;"> [0.36, 0.483] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> rfxwOBA </td>
   <td style="text-align:right;"> 0.490 </td>
   <td style="text-align:left;"> [0.431, 0.545] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> bsxwOBA </td>
   <td style="text-align:right;"> 0.445 </td>
   <td style="text-align:left;"> [0.383, 0.503] </td>
  </tr>
</tbody>
</table>


The following table displays correlation of each metric to itself in the following season with $95\%$ confidence intervals.

<table class="table table-striped" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> Metric </th>
   <th style="text-align:right;"> Correlation to Itself Next Season </th>
   <th style="text-align:left;"> 95% CI </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> wOBA </td>
   <td style="text-align:right;"> 0.424 </td>
   <td style="text-align:left;"> [0.36, 0.483] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> rfxwOBA </td>
   <td style="text-align:right;"> 0.616 </td>
   <td style="text-align:left;"> [0.568, 0.661] </td>
  </tr>
  <tr>
   <td style="text-align:left;"> bsxwOBA </td>
   <td style="text-align:right;"> 0.625 </td>
   <td style="text-align:left;"> [0.577, 0.669] </td>
  </tr>
</tbody>
</table>

Below, we display a plot that shows how this metric might be used. 
