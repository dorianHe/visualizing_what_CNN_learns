# Visualizing what CNN learns
*based on CS231n ["Visualizing and Understanding"](http://cs231n.stanford.edu/slides/2018/cs231n_2018_lecture13.pdf)*

It is very nature to think about what have the kernels in the CNN learned during the training process. The visualizing and understanding CNN plays an important role in CNN validating.

## First Layer: Visualize Filters

Visualize the kernels from the first layer. We can also visualize filters at higher layers, but not that interesting.

## Last Layer

The last layer here means the layer immediately before the classifier. So it is actually a feature vector.

### Nearest Neighbors

(from [ImageNet Classification with Deep Convolutional
Neural Networks](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf))

The idea is to show the top k-th training image that produce feature vectors with the smallest Euclidean distance from the feature vector for the test image.

### Dimensionality Reduction

(from [Visualizing Data using t-SNE](http://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf))

Visualize the space of the feature vectors b reducing the dimensionality of vectors from high dimensions to 2 dimensions using simple algorithm PCA or more complex algorithm t-SNE.

## Visualizing Activations

Visualize each feature map at some certain layer as grayscale images.

## Maximally Activating Patches

(from [Striving for Simplicity: The All Convolutional Net](https://arxiv.org/pdf/1412.6806.pdf))

1. Pick a layer and a channel; e.g. conv5 is $128*13*13$, pick the channel $17/128$
2. Run many images through the network record values of chosen channel
3. visualize image patches that correspond to maximal activations

## Which pixels matter: Saliency vs Occlusion

Mask part of the image before feeding to CNN, check how much predicted probabilities change.

*T.B.C.*