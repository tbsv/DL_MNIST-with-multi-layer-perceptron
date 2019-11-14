# Deep Learning // MNIST with multi layer perceptron

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tbsv/DL_MNIST-with-multi-layer-perceptron/master?filepath=MNIST-with-multi-layer-perceptron_solution.ipynb)

This is Binder-compatible repo with a `requirements.txt` file.

## Summary

In this lesson, we will create a multi-layer perceptron model and try to classify handwritten numbers. This is a very common entry-level problem for Tensorflow.

## Contents

There is 1 notebook in this repository:

- [MNIST-with-multi-layer-perceptron_solution.ipynb](MNIST-with-multi-layer-perceptron_solution.ipynb) : runs a MNIST with multi layer perceptron exercise that is taken from a Udemy course (see details in the *About* section below).

In addition, the following ressources are in this repository:

- [requirements.txt](requirements.txt) : lists all Python libraries that the notebook depends on.
- [DATA](DATA) : contains all data sets and further ressources that are used within the Jupyter Notebook.

## Usage

Dependencies are specified in [requirements.txt](/requirements.txt) :

```
pip install -r requirements.txt
```

You can access this repo via **Binder** at the following URL 
https://mybinder.org/v2/gh/tbsv/DL_MNIST-with-multi-layer-perceptron/master or via the Binder badge above.

Alternatively, you can run the notebook locally. Therefore, you will need to have python installed,
preferably through [Anaconda](https://www.anaconda.com/download/).

## Run the notebook

Each cell of code can be run with `shift + enter` or you can run the entire notebook by selecting `Cell` -> `Run All` in the toolbar.

![Screenshot](DATA/jn_run-all.png?raw=true "Screenshot")

For more information on running Jupyter notebooks, see the [Jupyter Documentation](https://jupyter.readthedocs.io/en/latest/).

## Unit tests (for reproduction)

The jupyter notebook contains several unit tests. For testing the model, the following suitable indicators are defined.
1. Accuracy: if accuracy is not empty, the model likely runs as expected.
2. Confusion matrix: if the confusion matrix is present with same dimension, the model likely runs as expected.
3. Runtime: if the runtime is not empty and additionaly doesn't exceed defined vaule with 120%, the model likely runs as expected.


### Test data

- [test-file_01.json](./DATA/test-file_01.json) : contains test data that is used for the unit tests within the Jupyter Notebook.
- [test-file_02.json](./DATA/test-file_02.json) : contains test data that can be used for reproduction of the unit tests within the Jupyter Notebook.

### Output of unit tests (example)
```
test_accuracy (__main__.TestInput) ... ok
test_confusion_matrix (__main__.TestInput) ... ok
test_runtime (__main__.TestInput) ... 
Epoch: 1 Cost=0.2038
Epoch: 2 Cost=0.2097
Epoch: 3 Cost=0.2713
Epoch: 4 Cost=0.2362
Epoch: 5 Cost=0.1698
Epoch: 6 Cost=0.1725
Epoch: 7 Cost=0.2194
Epoch: 8 Cost=0.2141
Epoch: 9 Cost=0.1781
Epoch: 10 Cost=0.1801
Epoch: 11 Cost=0.2359
Epoch: 12 Cost=0.1792
Epoch: 13 Cost=0.1373
Epoch: 14 Cost=0.1545
Epoch: 15 Cost=0.1708
Modellierung ist beendet: 15 Epochs of Training

train_model ran in: 57.73061203956604 sec
ok

----------------------------------------------------------------------
Ran 3 tests in 58.022s

OK
```

### Reproduction of unit tests
If you would like to reproduce the unit tests with anothter data set, you can simply provide another test data file as JSON and change the data import in the following line of the jupyter notebook.

```python
import json
with open('./DATA/test-file_01.json') as json_file:
        test_data = json.load(json_file)
        print("Test data:", test_data)
```

Example: Simple replace 'test-file_01.json' with 'test-file_02.json') and rerun the unit tests.

## Issues

Please [open an issue](https://github.com/tbsv/DL_MNIST-with-multi-layer-perceptron/issues) if you encounter any problems while trying to run the notebooks.

## About
This data science exercise is part of the Digital Business Engineering Master at HHZ.

The given examples were taken from the Udemy course [Python for Data Science, Machine Learning & Visualization](https://www.udemy.com/course/python-data-science-machine-learning/).

Adaptions to the jupyter notebook are made by [Tobias Vetter](mailto:tobias.vetter@student.reutlingen-university.de).