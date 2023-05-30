# Analysis of Minimal Constraints for EDF Schedulability

## How to use
This repository makes use of Jupyter Notebooks to provide a more interactive experience. 

If you want to run the code without having already prepared the proper Python environment , you can do so by clicking on the Colab badge below. This will open a Jupyter Notebook in your browser. You can then run the code by clicking on the "Run" button in the toolbar. The code will be executed and the output will be displayed below the cell.

[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jannhs/edf_hull)

If you want to run the code locally, you can do so by installing the required dependencies and running the notebook. The required dependencies are listed in the `requirements.txt` file. You can install them by running the following command in your terminal:

```bash
pip install -r requirements.txt
```

## Libraries

The core Python libraries we will be using are:

* **[NumPy](https://numpy.org/)**: the fundamental package for **scientific calculation** in Python, useful when inserting any type of mathematical operation in the code;
* **[Pandas](https://pandas.pydata.org/)**: a library for **data manipulation and analysis**, extensively used for importing and managing the datasets;
* **[Matplotlib](https://matplotlib.org/)**: a Python **2D plotting library**, used to plot any type of charts in Python.


Additional libraries for data visualization are:
* **[Seaborn](https://seaborn.pydata.org/)**: a library build on top of Matplotlib that offers choices for plot style and color defaults;
* **[Plotly](https://plotly.com)**: expecially apt if the visualization needs to be dynamic and published on the web.

Additional libraries for data analysis are:
* **[Sklearn](https://scikit-learn.org/stable/)**: a library that makes available many tools for **preprocessing data**.

All these libraries are already available in the [Anaconda](https://www.anaconda.com/) distribution. Or you can install them with [pip](https://packaging.python.org/en/latest/tutorials/installing-packages/).


Once all the required libraries are ready, you have one of two choices: 
* create and later analyze a customized dataset (--> go to the [Data collection](./data_collection.ipynb) notebook) 
* analyze [datasets already available](../datasets/) (--> go to the [Data analysis](./data_analysis.ipynb) notebook)

## Data collection
The [Data collection](./data_collection.ipynb) notebook is used to create a customized dataset. It is composed of three main sections:
1. **Data generation**: the user can generate a dataset by specifying the number of tasks, the number of cores, the utilization factor and the number of tasks per core. The dataset is then saved in the [datasets](../datasets/new) folder.
1. **Data subset**: the data just generated is then filtered to create a subset of interest for us. The subset is saved in the csv file [selected](../datasets/selected.csv).
1. **Task-set specific data**: all task-sets from the subset are then re-run through the `edf_hull` procedure. The result will be as many csv files as the number of task-sets in the subset. All files are saved in the [datasets](../datasets/additional_info/) folder.

## Data analysis
The [Data analysis](./data_analysis.ipynb) notebook is used to analyze the datasets already available. 

