# Basleline model - This is our baseline model, on pixel info, uses CNN only.

# Purpose

To make a combined python notebook, in which we can add our model, then run it.
Currently, it uses a very simple CNN model.

# Run

### The ipynb notebook is what you can directly run.

### You can visit this colab link: https://colab.research.google.com/drive/1Gn6MFglgYsezdccKExZqGafvH7I4N4B7?usp=sharing

### Please do 'Save a copy in drive', then you can edit the new opened tab with a copy.

## Just CNN model. Trained on Google Colab using GPU. Takes 1-1.5 hours maximum.
#### Make sure to only use GPU when you need it. While simply editing code, you can turn GPU off, to save your GPU quota (exact value unspecified).

## Trained with 50% of data and tested on 50% of data.

## Accuracy 0.69/1 = 0.69%, Cohen kappa score 0.38/1 = 0.38%

## Performs much better than random. Overall, moderate performance, based on cohen kappa score. 

Confusion matrix:

non rumor, rumor

array([

[1833,  828],

[1184, 2791]
       
])

6636 test images, with 3619 of rumor and 3017 of nonrumor.

### Accurately predicted  2791/3619 = 77.12% of rumor images, and 

### 1833/3017 = 60.75% of non rumor images.

### Overall, accuracy = 4624/6636 = 69.68%.

# You only need to run the ipynb notebook.

The other files are just there for debugging how the distribution of data set occured.
