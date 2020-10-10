# Purpose

To make a combined python notebook, in which we can add our model, then run it.
Currently, it uses a very simple CNN model.

# Run
The ipynb notebook is what you can directly run.

# Just CNN model. Trained on Google Colab using GPU. Takes 1-1.5 hours maximum.

# Trained with 50% of data and tested on 50% of data.

# Accuracy 0.69/1 = 0.69%, Cohen kappa score 0.38/1 = 0.38%

# Performs better than random.

Confusion matrix:

non rumor, rumor

array([

[1833,  828],

[1184, 2791]
       
])

6636 test images, with 3619 of rumor and 3017 of nonrumor.

Accurately predicted 
2791/3619 = 77.12% of rumor images,

and 

1833/3017 = 60.75% of non rumor images.

Overall, accuracy = 4624/6636 = 69.68%.
