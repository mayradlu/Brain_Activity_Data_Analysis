# Brain Activity Data Analysis

## General Information
This project aims to analyze brain activity data obtained from neuropsychological experiments using various machine learning classification models. The primary objective is to explore the application of these models to EEG (Electroencephalography) signals, which measure the brain's electrical activity. The project involves four main stages: data collection, data preparation, model evaluation, and transfer learning.

## Project Description 

Electroencephalography (EEG) is a technique used to measure the brain's electrical activity through electrodes placed on the scalp. These signals, known as brain rhythms, are a summation of sinusoidal and cosine oscillations at various frequencies. This study uses the ["Unicorn Hybrid Black"](https://www.gtec.at/product/unicorn-hybrid-black/?srsltid=AfmBOor1sP4KGgQhEqmFyZtbXEVgSk2b7ByEN43XmFPV832OHbX7-R8B), a portable 8-channel EEG device that follows the international 10-20 system for electrode placement.

## Experiments Conducted
Two experiments were conducted to gather and prepare the EEG data:

* P300 Experiment: Participants observed and counted the occurrences of a smiling face appearing at random positions on a screen.Data was collected 800 milliseconds after each appearance, filtered using a bandpass filter (4 Hz to 20 Hz), and spatially filtered to enhance signal quality.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f10677d9-06e7-49d9-91a9-9ead93457661" alt="imagen" width="400">
</p>


* Cognitive Task Experiment: Participants performed various cognitive tasks (calculation, reading, naming objects) for 15 seconds, followed by a 10-second cross-display for non-task data collection. Spectral power analysis (PSD) was applied to these data segments for feature ext
<p align="center">
  <img src="https://github.com/user-attachments/assets/301701a1-9eac-4a23-b83a-9d39e1b4672e" alt="imagen" width="400">
</p>

## Classifiers Used 
Three classification tasks were defined:
* P300 vs. Non-P300 Potential
* Non-Cognitive Task (Cross) vs. Cognitive Task
* Calculation Task vs. Reading Task vs. Naming Task

Five different classifiers were evaluated for these tasks:
* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)
* Multilayer Perceptron (MLP)
* Random Forest
* Decision Tree

## Model Evaluation

The models were evaluated based on the following metrics:
* Precision
* Recall
* Accuracy
* F1-Score
  
A example of the table of model evaluation is shown
<p align="center">
  <img src="https://github.com/user-attachments/assets/082a2674-b733-4237-b646-c0cbf2961f97" alt="imagen" width="600">
</p>


A weighted average was used to account for class imbalance. Hyperparameter tuning was performed for SVM and KNN using techniques such as GridSearch and varying the 'k' value in KNN.

## Feature Selection
A filter-based approach was used for feature selection to reduce data dimensionality. Different values of 'k' were explored to identify the most relevant features.
<p align="center">
  <img src="https://github.com/user-attachments/assets/80dac13b-448b-457f-b5aa-3c0270cf7875" alt="imagen" width="600">
</p>

## Transfer Learning
Transfer learning was tested by training the P300 model on one subject's data and testing it on another's. The decrease in accuracy highlighted potential differences or imbalances in the data between subjects.
<p align="center">
  <img src="https://github.com/user-attachments/assets/7d5069e9-ad21-4565-8a11-7fa99c9e9543" alt="imagen" width="600">
</p>


