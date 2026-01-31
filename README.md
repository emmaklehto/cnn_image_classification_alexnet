# Image Classification with AlexNet (ImageNet)

Simple image classification pipeline using a pretrained AlexNet model from PyTorch.
The script performs Top-1 and Top-5 predictions on images using ImageNet class labels.

Credits:
https://github.com/Holmes-Alan/ImageNet_sample/tree/main


## Description

This project demonstrates inference with a pretrained convolutional neural network (AlexNet)
using transfer learning. No training is performed.


## Model

– Architecture: AlexNet  
– Framework: PyTorch/torchvision  
– Pretrained on: ImageNet (1000 classes)

## Data

– Input images are loaded from the images/ directory  
– Class label mappings are loaded from:
  – imagenet_classes.txt
  – imagenet_synsets.txt

## Preprocessing

– Resize images to 256×256  
– Center crop to 224×224  
– Convert to tensor  
– Normalize using ImageNet mean and standard deviation


## Inference

– Load image using PIL  
– Apply preprocessing  
– Add batch dimension  
– Move tensor to GPU if available  
– Forward pass through AlexNet  
– Apply softmax to obtain probabilities  
– Print Top-1 and Top-5 predictions


## Output

Example:

Top-1: 92.00% – tabby cat

Top-5:
– tabby cat  
– tiger cat  
– Persian cat  


## Observations

– Performs best on clear, single-object images  
– Confuses visually similar classes  
– Performance drops with occlusions or multiple objects


## Possible Improvements

– Fine-tune on a custom dataset  
– Replace AlexNet with a modern architecture (ResNet, EfficientNet)  
– Add batch inference  
– Compute Top-1 and Top-5 accuracy on a validation set

## Technical Info

– Number of classes: 1000  
– Input image size: 224×224  
– AlexNet layers: 5 convolutional + 3 fully connected
