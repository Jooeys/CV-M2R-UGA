This exercise is composed of three parts.
### 1) Construct a data-set of Positive and Negative face imagettes from the first 8 folds of FDDB.
Divide this data set into Training Data and Validation data. The validation data is used to test
for over-fit.
### 2) Construct and train a MultiLayer Perceptron (MLP) with variations in hyper-parameters. Train
and validate each MLP using your test and validation data-sets.
### 3) Evaluate each MLP with the evaluation data set available on the Course web site, and display an
ROC curves for each MLP. Note that the evaluation data has been constructed from folds 9 and
10 of FDDB, to is important not to train on this data.
duplicates, which makes it appropriate for detecting similar
images in our data set.
As with most automatic approaches for duplicate detection, this approach has a trade-off among false positives
and false negatives. To restrict the number of false positives, while maintaining a high t



1) Split FDDB dataset (folds 01-08) into training and validation sets.
2) Generate training samples from dataset folds (01-08). Your training samples need to include
a positive imagette for each face, and a negative imagette of the same size taken at random
from the same image.
3) Build your MLP models using Keras. Remember to resize and flatten your input images into
a fixed size vector before passing them through MLP network.
4) Download the test set, and test your model on the provided imagettes.
5) Tune your model parameters, and post your best model results on


### Question
1. 