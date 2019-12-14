+++
image = "img/intro/research.jpeg"
date = "2019-12-12"
title = "Study aim"
categories = [ "Introduction" ]
draft = false
weight = 4
+++

<!--more-->

Although *wOBA* is a very useful statistic because it attempts to tie batter outcomes directly to run production, it is still “outcome-oriented” in that it is purely a function of the batter’s game-recorded outcomes. Outcome-oriented statistics are convenient and justifiable in the longterm, but they are not necessarily optimal for player evaluation and the prediction of future results.

As an analogy, imagine a novice poker player facing off against a professional. Since the game of poker has elements of both luck and skill, it is possible for the novice to beat the professional in a given match. An outcome-oriented analysis would conclude that the novice played better than the professional. But an informed observer would likely be able to recognize that the professional’s decisions throughout the game were actually superior, and he just happened to be unlucky. In much the same way, a batter’s recorded outcomes (single, double, etc.) are the result both of his own actions (hitting the ball and running), and factors outside of his control (defensive quality and stadium factors).

In 2015, a new technology called [Statcast](https://en.wikipedia.org/wiki/Statcast) was introduced to Major League Baseball stadiums. The tool uses high-speed cameras to take measurements of ball and player movements during a game. Statcast produces a robust set of data about each baseball play, providng a large quantity of data that can be used to evaluate players in ways qualitatively different from what has been previously possible.

Using Statcast data, we may be able to identify the value of *batter-based* actions, we might arrive at an expectation of *wOBA* that is a more accurate indicator of batter quality than *wOBA* itself, which only considers the outcomes of each play.

This concept is not new; the analytics firm Statcast calculates a statistic called [*xwOBA*](http://m.mlb.com/glossary/statcast/expected-woba), short for "expected wOBA," which attempts to determine the *wOBA* that could be expected from the batter's contact with the ball, as measured by launch speed, or the velocity at which the ball leaves the bat, and launch angle, or the vertical angle at which the ball leaves the bat. However, to our knowledge the algorithm used to calculate the statistic is not publicly available. We will calculate our own version of expected wOBA which uses many more variables than what Statcast claims to. We believe that one of these variables, sprint speed, should add value to the model because it is a batter-level variable that is an important factor in whether a given batted ball is converted into a single, double, or triple. Another factor that we believe will be important is spray angle, which is an engineered feature that approximates the horizontal angle describing the direction in the field that the ball was hit. We also include other variables *outside* the batter's control and attempt to marginalize over their league-distribution. It is debatable whether such a procedure should produce better predictions of *wOBA* than simply omitting those variables from the beginning, but including them allows us to answer independent questions of interest with regard to what external factors affect batting outcomes.
