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

## VGG_16_VGG_19_Ayush_and_Chiu.ipynb (in the Baseline->Baselines folder)

The source notebook for training and validating the Baseline models of VGG-16, VGG-19 and Inception_v3. These are popular pre-trained models in the field of Deep learning for Image classification. The VGG-16 and VGG-19 were originally used in ImageNet data set, here we tuned them on the Weibo data set. We use an 80% training and 20% testing split. We also use Early stopper as well as learning rate reducer if there is almost no progress in training. Rumor means fake news, Non rumor means real news. Regarding the data, we perform shuffling before splitting the data set, this ensures that we can get a balance of both the classes of rumor and non rumor. At the end of the code you can see the score from metrics we used and the results of these 3 models.

## 1_Conv_layers_Ayush.ipynb, 2_Conv_layers_Ayush.ipynb, 3_Conv_layers_Ayush.ipynb, 4_Conv_layers_Ayush.ipynb (in the Baseline->Sequential_of_CNN then in 1_layers, 2_layers, 3_layers and 4_layers folders)


The source notebooks for training and validating the Sequential models of CNN with different number of Conv2D layers, such as 1,2,3 and 4, present in folders 1_layers, 2_layers, 3_layers and 4_layers. These models are implemented by us, and are a simplified version of the VGG-16 and VGG-19. We use an 80% training and 20% testing split. We also use Early stopper as well as learning rate reducer if there is almost no progress in training. Rumor means fake news, Non rumor means real news. Regarding the data, we perform shuffling before splitting the data set, this ensures that we can get a balance of both the classes of rumor and non rumor. At the end of the code you can see the score from metrics we used and the results of the corresponding models.


# 4. An example to show how to run the program
- Run MVNN_training_validation.ipynb directly, it will first load the necessary packages, then requires for google drive permission to mount the google drive (since we want to save the trained model on the drive). Then, it will start downloading the Weibo dataset. Later we load all the python classes. With the default hyper-parameters and selection of model, the training starts with GPU by running the code block under the "Let's Start Training" Section. The validation will be run whilst the training. After training, it will plot the training graph and save the trained model on the mounted google drive. A validation process is also given in the last code block.

- The procedure to run Run MVNN_prediction_new_set.ipynb is basically the same, except that it directly downloads the trained MVNN model (there are 6 models) and performs prediction on a completely new set (i.e., Twitter dataset).

# 5. the operating system you tested your program
The program is tested on Google Colab

# 6. others
Use GPU as the training needs GPU.
Training time is generally within 30 minutes to 90 minutes, while using a Google Colab GPU.

Here is a useful guide: https://colab.research.google.com/drive/1P7okDVh6viCIOkii6UAF2O9sTAcKGNWq
