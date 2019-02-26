# Anomaly Detection

This is the final project for CMPT 318 Cybersecurity, which involves using `R` to perform statistical analysis and anomaly detection on a household electric power consumption dataset.

The project consists of three main parts:

1. explore the characteristic features and seasonal trends of given datasets, then generate graphs to compare the difference between training and testing datasets.

2. use **Out of Range** and **Moving Average** methods to find point anomalies, then record them in `.csv` files.

    * **Out of Range** is based on the `Min` and `Max` values of a feature in specified time windows in training dataset.

    * **Moving Average** is a fixed size window of observations which slides one record at a time. The average of the window is calculated to compare against the value of the record; if the difference is above or below a certain threshold, that record is considered a point anomaly.

3. train **Hidden Markov Models** to compare the log-likelihoods between training and testing datasets. The higher the log-likelihood value, the better the model characterizing the data. So, in theory, the results between training and testing datasets should be similar, with the former performing better.

## Libraries

* `data.table` - for cleaning and aggregating data

* `depmixS4` - for Hidden Markov Model functions

## Folder Structure

    .
    ├── data
    ├── doc
    ├── figs
    ├── output
    ├── project.r
    └── README.md

* The `data` folder contains training and testing datasets in `.txt` files, with a total of 2 million records.

* The `doc` folder contains project requirements and analysis reports.

* The `figs` folder contains generated figures and statistical graphs.

* The `output` folder contains processed datasets, which are anomalous records in `.csv` files.