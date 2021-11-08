# How to run the code

## 1. Setting up environment
- Clone the code repository using `git clone https://github.com/aishwaryaprabhat/CS7641-Machine-Learning.git`
- Navigate to the `random-optimization` directory using `cd CS7641-Machine-Learing/random-optimization`
- Install conda (refer to https://conda.io/projects/conda/en/latest/user-guide/install/index.html for instructions)
- Set up and activate the virtual environment using:
```
conda env create -f conda_env.yml
conda activate cs7641
```

## 2. Downloading data
### 2.1 MoCap Dataset
- Download `Postures.zip` from https://archive.ics.uci.edu/ml/machine-learning-databases/00405/ into the `data` directory
- Navigate to the `data` directory and unzip the `Postures.zip` file. You may use the following commands:
```
cd data
unzip Postures.zip
```
- You may choose to remove the .zip file using `rm Postures.zip`

### 2.2 Parkinson's Disease Dataset
- Navigate to https://www.kaggle.com/dipayanbiswas/parkinsons-disease-speech-signal-features and click on "Download"
- Save the `archive.zip` file in the `data` directory
- Navigate to the `data` directory and unzip the `archive.zip` file. You may use the following commands:
```
cd data
unzip archive.zip
```
- You may choose to remove the .zip file using `rm archive.zip`


## 3. Re-running Experiments
### 3.1 Running the code
- Ensure that you complete the setup in section 1 and 2 correctly
- From the `CS7641-Machine-Learing/random-optimization` directory launch Jupyter using the command `jupyter notebook`
- Open each notebook for the respective optimization problems
- To run the code, execute the cells in order 

## 4. References
- https://www.datacamp.com/community/tutorials/decision-tree-classification-python
- https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html
- https://scikit-learn.org/stable/auto_examples/model_selection/plot_learning_curve.html#sphx-glr-auto-examples-model-selection-plot-learning-curve-py
- https://github.com/hiive/mlrose
- https://mlrose.readthedocs.io/en/stable/