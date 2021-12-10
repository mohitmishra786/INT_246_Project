# INT_246_Project

## Image Captioning with Keras and TensorFlow

Image captioning is a new technology that combines LSTM text generation with the computer vision powers of a convolutional neural network.  I first saw this technology in Andrej Karpathy's Dissertation. [[Cite:karpathy2016connecting]](https://cs.stanford.edu/people/karpathy/main.pdf) Down Given Figure shows images from his work.

**Andrej Karpathy's Dissertation**
![Captioning](https://raw.githubusercontent.com/jeffheaton/t81_558_deep_learning/master/images/karpathy_thesis.jpg "Captioning")

In this part, we will use LSTM and CNN to create a basic image captioning system. We will use transfer learning to utilize this proje:

* [InceptionV3](https://arxiv.org/abs/1512.00567)
* [Glove](https://nlp.stanford.edu/projects/glove/)

We use inception to extract features from the images.  Glove is a set of Natural Language Processing (NLP) vectors for common words. Below Figure gives a high-level overview of captioning.


We begin by importing the needed libraries.

- For the installation of the required libraries run `pip install requirements.txt`

### Needed Data

You will need to download the following data and place it in a folder for this example.  Point the *root_captioning* string at the folder that you are using for the caption generation. This folder should have the following sub-folders.

* data - Create this directory to hold saved models.
* [glove.6B](https://nlp.stanford.edu/projects/glove/) - Glove embeddings.
* [Flicker8k_Dataset](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip) - Flicker dataset.
* [Flicker8k_Text](https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip)

Note, the original Flickr datasets are no longer available, but you can download them from a location specified by [this article](https://machinelearningmastery.com/prepare-photo-caption-dataset-training-deep-learning-model/). 
