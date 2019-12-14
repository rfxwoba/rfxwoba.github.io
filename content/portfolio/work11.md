+++
draft = false
image = "img/intro/data.jpg"
date = "2019-12-12"
title = "Data"
categories = [ "Introduction"]
weight = 11
+++

377,050 samples of baseball batted-event data are collected from TODO. 

<!--more-->

For this investigation, we are interested in event-related batted ball-outcomes; that is, those at-bats that end with either 
i) an out 
ii) a single
iii) a double
iv) a triple
v) a home run

Predictors of interest are broken into two categories: those that the batter has control of, and those the batter does not have control of. 100% of the dataset contains valid outcome variables, whereas 4.6% of the dataset contains incomplete predictor rows. The dataset consists of of 239,521 (66.5%) of outs, 75,935 (21.1%) of singles, 24,345 (6.7%) of doubles, 2356 (0.6%) of triples, and 17,624 (4.9%) of home runs. The predictors of interest are organized as follows:

1. Batter-Controlled Predictors
    + Launch Speed: The velocity the ball is hit.
    + Launch Angle: The angle of the ball's trajectory, relative the ground.
    + Spray Angle: The angle of of the ball's trajectory, relative the field. TODO Joe add citation
    + Strike Zone, Top: Whether the ball is in the top of the batter's strike zone.
    + Strike Zone, Bottom: Whether the ball is in the bottom of the batter's strike zone.
    + Ball/Strike Count: The current number of balls/strikes in the count.
    + Batting Handedness: The side of the plate from which the batter hits.
    + Sprint Speed: The top sprint speed of the batter.
2. Non-Batter-Controlled Predictors
    + Release Position of Pitch (x/y/z): The position the ball is release from.
    + Velocity of Pitch (x/y/z/cumulative): The velocity of the pitch.
    + Zone: The categorical zone in which the ball crosses the plate.
    + Pitcher Throwing Handedness: The hand from which the pitcher throws.
    + Movement of Pitch (x,z): The relative drop of the pitch in the x and z dimensions.
    + Plate Location (x, z): The location at which the ball crosses the plate.
    + Runner Positions: Whether there are runners on 1st, 2nd, or 3rd bases at the time of the at-bat.
    + Acceleration of Pitch (x/y/z/cumulative): THe acceleration of the pitch.
    + Effective Speed: The effective speed of the pitch, based on where the pitcher releases the ball.
    + Release Spin Rate: The spin rate of the pitch.
    + Release Extension: The extension point at which the pitch is released.
    + Pitch Number: Total number of pitches thrown.
    + Pitch Name: The label of the pitch type (fastball, curveball, changeup, etc.).
    + Fielder Defensive Statistics: The defensive rating of each of the 9 fielders. TODO what statistic is used?
    + Score of Batter's Team: Score of the team the batter is on.
    + Score of Pitcher's Team: Score of the team the pitcher is on.
    + Infield Fielding Alignment: The label of the infield fielding strategy employed (traditional, overshift, extra infielder, etc.).
    + Outfield Fielding Alignment: The label of the outfield fielding strategy employed (traditional, overshift, extra outfielder, etc.).
    + Inning Number: The number of the inning.
    + Inning Half: Whether it is the top or bottom of the inning.



