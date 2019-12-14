+++
draft = false
image = "img/intro/data.jpg"
date = "2019-12-12"
title = "Data"
categories = [ "Introduction"]
weight = 5
+++

554,149 samples of baseball event data are collected from [Baseball Savant](https://baseballsavant.mlb.com/statcast_search).

<!--more-->

For this investigation, we are interested in event-related batted ball-outcomes; that is, those at-bats that end with either i) an out , ii) a single, iii) a double, iv) a triple, or v) a home run. (Technically, an event recorded as an “out” may have been a fielding error that allowed the batter to reach base.) 377,050 (68.6%) of the samples produced a batted ball event. Predictors of interest are broken into two categories: those that the batter controls at least partially, and those the batter does not control. 100% of the dataset contains valid outcome variables, whereas 4.6% of the dataset contains incomplete predictor rows. The dataset consists of of 239,521 (66.5%) of outs, 75,935 (21.1%) of singles, 24,345 (6.7%) of doubles, 2356 (.6%) of triples, and 17,624 (4.9%) of home runs. The predictors of interest are organized as follows:

Predictors of interest are broken into two categories: those that the batter has control of, and those the batter does not have control of. 100% of the dataset contains valid outcome variables, whereas 4.6% of the dataset contains incomplete predictor rows. The dataset consists of of 239,521 (66.5%) of outs, 75,935 (21.1%) of singles, 24,345 (6.7%) of doubles, 2356 (0.6%) of triples, and 17,624 (4.9%) of home runs. The predictors of interest are organized as follows:

1. Batter-Controlled Predictors
    + Launch Speed: The speed of the ball immediately after being hit.
    + Launch Angle: The angle of the ball's trajectory, relative the ground (altitude angle).
    + Spray Angle: The angle of of the ball's trajectory, relative the batter's forward perspective towards the pitcher (azimuth angle). This feature was approximated using a coordinate system of where the ball was fielded. This was accomplished using a formula from a contributor at [The Hardball Times](https://tht.fangraphs.com/research-notebook-new-format-for-statcast-data-export-at-baseball-savant/).
    + Strike Zone, Top: The height of the top of the batter's strike zone. (According to MLB rules, this is halfway between the batter's shoulders and the top of his pants.)
    + Strike Zone, Bottom: The height of the bottom of the batter's strike zone. (According to MLB rules, this is at the batter's knees.)
    + Ball/Strike Count: The current number of balls/strikes when the pitch was thrown.
    + Batting Handedness: The side of the plate from which the batter hits.
    + Sprint Speed: The top sprint speed of the batter measured from that season. This data was also acquired from [Baseball Savant](https://baseballsavant.mlb.com/sprint_speed_leaderboard) in a separate data set.
2. Non-Batter-Controlled Predictors
    + Release Position of Pitch (x/y/z): The position the ball is release from. (The *z*-axis is perpendicular to the ground. The *y*-axis is the forward perspective of the batter towards the pitcher. The *x*-axis is horizontal, running parallel to the front edge of home plate, or equivalently the line connecting first base and third base.)
    + Velocity of Pitch (x/y/z/cumulative): The velocity of the pitch.
    + Zone: The categorical zone in which the ball crosses the plate, split into 14 sectors in the *xz* plane.
    + Pitcher Throwing Handedness: The hand from which the pitcher throws.
    + Movement of Pitch (x, z): The relative drop of the pitch in the x and z dimensions.
    + Plate Location (x, z): The location at which the ball crosses the plate.
    + Runner Positions: Whether there are runners on 1st, 2nd, or 3rd bases at the time of the at-bat.
    + Acceleration of Pitch (x/y/z): The acceleration of the pitch.
    + Effective Speed: The effective speed of the pitch, based on where the pitcher releases the ball.
    + Release Spin Rate: The spin rate of the pitch.
    + Release Extension: The extension point at which the pitch is released.
    + Pitch Number: Total number of pitches thrown in current plate appearance.
    + Pitch Name: The label of the pitch type (fastball, curveball, changeup, etc.).
    + Fielder Defensive Statistics: The defensive rating of each of the 9 fielders. The statistic used for these variables is [Defensive Runs Saved (DRS)](https://library.fangraphs.com/defense/drs/) which measures how many runs above or below average a fielder contributes to their team. In this model, the DRS for the player at that position in that season was normalized to 1,000 innings played. The DRS measurements were obtained from [fangraphs.com](https://www.fangraphs.com/leaders.aspx?pos=all&stats=fld&lg=all&qual=y&type=1&season=2019&month=0&season1=2019&ind=0&team=0&rost=0&age=0&filter=&players=0&startdate=&enddate=).
    + Score of Batter's Team: Score of the team the batter is on.
    + Score of Pitcher's Team: Score of the team the pitcher is on.
    + Infield Fielding Alignment: The label of the infield fielding strategy employed (standard, strategic, shift).
    + Outfield Fielding Alignment: The label of the outfield fielding strategy employed (standard, strategic, extra outfielder).
    + Inning Number: The number of the inning.
    + Inning Half: Whether it is the top or bottom of the inning.

In the data set, 360,967 batted ball events contained complete data for all the predictors listed above. This subset of the data was used for model training.
