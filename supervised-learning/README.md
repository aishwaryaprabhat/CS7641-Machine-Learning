# How to run the code

## 1. Setting up environment
- Clone the code repository using `git clone https://github.com/aishwaryaprabhat/CS7641-Machine-Learning.git`
- Navigate to the `supervised-learning` directory using `cd CS7641-Machine-Learing/supervised-learning`
- Install conda (refer to https://conda.io/projects/conda/en/latest/user-guide/install/index.html for instructions)
- Set up virtual environment
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
- Your file structure should look something like this:
```
.
├── Classification on MoCap Dataset.ipynb
├── Classification on Parkinson's Disease Dataset.ipynb
├── README.md
├── conda_env.yml
├── data
│   ├── Postures.csv
│   ├── Postures.zip
│   ├── archive.zip
│   ├── mocap_experiments
│   ├── pd_experiments
│   └── pd_speech_features.csv
├── docs
├── images
└── requirements.txt
```


## 3. Re-running Experiments
### 3.1 Running the code
- Ensure that you complete the setup in section 1 and 2 correctly.
- From the `CS7641-Machine-Learing/supervised-learning` directory launch Jupyter using the command `jupyter notebook`
- Open `Classification on MoCap Dataset.ipynb` and `Classification on Parkinson's Disease Dataset.ipynb` for running the code for their respective datasets
- To run the code, execute the cells in order 

### 3.2 Mlflow-specific instructions (optional)
Parts of the code in the jupyter notebook log metrics and parameters to mlflow. These were then used to create parallel coordinate plots that were added to the report. This logging and plotting was particularly useful for hyperparameter tuning. If you would like to review the experiment results, you follow one of the following approaches:

#### 3.2.1 Logging using the jupyter notebooks and viewing on MLflow UI
- If the conda environment, data and notebook are setup correctly, you can just run the cells in the notebook that are logging to mlflow
- If you are in the `CS7641-Machine-Learing/supervised-learning` directory, you should see the directory `mlruns`
- On your CLI, navigate to the `CS7641-Machine-Learing/supervised-learning` directory and run the command `mlflow ui`
- On your browser, on http://localhost:5000 you should be able to see the MLflow UI
- Use the UI to navigate through the experiment results

#### 3.2.2 Downloading original mlruns
- Alternatively, you can download `mlruns.zip` from https://drive.google.com/file/d/1Jj4NNOnMf420EEaL6ZV8B4QQWsXtEiCp/view?usp=sharing 
- Unzip the `mlruns.zip` file in any directory
- On your CLI, navigate to the directory you unzipped the file to and run `mlflow ui` command to launch the UI
- On your browser, on http://localhost:5000 you should be able to see the MLflow UI
- Use the UI to navigate through the experiment results

#### 3.2.3 Perusing the results logged as a csv file
- You can find the experiment metrics and parameters logged as csv files in the `data` directory
- For the MoCap dataset, the experiment logs can be found in `data/mocap_experiments`
- For the Parkinson's Disease dataset, the experiment logs can be found in `data/pd_experiments`

## 4. References
- https://www.datacamp.com/community/tutorials/decision-tree-classification-python
- https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html
- https://scikit-learn.org/stable/auto_examples/model_selection/plot_learning_curve.html#sphx-glr-auto-examples-model-selection-plot-learning-curve-py