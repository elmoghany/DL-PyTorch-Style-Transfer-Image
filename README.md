# PyTorch Style Transfer for image and video generation 

via a content image, style image and random noise of target image which will be the output image

### Image demo
![hidden text](/images/output.png)

### Video Demo
![hidden text](/video/output.gif)


# Illustration
1) Use VGG pretrained model
2) Input Content Image
3) Input Style Image
4) Output Target Image from random noise start point

# Model & Architecture
1) VGG19 Pre-trained model
2) modelLayersFeatureMaps function to extract the features in each convolution layer
3) gram_matrix function to calculate the gram matrix of the style at each convolution layer
4) contentLayers       = [ 'ConvLayer_4' ]
5) weightContentLayers = 1 #alpha
6) styleLayersWeight = {
    'ConvLayer_1': 1,
    'ConvLayer_2': 0.8,
    'ConvLayer_3': 0.5,
    'ConvLayer_4': 0.3,
    'ConvLayer_5': 0.1
5) styleScaling    = 1e6
6) Recommended: epochs = 10,000
7) Using VideoWriter to create the video out of frames saved during creation of the target image
     
# Conclusions:
1) There are many parameters to play with and to compare in order to get better results
