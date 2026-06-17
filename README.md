# Digital Twin for Water Network Leak Detection

## Project Overview

This project investigates machine learning and deep learning techniques for water network leak detection using the LeakDB dataset. The study compares Random Forest, Long Short-Term Memory (LSTM), and CNN-LSTM models for identifying leak and non-leak conditions using pressure, demand, and flow-related features.

This project was developed for the Deep Learning Applications module (CMP-L016).

## Dataset

The dataset used in this project is LeakDB.

The dataset contains the following features:

* AvgDemand_PercentDiff
* AvgPressure_PercentDiff
* Link1_PercentDiff
* Link2_PercentDiff
* Link3_PercentDiff
* Link4_PercentDiff

Target variable:

* Leak

  * 0 = No Leak
  * 1 = Leak

After preprocessing, the dataset contained 559,798 records.

## Models Implemented

The following models were developed and evaluated:

1. Random Forest
2. LSTM
3. CNN-LSTM

## Main Results

| Model         | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
| ------------- | -------: | --------: | -----: | -------: | ------: |
| Random Forest |   99.83% |    97.76% | 93.66% |   95.67% |  0.9999 |
| LSTM          |   97.96% |     0.00% |  0.00% |    0.00% |  0.5009 |
| CNN-LSTM      |   97.96% |     0.00% |  0.00% |    0.00% |  0.4921 |

## Requirements

The notebook can be run in Google Colab. The main Python libraries used are:

* pandas
* numpy
* matplotlib
* scikit-learn
* tensorflow
* keras

## How to Run

1. Open the notebook `DL.ipynb` in Google Colab.
2. Upload the dataset file to the Colab environment.
3. Make sure the dataset path matches the path used in the notebook:

```python
/content/Dataset - 2 (LeakDB).csv
```

4. Run the notebook cells from top to bottom.
5. The notebook will generate:

   * Dataset distribution graph
   * Confusion matrices
   * Training accuracy and loss curves
   * ROC curve
   * Precision-Recall curve
   * Feature importance graph
   * Final model comparison table

## Repository Contents

```text
DL.ipynb
README.md
```

Optional folders may include:

```text
figures/
results/
```

## Key Findings

The Random Forest model achieved the best performance for leak detection. Although LSTM and CNN-LSTM achieved high accuracy, they failed to detect leak events effectively due to severe class imbalance in the dataset. This shows that accuracy alone is not sufficient for evaluating imbalanced classification problems.

## Author

Madhu Sudhan Atheni
Student ID: A00033579
MSc Data Science
University of Roehampton

