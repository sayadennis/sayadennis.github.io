---
layout: page
title: Module for Nested CV
description: Portable ML module with nested cross-validation
img: assets/img/classical-ml-screenshot.png
importance: 3
category: work
---

## Portable Nested Cross-Validation Module

<p style="text-align: center;"><a href="https://github.com/sayadennis/classical-ml/tree/main">Link to Repo</a></p>

In my work, I often found myself performing the same nested cross-validation routines repeatedly for different projects. Setting up hyperparameter searches and evaluating generalization performance was tedious and time-consuming. To simplify this process, I decided to build a Python module that automates these tasks, making it reusable and efficient for any dataset.

### What is it?

This module is a portable script that automates nested cross-validation for hyperparameter tuning and generalization performance evaluation. All you need to do is point to your input (X) and target/label (y) CSV files, and the script will take care of the rest. The hyperparameter ranges are pre-defined in a `param_distributions.json` file located in the `ClassicalML/` directory. You’ll have everything you need to evaluate your model effectively and interpret its results.

### Key Features

1. Model Performance Metrics
  * For every test fold of each split in the cross-validation, the module records the balanced accuracy, precision, recall, and F1 scores. 
  * These metrics are saved in a CSV file for easy analysis.
  * The number of splits and folds is fully customizable, so you can tailor it to your specific use case.
2. Feature Importance Scores
  * Ever wondered which features drive your model’s performance? This module calculates feature importance scores for each training set across the folds.
  * The output is a distribution of importance scores, helping you identify consistently influential features.
3. SHAP Scores on Test Sets
  * To better understand model predictions, the module computes SHAP scores for each sample in the test sets.
  * Each sample will have as many SHAP scores as there are splits. 
  * This data is stored in a pickle file for easy integration into downstream analysis.
4. Sample-Wise Performance
  * If you’re performing multiple splits, this feature tracks how often each sample is predicted correctly.
  * By analyzing the proportion of correct predictions for each sample, you can check whether all your samples are misclassified at a similar rate, or if there are a subset of samples that are consistently misclassified.

### Why Use This Module?

* Efficiency: Save time by automating nested cross-validation and related analyses.
* Reusability: Designed to be portable and applicable across multiple projects.
* Insightful Outputs: Beyond just performance metrics, gain deeper insights into feature importance and sample-level behavior.
* Customizable: Specify hyperparameter ranges in a JSON file and control the splits/folds easily.

### Link to Repo

Explore the code and documentation on my [GitHub](https://github.com/sayadennis/classical-ml/tree/main).

This tool has saved me a lot of time for my projects, and I hope it can do the same for yours!

