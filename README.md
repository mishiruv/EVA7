# EVA5
## Assignment 4

The data set is MNISt which is small se of images 28X28. so we don't need large no of channels to convolve through the imgae

The Architecure has 3 blocks of convolution layers each having 2 sets of convolution followed by activation, batch normnalisation and maxpooling and dropout
The no of parameters are 17000+ with batch size of 128 and 20 epochs.

Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [-1, 8, 28, 28]              80
            Conv2d-2           [-1, 16, 28, 28]           1,168
              ReLU-3           [-1, 16, 28, 28]               0
       BatchNorm2d-4           [-1, 16, 28, 28]              32
         MaxPool2d-5           [-1, 16, 14, 14]               0
           Dropout-6           [-1, 16, 14, 14]               0
            Conv2d-7           [-1, 32, 14, 14]           4,640
              ReLU-8           [-1, 32, 14, 14]               0
       BatchNorm2d-9           [-1, 32, 14, 14]              64
           Conv2d-10            [-1, 8, 14, 14]           2,312
             ReLU-11            [-1, 8, 14, 14]               0
      BatchNorm2d-12            [-1, 8, 14, 14]              16
        MaxPool2d-13              [-1, 8, 7, 7]               0
          Dropout-14              [-1, 8, 7, 7]               0
           Conv2d-15             [-1, 16, 7, 7]           1,168
             ReLU-16             [-1, 16, 7, 7]               0
      BatchNorm2d-17             [-1, 16, 7, 7]              32
           Conv2d-18             [-1, 32, 7, 7]           4,640
             ReLU-19             [-1, 32, 7, 7]               0
      BatchNorm2d-20             [-1, 32, 7, 7]              64
        MaxPool2d-21             [-1, 32, 3, 3]               0
          Dropout-22             [-1, 32, 3, 3]               0
           Conv2d-23             [-1, 10, 1, 1]           2,890
================================================================
Total params: 17,106
Trainable params: 17,106
Non-trainable params: 0

This has resulted in accuracy of 99.41%
