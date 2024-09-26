# PyTorch Style Transfer for image and video generation 

via a content image, style image and random noise of target image which will be the output image

### image demo
![hidden text](/images/output.png)

### Video Demo
![hidden text](/video/output.gif)


# Illustration
1) Training: We train a CNN model on cifar input images
2) Input features: 3*28*28 (RGB channels, width, heigth)
3) Output targets: ['T-shirt/top', 'Trouser', 'Pullover', 'Dress', 'Coat', 'Sandal', 'Shirt', 'Sneaker', 'Bag', 'Ankle boot']

# Model & Architecture
1) CNN DL Model
2) 3 convolution layers + batchnorm + leaky_relu
3) CNN img size 28 -> 13 ->  5  -> 1
4) CNN Kernels  1  -> 64 -> 128 -> 256
5) Linear layer + leaky_relu + dropout 0.5
6) inChans  = 1 # RGB => should be changed to 1
7) outChans = 64 # of feature maps / kernels
8) krnSize  = 3x3 # odd number
9) padding  = 0 # No padding
10) stride   = 1 # used stride
11) batchnorm = 1
12) Use of CrossEntropyLoss for classification of 10 targets
13) Minibatches = 32
14) Adam Optimizer with weight decay of 1e-4

# Results
1) Accuracy: Got 99% train accuracy and 91% test accuracy for the prediction of the fashion of the dataset "overfit with 8%"
    
# Conclusions:
1) Need to finetune the metaparameters and see what can increase the results of the test accuracy
