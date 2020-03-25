# Rapid-Diagnostic-Model-keras-tensorflow
The notebook is based on the pipeline from https://github.com/sahupankaj10/Chest-X-ray-image-classification
![Block diagram of the CNN](https://github.com/covid19-Rapid-AI-Diagnostics/Rapid-Diagnostic-Model-keras-tensorflow/blob/master/CNN%20model%20for%20pneumonia.jpg)

This model is based on the concept of skip connections. It has 5 convolutional blocks (can be changed); with 16,32,64,32,16 filters. The convolutional blocks are followed by 2 dense layers and an output layers (can be changed). Each convolutional block has three signal pathways, let's call them x1, x2 and x3. x1 receives x as input, apply 3by 3, then 5 by 5 and then 7 by 7 convolutional kernels. x2 receives x1 as input, apply 5 by 5 and then 7 by 7 convolutional kernels and x3 apply a 7 by 7 convolutional kernels to x2. Afterwards,x1 and x2 are concatenated to create x12. x12 and x3 are concatenated to create x. x is passed through the dense layers and then output layers. 
