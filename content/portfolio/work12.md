+++
draft = false
image = "img/result/xv_folds.png"
date = "2019-12-12"
title = "Prediction"
categories = [ "Results"]
weight = 12
+++

Random Forest Prediction of Event Outcomes

<!--more-->

Random Forests are trained using the 359,781 samples of complete-predictor batted-ball event data. For model evaluation, we consider two cross-validative strategies. First, we perform traditional 50-fold Cross Validation, in which we separate the samples randomly into 50 folds, and for iterations i=1, ..., 50, train the model on all folds j not equal to i, and use the ith fold as the testing set. The purpose of this approach is primarily for developing insights into how effectively, the model is making predictions, and in particular, where and when it is getting predictions wrong. We evaluate our strategy using a Confusion Matrix. A confusion matrix is constructed by generating a K*K matrix, where the row-wise entries are the predicted outcomes, and the column-wise entries are the true outcomes. A single (i, j) entry represents the fraction times the true items of class j are predicted to be part of the ith class. Ideally, an effective model will have true outcomes predominantly being predicted into the correct class, in which the on-diagonal entries will exceed the off-diagonal entries.

![](/img/result/xv_folds.png)

Figure 1: The average confusion matrix after 50-fold cross-validation. Individual cells are colored by the fraction of samples with the true outcome indicated by the column predicted into the predicted outcome indicated by the row (that is, each row sums to 100), and the average percent is reported along with the standard deviation across all entries. As we can see based on the confusion matrix, the model performs exceptionally well for both Outs and Home runs, as these two classes individually see an accuracy rate of 93.8% and 72.6%, with the accuracy for singles more modest at 52.9%. The model is relatively ineffective for predicting both doubles and triples, which are most commonly mislabelled as outs. Of note, Outs represent over 60% of the dataset, so it is not surprising that most of the incorrect predictions are mislabelled as outs (as the leaf nodes will consist >60% of outs).

Second, we compare our model to the "random guess" classifier, which simply guesses the maximally proportionate class. An effective classifier will certainly outperform the "random guess" classifier, so this serves as an effective benchmark for a minimal acceptable classification accuracy. The average accuracy is 79.0+/-.4%, whereas the random guess classifier has only 66.6+/- .6% accuracy, indicating that our SPORF classifier substantially outperforms the random guess classifier. 
