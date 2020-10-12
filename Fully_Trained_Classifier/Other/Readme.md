# Classifiers other than MVNN type as in paper

# VGG-16, VGG-19, Inception V3 - Added by AG (Chiu Wai), slightly modified by Ayush

## Version 1 by Chiu Wai
vgg16-19-inception_v3.ipynb

## Version 2 by Ayush - just adding more metrics and making the history of all 3 models visible
V2_vgg16-19-inception_v3.ipynb

## Train and Test

### 6636 images for Train (including validation)

### 6636 images for Testing

#### Non rumor - 2661 images (40% of total testing)
#### Rumor - 3975 images (60% of total testing)
### Images data generator is used for both training and testing
### Keras code, not pytorch

### Scores:

#### VGG-16

Accuracy: 0.7276974080771549

Balanced Accuracy: 0.7140075017903611

Confusion Matrix:

[[1716  945]

[ 862 3113]]

Cohen Kappa Score: 0.43023302224168447

Classification Report:

precision    recall  f1-score   support


class 0       0.67      0.64      0.66      2661

class 1       0.77      0.78      0.78      3975


accuracy                           0.73      6636

macro avg       0.72      0.71      0.72      6636

weighted avg       0.73      0.73      0.73      6636

#### VGG-19

Accuracy: 0.7233273056057866

Balanced Accuracy: 0.6911046350854055

Confusion Matrix:

[[1406 1255]

[ 581 3394]]

Cohen Kappa Score: 0.39890930694546445

Classification Report:

precision    recall  f1-score   support


class 0       0.71      0.53      0.60      2661

class 1       0.73      0.85      0.79      3975


accuracy                           0.72      6636

macro avg       0.72      0.69      0.70      6636

weighted avg       0.72      0.72      0.71      6636

#### Inception_V3

Accuracy: 0.6107594936708861

Balanced Accuracy: 0.6248448235519346

Confusion Matrix:

[[1852  809]

[1774 2201]]

Cohen Kappa Score: 0.23556979096426167

Classification Report:

precision    recall  f1-score   support

class 0       0.51      0.70      0.59      2661

class 1       0.73      0.55      0.63      3975

accuracy                           0.61      6636

macro avg       0.62      0.62      0.61      6636

weighted avg       0.64      0.61      0.61      6636
