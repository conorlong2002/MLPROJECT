# Pulsar Classification CT4101 Machine learning project

## Project overiew

This project is intended to investigate if machine learning can differentiate pulsars from non pulsar candidates using eight numerical features from the HTRU2 dataset.

The target variable is 'class'
- 1 represents a pulsar
- 0 represents a non pulsar

The project covers data inspection, preprocessing, model training and evaluation of results. Accuracy, recall and F1 will be used to assess the performance.
  # The Dataset

  Source: UCI Machine learning repository.
  Dataset: https://archive.ics.uci.edu/dataset/372/htru2

  The dataset contains 17,898 observations and eight numerical input features. These decsribe the mean, standard deviation, skewness and kurtosis of the pulse profile and the DM-SNR curve.

  Class Distribution:
  - Pulsar: 16,529 observations
  - Non-Pulsar: 1,639 observations

    License: Creative commons attrivution 4.0 international (CC BY 4.0).

    Citation:
Lyon, R. (2015). HTRU2 [Dataset]. UCI Machine Learning Repository.
https://doi.org/10.24432/C5DK6R


## Setup
Python version: Python 3.14.0

Download the repository and open a terminal in its main folder, create an active a virtual environment using powershell.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install the required packages:

```powershell
python -m pip install -r requirements.txt
```

## Download data

Open the UCI dataset link above, download the dataset, create a folder named 'data' beside the notebook, place 'HRTU_2' inside the folder

## Running the notebook

Start Jupyter from the main project folder


```powershell
jupyter notebook
```
Open 'Pulsar.ipynb', select the project environment as the kernel and run all cells top down.

## Evaluation

The dataset is split into 80% training data and 20% test data.
Stratification maintains roughly the same class proportions in both sets, and 'random_state=42' allows for the split to be reproducible.

Scaling is fitted only on the training data via a pipeline.
A most frequent dummy classifier is used to provide a baseline.

Because the classes are imbalanced, recall and F1 are used alongside accuracy. The test set is reserved for evaluation and not used to tune model settings.



    
