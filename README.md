# Project-Automatic-Image-Captioning

<br />

In this project, I design and train a CNN-RNN (Convolutional Neural Network - Recurrent Neural Network) model for automatically generating image captions. The network is trained on the [ Microsoft Common Objects in COntext (MS COCO) dataset ](http://cocodataset.org/#home). 

<br />

**Tools : PyTorch, TorchVision, NLTK**
<br />

**Concepts : COCO Dataset, Transfer Learning, EncoderCNN/DecoderRNN, LSTMs, Feature Vectors, Word Embeddings**

<br />

The image captioning model is displayed below :

<br />

![Test Image 9](https://github.com/george-kalitsios/Project-Automatic-Image-Captioning/blob/master/Images/encoder-decoder.png)

<br />

The left half of the diagram depicts the "EncoderCNN", which encodes the critical information contained in a regular picture file into a "feature vector" of a specific size. That feature vector is fed into the "DecoderRNN" on the right half of the diagram (which is "unfolded" in time - each box labeled "LSTM" represents the same cell at a different time step). Each word appearing as output at the top is fed back to the network as input (at the bottom) in a subsequent time step, until the entire caption is generated. The arrow pointing right that connects the LSTM boxes together represents hidden state information, which represents the network's "memory", also fed back to the LSTM at each time step.

<br />
<br />

The Udacity repository for this project: [Project: Automatic Image Captioning](https://github.com/udacity/CVND---Image-Captioning-Project). 

<br />

The project will be broken up into four Python notebooks :

**Notebook 0 : Loading and Visualizing the Coco Dataset**

The Dataset notebook initializes the COCO API (the "pycocotools" library) used to access data from the MS COCO (Common Objects in Context) dataset, which is "commonly used to train and benchmark object detection, segmentation, and captioning algorithms."

**Notebook 1 : Setting up the Project and verify the Dataset and the Model**

The Preliminaries notebook uses the pycocotools, torchvision transforms, and NLTK to preprocess the images and the captions for network training. It also explores the EncoderCNN, which is taken pretrained from torchvision.models, the ResNet50 architecture.

**Notebook 2 : Training the CNN-RNN Model to predict the Caption**

In the Training notebook one finds selection of hyperparameter values and EncoderRNN training. The hyperparameter selections are explained.

**Notebook 3 : Validating the model and Do some fun with it**

The Inference notebook contains the testing of the trained networks to generate captions for additional images. No rigorous validation or accuracy measurement was performed, only sample images were generated. See below.

<br />

**Generating Image Captions , Here are some predictions from my model.**

## Good results

![Test Image 6](https://github.com/george-kalitsios/Project-Automatic-Image-Captioning/blob/master/Images/results.png)


## Not so good results

![Test Image 10](https://github.com/george-kalitsios/Project-Automatic-Image-Captioning/blob/master/Images/negativeresults.png)



