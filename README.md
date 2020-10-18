# COMP_5331_Project_Fake_News_Detection

## Folders

### Fully_trained_classifier

### Temporary_models

# Good Github practices 

#### Use Readme folder to post updates, it allows easier collaboration, to learn what each code does

# Ayush updates -

## Pytorch_Attention_COMP_5331_Ayush.ipynb

Added basic code of Fusion sub network, exact depends on Pixel and Frequency domain. Please refer to the additional links provided to better understand how to integrate it. This one was initially designed for RNN, for seq2seq modeling.

Let me know if you encounter any difficulties.

## Fully_trained_classifier

### Only_CNN - by Ayush on Pixel info
#### Data distribution - 50% for training, 50% for testing
#### Scores - 69% Overall accuracy, 77% on rumor set, 60% on non rumor set. Cohen kappa score of 0.38 = Moderate performonace against random classifier.
#### Colab notebook link: Please 1st save a copy in drive then edit:

### Others
#### VGG16 - Accuracy: 0.726, Cohen kappa = 0.406
#### VGG19 - Accuracy: 0.724, Cohen kappa = 0.424
#### [Need Refactor] Inception V3 - Accuracy: 0.630, Cohen kappa = 0.224

###### https://colab.research.google.com/drive/1Gn6MFglgYsezdccKExZqGafvH7I4N4B7?usp=sharing

# AG's updates

## Frequency
### 60% accuracy in frequency domain
