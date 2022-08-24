# Obtaining a Heat Map of the areas most influential in sorting chest X-ray images.
## The study focuses on the two most similar types (Covid - Pneumonia).


The neural network is based on the idea of ​​giving each of the factors that are considered an input to the neural network specific weights, and therefore, during the training phase of the neural network, the weights are adjusted through the loss function and the optimization follower used.
In convolutional neural networks, in each of the layers it is stacked using convoluation and pooling layers, and thus the goal is to get a feature map and finally through Perceptron layers the weights are modified for each feature map and thus we will benefit from the weights that were reached at the end Training from the last layer, in addition to making use of the last conv2D layer within the proposed neural network.

### The steps for extracting a heat map for X-ray images are summarized as follows:
- Proposing a convolutional neuron structure to classify two types of X-ray images (Covid, pneumonia).
- Training the proposed neural network and reaching the highest possible accuracy.
- Experimentation on a single image to reach (image rating prediction).
- Obtaining the weights through which the required classification was reached.
- Get the last feature map that precedes the classification layer (I'll explain this step in detail in Notebook).
- Try to expand the feature map to be in the form of (224, 224) and at this stage it can be expanded to the size you want.
- Multiply the feature map matrix after expansion with the matrix of weights obtained from the previous steps. (In this stage, we determine the values ​​of the most important pixels that the neural network will rely on during the classification process) (ie, at this stage we determine the feature map values ​​that have the highest weights).
- In the last stage, we will display the feature map image after expanding and multiplying it by the weights values, as well as showing the base image that has the same dimensions as the first image.

![download (57)](https://user-images.githubusercontent.com/108609519/186397736-ea5eec61-bdd1-459b-be8c-cd0b6e2b0ffa.png)

![download (58)](https://user-images.githubusercontent.com/108609519/186397808-0effe2fd-7725-411d-b012-4db6e6257c82.png)
