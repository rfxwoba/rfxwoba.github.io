+++
date = "2019-12-12"
title = "Model"
draft = false
image = "img/method/random_forest.png"
categories = [ "Methods"]
weight = 1
+++

<!--more-->

For this analysis, we chose to employ a random forest that inputs the predictors described above to predict one of the five batted ball outcomes. In the random forest model, we only considered batted balls that contained values for all the predictors above. 

![](/img/method/dag.png)

One reason for choosing a random forest is that many of the predictors are highly interactive in their propensity to produce certain outcomes. Another reason is that the random forest allows us to include an extensive set of features, so that we can identify which features are most important in predicting outcomes of batted balls. We expect that the features that are direct measurements of a batted ball, such as launch speed, launch angle, and spray angle, will be the most predictive of its outcome. However, we are also interested in identifying if other factors, such as attributes of the pitch, defense, or stadium, are important in predicting outcomes. Additionally, by including an expansive set of features, we can assess how well the most modern, cutting-edge measurements of baseball plays can predict their outcomes.


## SPORF

The particular implementation of Random Forest employed is [SPORF](https://arxiv.org/abs/1506.03410), or Sparse Projection Oblique Randomer Forests. Traditional Random Forests build upon the axis-aligned decision tree: that is, the trees split only along features that exist within the feature space of the dataset of interest. By contrast, oblique decision trees extend the split criterion to along one or more features. For a simple example, consider for instance when the outcome of interest is whether or not it is raining today. If we know that it rained yesterday, and we know that it is forecast to rain tomorrow, either one of these pieces of information may individually provide valuable insights into predicting whether or not it is raining today. However, considered together; that is, that it rained yesterday and it is forecast to rain tomorrow, these two pieces of information may yield a much stronger prediction to whether it is raining today. While an axis-aligned decision tree may well be capable of generating trees that can recognize this particular pattern, as the feature space widens, the tree depth to identify these "oblique" tendencies in the feature space grow exponentially. Trees of substantial depth unfortunately tend to lose generalizability and have a tendency to overfit the sample data. Fortunately, numerous strategies (for example, [XGBoost](https://arxiv.org/abs/1603.02754)) have been introduced to generate "oblique" ensembles: random forests built upon decision trees wholse split criterions include linear combinations, rotations, and other transforms of the individual features. SPORF was developed to accomodate these oblique strategies, while providing many of the computational benefits of a traditional axis-aligned method (particularly, computational efficiency, insensitivity to a large proportion of noisy inputs, and interpretability). For these reasons, as well as the ease-of-use of `SPORF` in the `R` programming language and heavy `C` optimization, we choose to use `SPORF`s for our project.


