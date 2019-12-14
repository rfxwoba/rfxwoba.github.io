+++
image = "img/intro/woba_2.jpg"
showonlyimage = false
date = "2019-12-12"
title = "Baseball statistics and wOBA"
categories = [ "Introduction" ]
draft = false
weight = 3
+++

Baseball statistics have been recorded and studied for well over one hundred years.
<!--more-->

Possibly due to the fact that individual actions are relatively easily separable in baseball (i.e., teammates have less of an effect on each other's individual outcomes than in other sports), baseball has also perhaps been the sport most responsible for the origination and explosion of advanced sports analytics, whereby analysts identify measured player accomplishments that are most likely to translate to runs and wins and apply sophisticated statistical methods to make predictions and inferences about such quantities. A pioneer of this work in the late 20th century was Bill James, honored as one of Time Magazine's 100 most influential people in the world for 2006. Advanced baseball statistics, often known as "sabermetrics," entered into popular culture with Michael Lewis's 2003 bestseller *Moneyball: The Art of Winning an Unfair Game* about the Oakland Athletics' adoption of sabermetric principles, later adapted into the Oscar-nominated 2011 film *Moneyball*.

In this project, we are going to focus on the [sabermetric statistic *wOBA*](https://library.fangraphs.com/offense/woba/), which stands for "weighted on-base percentage." For a given sequences of a batter's plate appearances, is calculated as follows:

![](/img/intro/woba.png)

where BB is the number of walks, HBP is the number of times hit-by-pitch (same outcome as walk), S is the number of singles, D is the number of doubles, T is the number of triples, HR is the number of home runs, PA is the number of plate appearances, and SacB is the number of sacrifice bunts.

The weights in the numerator are calculated so as to represent the number of additional runs scored that can be expected by a given batting outcome, relative to that batter instead getting out. The denominator normalizes the statistic to account for the fact that some batters have more opportunities to hit (plate appearances) than others. (Sacrifice bunts are a technicality that can be ignored for the purposes of understanding.)

Therefore, wOBA may be seen as a kind of "gold-standard" batting statistic; a player's wOBA represents a relative measure of how many runs he tends to contribute each time he goes to bat.

wOBA weights vary slightly from year-to-year, but for the purposes of this project we use weights that are displayed in the Baseball Savant data set where the data was obtained. Additionally, wOBA often includes inputs from the baserunning event, stolen bases. In this project we do not considering these events. Note that this means that our calculations of true wOBA may differ slightly from those published on popular baseball statistic websites.
