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

\[
wOBA = \frac{0.7*(W+HBP)+0.9*S+1.25*D+1.6*T+2*HR}{PA-SacB}
\]

where W is the number of walks, HBP is the number of times hit-by-pitch (same outcome as walk), S is the number of singles, D is the number of doubles, T is the number of triples, HR is the number of home runs, PA is the number of plate appearances, and SacB is the number of sacrifice bunts. 

![](/img/intro/woba.png)

The weights in the numerator are calculated so as to represent the number of additional runs scored that can be expected by a given batting outcome, relative to that batter instead getting out. The denominator normalizes the statistic to account for the fact that some batters have more opportunities to hit (plate appearances) than others. (Sacrifice bunts are a technicality that can be ignored for the purposes of understanding.)

Therefore, wOBA may be seen as a kind of "gold-standard" batting statistic; a player's wOBA represents a relative measure of how many runs he tends to contribute each time he goes to bat.
