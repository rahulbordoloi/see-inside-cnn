# see-inside-cnn
Going deeper into CNNs through visualization methods: 
- Saliency maps 
- Optimize random image wrt neuron
- Optimize random image wrt activations content 
- Deep Dream
- GAP visualization

---

## 01 Saliency maps

Saliency maps method is based on the main idea of the well known paper: [Deep Inside Convolutional Networks](https://arxiv.org/abs/1312.6034): Visualising Image Classification Models and Saliency Maps, Where we address the task knowing where in the input are the important pixels that influence the output.

![sm01](images/sm01.png)

## 02 optimize image wrt neuron

This is an interesting approach that tells us what kind of input excites a neuron or a set of neurons. Neurons learn to be feature detectors, and they get excited when a feature is found in the input. Usually, layers near the input are excited by basic or low level features (lines, curves, textures, colors), while deep layers are excited by high level feature (objects: faces, vehicles, animals).

![sm01](images/owrtn.gif)

## 03 optimize image wrt content

The basic idea to trying to get an image that produce almost the same activations of another image. In other words, both images are almost the same in the eyes of the neural network.

![owrtc01](images/owrtc03.png)

## 04 deep dream

Similar to when we look at the clouds and tries to interpret shapes that we know, DeepDream also interprets and enhances the patterns it sees in an image.

![dd](images/dd01.png)


## 05 gap visualization

In a classification scenario, if we design the network architecture so that the final convolution consists of filters equal to the number of classes, this will force the final convolutional filters to find out how each part of the image related to each class. Moreover, we can visualize the activations as a heatmap over the input image.

After this final convolution layer, global average pooling is applied across number of convolution features equal to number of classes, which results in a vector of values that we can then use to classify the input image.

![gap](images/gap01.png)

