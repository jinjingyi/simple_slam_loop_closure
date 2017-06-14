# Simple loop closure for Visual SLAM

Possibily the simplest example of loop closure for Visual SLAM. More information [on my blog](http://nicolovaligi.com/bag-of-words-loop-closure-visual-slam.html).

As I'm experimenting with alternative approaches for SLAM loop closure, I wanted a baseline that was reasonably close to state-of-the art approaches. The approach here is pretty similar to ORB-SLAM's, and uses SURF descriptors and *bag of words* to translate them to a global image description vector.

## The dataset

For testing, I've used the New College dataset published alongside FAB-MAP. It's available for download [here](http://www.ijrr.org/ijrr_2008/volume27-issue6/090961/3_data.htm). It's ideal for loop-closure testing, since it includes manual place associations that can be used for evaluation.

## Installation

The cmake build script downloads and build the [DBoW2 library](https://github.com/dorian3d/DBoW2) that's used for the bag of words representation.

## Compatibility

Only tested on Ubuntu 16.04 LTS with OpenCV3, gcc 5.4.0

## Plotting the confusion matrix

The `ground_truth_comparison.py` plots and compares the loop closures from the ground truth to the actual results from the code.
