 +++
draft = false
image = "img/result/Mike_Trout_2019_hold.png"
date = "2019-12-12"
title = "Shniy App Demo"
categories = [ "Resources"]
weight = 2
+++

We created two shiny apps to help visualize and search data. Due to large data size, the applications are not currently hosted online, however all code and data necessary to run the applications are available on our [github repository](https://github.com/ebridge2/rfxWOBA). Note that the data is stored on github using [Git Large File Storage](https://git-lfs.github.com/), so installing Git LFS is necessary to obtain the data.

<!--more-->

All of the data necessary for the shiny apps are contained in the `./data/shiny` directory of the repository.

The first app is found in the repository directory `./shiny/PlayerStats`, and displays densities of the sample of 1,000 *rfxwOBA* values generated for a given player in each of the 2017-2019 seasons. It also allows to visualize a plot of the rolling values of *wOBA*, *rfxwOBA*, and *bsxwOBA* over the three seasons. A demo for this application can be found [here](https://www.youtube.com/watch?v=4_vxycpgTuk&feature=youtu.be).

The second app is found in the repository directory `./shiny/BattedBall`, and uses the *SPORF* model that held out 2019's season data to make predictions on batted ball events. The app allows the user to randomly select a real play from the 2019 season, or to input custom values of batted ball measurements to generate a prediction. A demo for this application can be found [here](https://www.youtube.com/watch?v=iB5M5RliKTI).
