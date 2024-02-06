# Gesture-Recognition-for-SMART-TVs
A cool feature in the smart TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.  

## Gesture - Functionality mapping
The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

 - Thumbs up:  Increase the volume
 - Thumbs down: Decrease the volume
 - Left swipe: 'Jump' backwards 10seconds
 - Right swipe: 'Jump' forward 10 seconds  
 - Stop: Pause the movie
 
## The Dataset  

The [dataset](https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL) consists of video sequences. Each video is a sequence of 30 frames (or images).  

The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam, similar to what the smart TV will use.  

All images in a particular video have the same dimensions but different videos may have different dimensions.

Each row of the CSV file represents one video and contains three main pieces of information - the name of the subfolder containing the 30 images of the video, the name of the gesture and the numeric label (between 0-4) of the video. 

## Approach

We have used several models and used their accuracies to select the best model. 
- Conv2D + LSTM + GRU
  - used augmentations, achieved 85% accuracy.
- Conv3D
  - used a batch size of 20, achieved 90% accuracy.
- Transfer Learning
  - used imagenet and then trained the weights, achieved 98% accuracy.

## 
