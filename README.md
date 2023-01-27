# Modulation Classification

## Problem Statement

DeepSig Dataset: RadioML 2016.04C
A synthetic dataset, generated with GNU Radio, consisting of 10 modulations(2 Analog, 8 Digital).
This is a variable-SNR dataset with moderate LO drift, light fading, and numerous
different labeled SNR increments for use in measuring performance across
different signal and noise power scenarios.

You can download the dataset from [__here!__](http://opendata.deepsig.io/datasets/2016.10/RML2016.10b.tar.bz2)

## Creating Different Feature Spaces

Each sample was represented using two vectors where each of them has 128 elements.

We created the following operations to generate new feature spaces from the raw data.

1. Raw time series as given (two channels)
1. First derivative in time (two channels)
1. Integral in time (two channels)
1. Combinations of 1,2 and 3. (More channels)

## Data Reorganization

we split the data into 70% training/validation and 30% for training, we also used 5% of the training/validation set for validation.

## Models Used

We built 3 models: CNN, vanilla RNN and LSTM as classifiers for our problems.

## Big Picture

We compared each of the learning models used with different features and realized the accuracies and the difference of performance between each classifier

## More Details?

There is a [__PDF__](https://github.com/iZarrios/modulation-classification/blob/master/Report/Modulation%20Classification%20Report.pdf) included which has our trials results as well as some other aspects such as F1 score and confusion matrix for each SNR value available in the dataset.
