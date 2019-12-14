+++
draft = false
image = "img/result/feat_imp.png"
date = "2019-12-12"
title = "Feature Importances"
categories = [ "Results"]
weight = 2
+++

Random Forest Feature Importances

<!--more-->

Second, we are concerned with discerning which features provide, or do not provide, meaningful insights into our predictive task. To this extent, we consider two popular metrics for evaluating the "importance" of features: the Gini importance (G, for Gini) and simply counting the number of times a feature is used across the forest (C, for count). Unlike the count strategy, the gini importance weights a feature's importance by how much it improves the purity a resulting split criterion divides the sample data at a particular node (that is, how much it improves the separation of classes within the dataset). For instance in a 2 class problem, if a particular feature and threshold chosen at a particular node divides the data evenly into the two classes, this feature would receive a high importance, whereas a feature and threshold chosen at a particular node that does little to divide between the two classes would have a lower importance. Both strategies are popular for determining the importance of features leveraged in a Random Forest.

![](/img/result/feat_imp.png)

Figure 2: Assessing the relative importance of features, as determined by the Gini Importance Metric or the Count Metric. Both metrics are normalized across features by the maximum for each respective metric, to make the scales comparable. The top ten features by importance are identical across both Gini and the Count metric. Of note, the Gini clearly places higher relative importance on the Launch Angle, which has the interpretation that the launch angle is extremely effective for creating splits that result in more pure sub-samples at nodes within the random forest.


