# hierarchical-sexism-detection-SemEval-23-Task7

### Step 1: Check conda installation

You need anaconda or miniconda installed. Run 'which conda' (Linux/Mac platform) or 'where conda' (Windows platform) to check whether conda is installed or not.
You can install miniconda using following commands -
```
mkdir -p ./miniconda3

wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ./miniconda3/miniconda.sh

bash ./miniconda3/miniconda.sh -b -u -p ./miniconda3

rm -rf ./miniconda3/miniconda.sh

./miniconda3/bin/conda init bash

./miniconda3/bin/conda init zsh
```

More details [here](https://docs.conda.io/en/latest/miniconda.html)

### Step 2: Installing dependancies

The 'semeval_10.yaml' has listed all the dependancies required by all the models. Run the below command to create a conda environment and activate it by
```
conda env create -n semeval_10.yaml

conda activate semeval_10
```
### Step 3: Running Model1-ML

Run jupyter notebook using command - juputer notebook

It contains the Logistic regression, Decison Tree, Xgboost, Random Forest models.
The training data is present in the 'data' folder and classification report will be saved in the 'result' folder.
You need to run the 'semeval_10_ML.ipynb' file.

### Step 4: Running Model2-MLP

We use the jupyter notebook to run this code. It contains the MLP model developed of TFIDF features. The each Task A, B, C is trained independently using same model architecture. 
The training data is present in the 'data' folder and classification report, loss curve, confusion matrix will be saved in the 'result' folder.
You need to run 'semeval_10_MLP.ipynb' file.

### Step 5: Running Model3-BiLSTM

We use the jupyter notebook to run this code. It contains the BiLSTM model. It uses golve embeddings. The embedding file will be downloaded on the runtime. Since the file size in the GB, it might take a while to
run this model for the first time. If you already have the 'glove.6B.300d.txt' file, you may capy it the 'glove' folder to reduce the execution speed.
The training data is present in the 'data' folder and classification report, confusion matrix will be saved in the 'result' folder.
You need to run 'semeval_10_BiLSTM.ipynb' file.

### Step 6: Running Model4-HAM

Stop the jupyter notebook. This model has .py file which will be run through a terminal.

This folder contains the Hierarchical Attention Model. The training data (csv files) is present inside the 'data' folder. The tsv file are genereted by this
code and used as intermediatary supporting files. 
The 'log' folder contains the running status of the code. All the info and error logs are added in the 'model_log.txt' file.
The classification report, trained model, loss curve will be saved in the 'result' folder.
The 'utils' conatins the data loading and preprocessing part.
You can change the model parameter and they are located in the main() function of the 'train.py' file. You should only change the params present in the
'YOU MAY EDIT THE BELOW PARAM' section.
You need to run the 'train.py' file.
```
python ./Model4-HAM/train.py
```
