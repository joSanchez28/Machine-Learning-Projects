# EPFL Machine Learning - Project 1

* Team Name: Mi Equipo

This is the first class project of the 2018 EPFL Machine Learning course. In this document you can see an overview of the project architecture and how to run it, as well as some useful information about the implementation. If you require more specific information, you can check the report (`report.pdf`).

## Project folders
* `data/`. Directory with the input data, namely `test.csv` and `train.csv` downloaded from Kaggle.
* `docs/`. Directory with the report in pdf `report.pdf` and in `report.tex` and the plots included in this report.  
* `scripts/` Python files
    * `proj1_helpers.py`. Helper functions provided by the course.
    * `implementations.py`. The six functions asked and the implementations required.
    * `run.py`. Execute this file for obtaining the output submitted in Kaggle.
    * `hyperparameters_and_plots.py`. For testing different models with different hyperparameters. Using Ridge Regression and Cross Validation.
* `results/` Directory with the file `csv` with our best result in Kaggle.

## Requirements for running the project

Only a computer with a valid installation of Python 3 is required.
The packaged used are NumPy and Matplotlib, you can get them with pip tool:
* `pip3 install numpy`
* `pip3 install matplotlib`

## Running the project

### Obtaining the `.csv` output
The main program is `run.py`, it has to be executed from the scripts folder:
```
/scripts$ python3 run.py
```
It will load the  training data from `train.csv` file, and the test data from `test.csv`, both included in `../data/`. The program will generate the `.csv` file that contains the result submitted in `../results/` directory.

### Testing and plotting

To run different validations, the `hyperparameters_and_plots.py`. It has to be executed from the scripts folder:
```
/scripts$ python3 hyperparameters_and_plots.py
```
The program will output the following progress updates through the standard output:

```
split_ratio=0.85, degree=3, lambda_=0.000000000, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000001, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000002, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000006, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000014, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000033, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000080, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000193, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
split_ratio=0.85, degree=3, lambda_=0.000000464, Test RMSE=0.771, Train RMSE=0.770, %test=0.79373, %train=0.79570
...
```
So, you will be able to check in the terminal the accuracy (*test%* = accuracy over the test data and *train%* = accuracy over the train data) and the RMSE (over the test data) of the different models.
Finally you will obtain the plots showing the accuracy (over the test data) of different configurations (depending on the hyperparameters `lambda` and `degree`)
