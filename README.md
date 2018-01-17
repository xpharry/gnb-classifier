# GNB_Classifier
CarND-Term3: Path Planning. A Mini-Project on manually construct a Gaussian Naive Bayes Classifier for Trajectory Classifying.

## Problem Overview
This example is to implement a Gaussian Naive Bayes classifier to predict the behavior of vehicles on a highway. In the image below you can see the behaviors you'll be looking for on a 3 lane highway (with lanes of 4 meter width). The dots represent the d (y axis) and s (x axis) coordinates of vehicles as they either...

1. change lanes left (shown in blue)
2. keep lane (shown in black)
3. or change lanes right (shown in red)

![image](./trajectory_classifier.png)

This classifier can predict which of these three maneuvers a vehicle is engaged in given a single coordinate (sampled from the trajectories shown below).

Each coordinate contains 4 features:

- s
-  d
- s_dot 
- d_dot 

The lane width is 4 meters (this might be helpful in engineering additional features for the algorithm).

## Instruction

Implement the `train(self, data, labels)` method in the class `GNB` in `classifier.cpp`.

Training a Gaussian Naive Bayes classifier consists of computing and storing the mean and standard deviation from the data for each label/feature pair. For example, given the label "change lanes left” and the feature s_dot, it would be necessary to compute and store the mean and standard deviation of s_dot over all data points with the "change lanes left” label.

## Other Resources

- [sklearn documentation on GaussianNB](http://scikit-learn.org/stable/modules/naive_bayes.html#gaussian-naive-bayes)
- [Wikipedia article on Naive Bayes / GNB](https://en.wikipedia.org/wiki/Naive_Bayes_classifier#Gaussian_naive_Bayes)