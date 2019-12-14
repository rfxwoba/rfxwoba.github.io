+++
draft = false
image = "img/method/woba.png"
date = "2019-12-12"
title = "rfxwOBA"
categories = [ "Methods"]
weight = 10
+++

<!--more-->

As stated above, we will use the results of the random forest model to produce our own expectation of *wOBA*. In order to produce this, we will use a permutation strategy to create a marginal distribution of expected *wOBA* for each batted ball event. The process will be executed as follows:

* Assign the appropriate wOBA weights to all non-batted ball events (0 for strikeouts and 0.7 for walks and hit by pitch)
* Subset the data to only include the batted ball events and randomly impute any missing predictors from the complete cases
* Randomly shuffle the rows for every predictor except for five predictors which are direct measurements of the batter *(batter handedness, launch speed, launch angle, spray angle and sprint speed)*
* Produce predicted probabilities of each outcome for each event by running this modified data set through the random forest
* Linearly combine these predicted probabilities with the corresponding *wOBA* weights to produce an expected *wOBA* value for each event

We chose to keep the five predictors listed above as constant in this process because we believe that those five variables are the best indicators of a batter's skill in producing a positive batted ball outcome.

We will repeat this procedure 1000 times to produce 1000 expected *wOBA* values for each event. We will consider this to be a sample from the distribution of expected *wOBA* values for an event given the five "batter" measurements held constant. Using these values for a given player over a season, we can produce 1000 expected *wOBA* values for that player in that season. We can visaulize and analyze the distribution of these expected *wOBA* values, as well as produce a point estimate of expected *wOBA* by taking the mean of the 1000 values. We will refer to this point estimate as *rfxwOBA* or "random forest expected wOBA".

We will produce these distributions and metrics in two ways. Once by obtaining estimates of the entire data set (2017-2019 seasons) on a model trained on the complete cases of the entire data set. We will also fit three additional random forest models, with each of them holding out one season's data from the training set. Then we will produce the estimates for the events in a given season using the model that did not include that season's data in the training set.

In order to assess the validity of this metric for projecting a player's future performance, we will calculate league-wide correlations of a season's *rfxwOBA* to the following season's *wOBA*, and comparing it to the correlation of the season's *wOBA* to the following season's *wOBA*. A stronger association between *rfxwOBA* and next season's *wOBA* than *wOBA* and next season's *wOBA* will suggest evidence that *rfxwOBA* is a better predictor of a player's future performance than actual *wOBA*. We will also assess the reliability of *rfxwOBA* by calculating the correlation of league-wide *rfxwOBA* in a season to *rfxwOBA* in the following season.

The data exported from Baseball Savant also includes a column labeled `estimated_woba_using_speedangle` for each event. There is not documentation on how these values are calculated. We will also produce expected *wOBA* values from these values, referred to as "baseball savant expected wOBA" or *bsxwOBA*. We will also consider this metric in assessing player projection and metric reliability.