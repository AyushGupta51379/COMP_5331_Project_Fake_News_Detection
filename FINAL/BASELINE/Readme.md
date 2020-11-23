# Here are our Baseline models and Sequential model of CNN

### VGG16, VGG19 and InceptionV3 are in Baselines Folder

Contains source notebook for training and validating the Baseline models of VGG-16, VGG-19 and Inception_v3. These are popular pre-trained models in the field of Deep learning for Image classification. The VGG-16 and VGG-19 were originally used in ImageNet data set, here we tuned them on the Weibo data set. We use an 80% training and 20% testing split. We also use Early stopper as well as learning rate reducer if there is almost no progress in training. Rumor means fake news, Non rumor means real news. Regarding the data, we perform shuffling before splitting the data set, this ensures that we can get a balance of both the classes of rumor and non rumor. At the end of the code you can see the score from metrics we used and the results of these 3 models.

### Sequential models of CNN are in Sequential_of_CNN Folder, models with different number of CNN layers such as 1,2,3,4

Contains the source notebooks for training and validating the Sequential models of CNN with different number of Conv2D layers, such as 1,2,3 and 4, present in folders 1_layers, 2_layers, 3_layers and 4_layers. These models are implemented by us, and are a simplified version of the VGG-16 and VGG-19. We use an 80% training and 20% testing split. We also use Early stopper as well as learning rate reducer if there is almost no progress in training. Rumor means fake news, Non rumor means real news. Regarding the data, we perform shuffling before splitting the data set, this ensures that we can get a balance of both the classes of rumor and non rumor. At the end of the code you can see the score from metrics we used and the results of the corresponding models.

# How to run the code?

### They are all Python notebooks: Run via Jupyter notebook or by Uploading to Google Colab.

The codes will use internet, publically available Image data set. You do not need to worry about it. Just run the code, on a GPU. 

Since they are already interactive notebooks, you can easily see their code with outputs.

### Use GPU as the training needs GPU.

Training time is generally within 30 minutes to 90 minutes, while using a Google Colab GPU.

Here is a useful guide: https://colab.research.google.com/drive/1P7okDVh6viCIOkii6UAF2O9sTAcKGNWq

