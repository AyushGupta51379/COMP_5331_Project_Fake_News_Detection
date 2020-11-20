# 2 folders - BASELINE and MVNN

### Baseline folder contains Baselines models of VGG16,VGG19 and the Sequential models of CNN.

### MVNN folder contains MVNN model and its different variations.

# 1 & 2. How to compile & run the code?
The source codes are all Python notebooks. Run the codes via Jupyter notebook or via Google Colab.

# 3. The description of each source file
## MVNN_training_validation.ipynb (in the MVNN folder): 
The source notebook for training and validating the MVNN models. There are in total 6 models: MVNN, MVNN_wout_freq (i.e., MVNN without the frequency subnetwork), MVNN_wout_pixel (MVNN without the pixel subnetwork), MVNN_wout_att (MVNN without attention mechanism), MVNN_wout_GRU (MVNN without GRUs in the pixel subnetwork), MVNN_wout_branches (MVNN without branches in the pixel subnetwork). The model can be selected by modifying the "modelname" variable under the "Hyper-parameters" Section.

## MVNN_prediction_new_set.ipynb (in the MVNN folder): 
The source notebook for loading the trained MVNN models to predict a new set (i.e. Twitter dataset).


# 4. An example to show how to run the program
- Run MVNN_training_validation.ipynb directly, it will first load the necessary packages, then requires for google drive permission to mount the google drive (since we want to save the trained model on the drive). Then, it will start downloading the Weibo dataset. Later we load all the python classes. With the default hyper-parameters and selection of model, the training starts with GPU by running the code block under the "Let's Start Training" Section. The validation will be run whilst the training. After training, it will plot the training graph and save the trained model on the mounted google drive. A validation process is also given in the last code block.

- The procedure to run Run MVNN_prediction_new_set.ipynb is basically the same, except that it directly downloads the trained MVNN model (there are 6 models) and performs prediction on a completely new set (i.e., Twitter dataset).

# 5. the operating system you tested your program
The program is tested on Google Colab

# 6. others
N/A
