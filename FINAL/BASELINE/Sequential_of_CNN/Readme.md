# Here are our Sequential models of different number of CNN layers (1,2,3,4)
The source notebook for training and validating the Sequential models of CNN with different number of Conv2D layers, such as 1,2,3 and 4, present in folders 1_layers, 2_layers, 3_layers and 4_layers. These models are implemented by us, and are a simplified version of the VGG-16 and VGG-19. We use an 80% training and 20% testing split. We also use Early stopper as well as learning rate reducer if there is almost no progress in training. Rumor means fake news, Non rumor means real news. Regarding the data, we perform shuffling before splitting the data set, this ensures that we can get a balance of both the classes of rumor and non rumor. At the end of the code you can see the score from metrics we used and the results of these 3 models.

# Different folders represent different number of CNN layers in the model.

### We experimented with number of CNN layers = 1,2,3,4.

The codes are present in their respective folders of 1_layers for 1 Conv2D, 2_layers for 2 Conv2D, 3_layers for 3 Conv2D and 4_layers for 4 Conv2D. Comments have been provided in the code to make it easier to understand.

# How to run the code?

### They are all Python notebooks: Run via Jupyter notebook or by Uploading to Google Colab.

The codes will use internet, publically available Image data set. You do not need to worry about it. Just run the code, on a GPU. 

Since they are already interactive notebooks, you can easily see their code with outputs.

### Use GPU as the training needs GPU.

Training time is generally within 30 minutes to 90 minutes, while using a Google Colab GPU.

Here is a useful guide: https://colab.research.google.com/drive/1P7okDVh6viCIOkii6UAF2O9sTAcKGNWq

