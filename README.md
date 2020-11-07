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

# Fandy's updates (updated on 4 Nov 2020)

## MVNN
Link to the trained model: https://drive.google.com/file/d/1-GnaZw9ZsYxq-2LiQtCNuBjtLwZl2T2E/view?usp=sharing

80% train, 20% validation, batch size = 32, lr = 0.0001, epoch = 6, stop at training loss < 0.1

Training time for each epoch: 5 min

```
Accuracy: 0.8220274390243902
Balanced Accuracy: 0.8182773000737064
Confusion Matrix:
 [[ 830  207]
 [ 260 1327]]
Cohen Kappa Score: 0.6309665637531666
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.76      0.80      0.78      1037
       rumor       0.87      0.84      0.85      1587

    accuracy                           0.82      2624
   macro avg       0.81      0.82      0.82      2624
weighted avg       0.82      0.82      0.82      2624
```

## MVNN without freq
Link to the trained model: https://drive.google.com/file/d/1-VN60TlFCGZLwv31CVDrY4iUvuaCklsw/view?usp=sharing

Same hyper-parameters as above, epoch = 5

Training time for each epoch: 5 min
```
Accuracy: 0.8117378048780488
Balanced Accuracy: 0.797647948915823
Confusion Matrix:
 [[ 763  286]
 [ 208 1367]]
Cohen Kappa Score: 0.6027802343746649
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.79      0.73      0.76      1049
       rumor       0.83      0.87      0.85      1575

    accuracy                           0.81      2624
   macro avg       0.81      0.80      0.80      2624
weighted avg       0.81      0.81      0.81      2624
```

## MVNN without attention
Link to the trained model: https://drive.google.com/file/d/1-PG9pKQ7TsLNzSBa1qU25-kXsU5M6H1h/view?usp=sharing

Same hyper-parameters as above, epoch = 4

Training time for each epoch: 5 min
```
Accuracy: 0.8178353658536586
Balanced Accuracy: 0.813468705193229
Confusion Matrix:
 [[ 809  210]
 [ 268 1337]]
Cohen Kappa Score: 0.6204900607507826
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.75      0.79      0.77      1019
       rumor       0.86      0.83      0.85      1605

    accuracy                           0.82      2624
   macro avg       0.81      0.81      0.81      2624
weighted avg       0.82      0.82      0.82      2624
```

## MVNN without GRU
Link to the trained model: https://drive.google.com/file/d/1-cLF3ietK0S2Ntgx9dLE1zXo6rjDTYYX/view?usp=sharing

Same hyper-parameters as above, epoch = 7

Training time for each epoch: 5 min
```
Accuracy: 0.8090701219512195
Balanced Accuracy: 0.8049089068825911
Confusion Matrix:
 [[ 833  231]
 [ 270 1290]]
Cohen Kappa Score: 0.6062849503327918
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.76      0.78      0.77      1064
       rumor       0.85      0.83      0.84      1560

    accuracy                           0.81      2624
   macro avg       0.80      0.80      0.80      2624
weighted avg       0.81      0.81      0.81      2624
```

## MVNN without branches
Link to the trained model: https://drive.google.com/file/d/1-75gl1akpCGlVcJXuemHBtzNoImWD0Aa/view?usp=sharing

Same hyper-parameters as above, epoch = 10

Training time for each epoch: 5 min
```
Accuracy: 0.8155487804878049
Balanced Accuracy: 0.8121739591869717
Confusion Matrix:
 [[ 843  218]
 [ 266 1297]]
Cohen Kappa Score: 0.6198446950444536
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.76      0.79      0.78      1061
       rumor       0.86      0.83      0.84      1563

    accuracy                           0.82      2624
   macro avg       0.81      0.81      0.81      2624
weighted avg       0.82      0.82      0.82      2624
```

# Alfred's updates

train MVNN on the twitter dataset. 

learning_rate = 0.0001 # adopt a small lr to ensure convergence

batch_size = 32

```


===== Start Validating ... =====
[Test] 2 / 2 batches tested
Accuracy: 0.703125
Balanced Accuracy: 0.6990196078431372
Confusion Matrix:
 [[26  8]
 [11 19]]
Cohen Kappa Score: 0.4003944773175543
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.70      0.76      0.73        34
       rumor       0.70      0.63      0.67        30

    accuracy                           0.70        64
   macro avg       0.70      0.70      0.70        64
weighted avg       0.70      0.70      0.70        64
```

use the  model trained from Weibo on Twitter

```
===== Start Validating ... =====
[Test] 10 / 11 batches tested
[Test] 11 / 11 batches tested
Accuracy: 0.5255681818181818
Balanced Accuracy: 0.5239664082687339
Confusion Matrix:
 [[ 78  94]
 [ 73 107]]
Cohen Kappa Score: 0.048063220624433245
Classification Report:
               precision    recall  f1-score   support

   non-rumor       0.52      0.45      0.48       172
       rumor       0.53      0.59      0.56       180

    accuracy                           0.53       352
   macro avg       0.52      0.52      0.52       352
weighted avg       0.52      0.53      0.52       352

```

# Ayush updates on 07-11-2020 -

Finalized scores of our baseline models VGG-16 and VGG-19, and Simple Sequential model of CNN have been updated in report.

## VGG-16 and VGG-19

Type of model, Precision, Recall, f1-score, Accuracy, Cohen Kappa
```
VGG-16 69%, 73% 57%,82% 62%,78% 72% 0.40

VGG-19 59%, 79% 76%,64% 66%,71% 69% 0.38
```
## Simple Sequential Model of CNN

```
Num of CNN layers, Precision, Recall, f1-score, Accuracy, Cohen Kappa
1 61%, 72% 56%,76% 59%,74% 66% 0.332
2 68%, 77% 67%,78% 68%,77% 73% 0.451
3 58%, 78% 71%,66% 64%,72% 70% 0.357
4 58%, 78% 71%,66% 64%,72% 68% 0.356

```
