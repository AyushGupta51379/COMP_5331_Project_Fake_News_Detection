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

#### VGG-16 - 72.8% accuracy, 0.43 cohen kappa score

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

#### VGG-19 - 72.3% accuracy, 0.398 cohen kappa score

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

#### Inception_V3 - 61% accuracy, 0.235 cohen kappa score

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

# Final version (V4) by Ayush


## VGG-16

Accuracy: 0.7182674199623352

Balanced Accuracy: 0.6948781482626445

Confusion Matrix:

[[ 615  466]

[ 282 1292]]

Cohen Kappa Score: 0.4004303989160324

Classification Report:

precision    recall  f1-score   support


class 0       0.69      0.57      0.62      1081

class 1       0.73      0.82      0.78      1574


accuracy                           0.72      2655

macro avg       0.71      0.69      0.70      2655

weighted avg       0.71      0.72      0.71      2655

## VGG-19

Accuracy: 0.688512241054614

Balanced Accuracy: 0.6991920042033648

Confusion Matrix:

[[ 818  263]

[ 564 1010]]

Cohen Kappa Score: 0.38173769584282846

Classification Report:

precision    recall  f1-score   support


class 0       0.59      0.76      0.66      1081

class 1       0.79      0.64      0.71      1574

accuracy                           0.69      2655

macro avg       0.69      0.70      0.69      2655

weighted avg       0.71      0.69      0.69      2655

## Inception-v3

### Removed due to some weird issues - it did not learn anything

Accuracy: 0.5928436911487759

Balanced Accuracy: 0.5

Confusion Matrix:

[[   0 1081]

[   0 1574]]

Cohen Kappa Score: 0.0

Classification Report:

precision    recall  f1-score   support


class 0       0.00      0.00      0.00      1081

class 1       0.59      1.00      0.74      1574


accuracy                           0.59      2655

macro avg       0.30      0.50      0.37      2655

weighted avg       0.35      0.59      0.44      2655

/usr/local/lib/python3.6/dist-packages/sklearn/metrics/_classification.py:1272: UndefinedMetricWarning: Precision and F-score are ill-defined and being set to 0.0 in labels with no predicted samples. Use `zero_division` parameter to control this behavior.
  _warn_prf(average, modifier, msg_start, len(result))
