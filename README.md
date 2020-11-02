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

# Fandy's updates (updated on 31 Oct 2020)

## MVNN (Correctly tested)
Link to the trained model: https://drive.google.com/file/d/1-eXekn8r9NkkJPCN9JVUa-AB9aOMhZ9R/view?usp=sharing

80% train, 20% validation, batch size = 32, lr = 0.0001, epoch = 6, stop at training loss < 0.1

Training time for each epoch: 5 min

```
Accuracy: 0.8288871951219512
Balanced Accuracy: 0.8299214671569295
Confusion Matrix:
 [[ 876  173]
 [ 276 1299]]
Cohen Kappa Score: 0.6491986965718315
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.76      0.84      0.80      1049
       rumor       0.88      0.82      0.85      1575

    accuracy                           0.83      2624
   macro avg       0.82      0.83      0.82      2624
weighted avg       0.83      0.83      0.83      2624
```


## MVNN (may NOT be correctly tested)
Link to the trained model: https://drive.google.com/file/d/1-1Io_bGiir9Wq4cgwzkdNrVzseRYX4pa/view?usp=sharing

80% train, 20% validation, batch size = 32, lr = 0.0001, epoch = 16

Training time for each epoch: 6 min
```
Accuracy: 0.9359756097560976
Balanced Accuracy: 0.9332094990773034
Confusion Matrix:
 [[ 961   84]
 [  84 1495]]
Cohen Kappa Score: 0.866418998154607
Classification Report:
               precision    recall  f1-score   support
   non-rumor       0.92      0.92      0.92      1045
       rumor       0.95      0.95      0.95      1579
    accuracy                           0.94      2624
   macro avg       0.93      0.93      0.93      2624
weighted avg       0.94      0.94      0.94      2624
```
## MVNN without freq
Link to the trained model: https://drive.google.com/file/d/1-in0Uly1vlRHvqaI7k1PGjZIDKuKZfFV/view?usp=sharing

Same hyper-parameters as above, epoch = 5

Training time for each epoch: 5 min
```
Accuracy: 0.8166920731707317
Balanced Accuracy: 0.7944524641760105
Confusion Matrix:
 [[ 717  332]
 [ 149 1426]]
Cohen Kappa Score: 0.6065748737879089
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.83      0.68      0.75      1049
       rumor       0.81      0.91      0.86      1575

    accuracy                           0.82      2624
   macro avg       0.82      0.79      0.80      2624
weighted avg       0.82      0.82      0.81      2624
```

## MVNN without attention
Link to the trained model: https://drive.google.com/file/d/1-26f0Tfl0-EmMjYM1LaYwi2UJL4w0Mtm/view?usp=sharing

Same hyper-parameters as above, epoch = 5

Training time for each epoch: 5 min
```
Accuracy: 0.8250762195121951
Balanced Accuracy: 0.8050978255935358
Confusion Matrix:
 [[ 740  309]
 [ 150 1425]]
Cohen Kappa Score: 0.6260409176096247
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.83      0.71      0.76      1049
       rumor       0.82      0.90      0.86      1575

    accuracy                           0.83      2624
   macro avg       0.83      0.81      0.81      2624
weighted avg       0.83      0.83      0.82      2624
```

## MVNN without GRU
Link to the trained model: https://drive.google.com/file/d/1-hpX0dsww13hgqSB561O85k5yyyVq2J7/view?usp=sharing

Same hyper-parameters as above, epoch = 12

Training time for each epoch: 5 min
```
Accuracy: 0.6798780487804879
Balanced Accuracy: 0.6625827247745767
Confusion Matrix:
 [[ 605  446]
 [ 394 1179]]
Cohen Kappa Score: 0.32785696468333814
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.61      0.58      0.59      1051
       rumor       0.73      0.75      0.74      1573

    accuracy                           0.68      2624
   macro avg       0.67      0.66      0.66      2624
weighted avg       0.68      0.68      0.68      2624
```
The training accuracy can reach 97%, but the test accuracy is only 68%. This means the model is just overfitting and does not really learn the underlying pattern of fake mews images without the help of GRU.


# Alfred's updates
80% train, 20% validation, batch size = 32, lr = 0.0001, epoch = 38, layer = 2
```
===== Start Validating ... =====
  0%|          | 0/331 [00:00<?, ?it/s]CNN_BiGRU : Epoch: 38/66  Val Loss: 0.020262  Val Accuracy: 79.283019
Accuracy: 0.8006859756097561
Balanced Accuracy: 0.7888929053402738
Confusion Matrix:
 [[ 773  291]
 [ 232 1328]]
Cohen Kappa Score: 0.5829244691248766
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.77      0.73      0.75      1064
       rumor       0.82      0.85      0.84      1560

    accuracy                           0.80      2624
   macro avg       0.79      0.79      0.79      2624
weighted avg       0.80      0.80      0.80      2624
```
train on the twitter dataset. 
learning_rate = 0.0001 # adopt a small lr to ensure convergence
batch_size = 32

```

===== Start Validating ... =====
[Test] [Epoch 15] 2 / 2 batches tested. Test Loss: 0.957414
Accuracy: 0.671875
Balanced Accuracy: 0.6691104594330402
Confusion Matrix:
 [[25  8]
 [13 18]]
Cohen Kappa Score: 0.3398821218074656
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.66      0.76      0.70        33
       rumor       0.69      0.58      0.63        31

    accuracy                           0.67        64
   macro avg       0.68      0.67      0.67        64
weighted avg       0.67      0.67      0.67        64


MVNN_wout_freq: [Epoch 16] [Iter 1/9] Loss: 0.113392  Acc: 1.000000
Training:  Avg Loss = 0.113392, Avg Acc = 1.000000
Training Time:      0.128 mins
MVNN_wout_freq: [Epoch 17] [Iter 1/9] Loss: 0.092333  Acc: 1.000000
Training:  Avg Loss = 0.092333, Avg Acc = 1.000000
Training Time:      0.128 mins
Training is stopped at [Epoch 17] as loss is already very low (0.092333)!

===== Finished Training & Validating =====
```
