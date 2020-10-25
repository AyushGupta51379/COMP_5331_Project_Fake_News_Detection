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

## Frequent Domain Subnetwork

Here is the freq subnetwork that gives the best result so far

```
Accuracy: 0.7181132075471698
Balanced Accuracy: 0.699630584151476
Confusion Matrix:
 [[ 640  406]
 [ 341 1263]]
Cohen Kappa Score: 0.4036238987882377
Classification Report:
               precision    recall  f1-score   support

     class 0       0.65      0.61      0.63      1046
     class 1       0.76      0.79      0.77      1604

    accuracy                           0.72      2650
   macro avg       0.70      0.70      0.70      2650
weighted avg       0.72      0.72      0.72      2650
```

## MVNN Prototype

I have created a prototype of MVNN, combining all things together. \\
For details, see `MVNN_prototype.ipynb`.

A quick run generates the following result:

```
Accuracy: 0.6806026365348399
Balanced Accuracy: 0.668415730628062
Confusion Matrix:
 [[ 650  426]
 [ 422 1157]]
Cohen Kappa Score: 0.3370310212379519
```

Not bad, it is believed to further improve after the pixel subnetwork is stable.

# Fandy's updates

## Pixel subnetwork (CNN without GRU)
80% train, 20% validation, batch size = 64, lr = 0.01, epoch = 11

Training time for each epoch: 2min
```
Accuracy: 0.8227896341463414
Balanced Accuracy: 0.7972461356455833
Confusion Matrix:
 [[ 699  332]
 [ 133 1460]]
Cohen Kappa Score: 0.6154466789035238
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.84      0.68      0.75      1031
       rumor       0.81      0.92      0.86      1593

    accuracy                           0.82      2624
   macro avg       0.83      0.80      0.81      2624
weighted avg       0.82      0.82      0.82      2624
```

## Pixel subnetwork (CNN with GRU, m = 2)
80% train, 20% validation, batch size = 32, lr = 0.0001, epoch = 10

Training time for each epoch: 2min
```
Accuracy: 0.8250762195121951
Balanced Accuracy: 0.8188904985138463
Confusion Matrix:
 [[ 846  233]
 [ 226 1319]]
Cohen Kappa Score: 0.63840559521179
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.79      0.78      0.79      1079
       rumor       0.85      0.85      0.85      1545

    accuracy                           0.83      2624
   macro avg       0.82      0.82      0.82      2624
weighted avg       0.82      0.83      0.82      2624
```
The GRU model is working now, with batch norm layers added and a very small learning rate of 0.0001.


## Pixel subnetwork (CNN with Bi-GRU, m = 1)
80% train, 20% validation, batch size = 32, lr = 0.0001, epoch = 63

Training time for each epoch: 2min
```
Accuracy: 0.8216463414634146
Balanced Accuracy: 0.8070327613666015
Confusion Matrix:
 [[ 782  297]
 [ 171 1374]]
Cohen Kappa Score: 0.6250735026076253
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.82      0.72      0.77      1079
       rumor       0.82      0.89      0.85      1545

    accuracy                           0.82      2624
   macro avg       0.82      0.81      0.81      2624
weighted avg       0.82      0.82      0.82      2624
```
The simpler Bi-GRU model is somehow much harder to train. I suggest use the original GRU model (m = 2).

