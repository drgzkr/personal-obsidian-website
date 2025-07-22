---
{"dg-publish":true,"permalink":"/science-projects/cnn-based-video-segmentation/"}
---

## What?

Naturalistic Video Segmentation using vgg19 Features
This notebook saves the individual frames of given videos, extracts selected vgg19 layer features for each frame for each video and creates feature timeseries, and lastly plots the difference between each frames features on a timeline.
There are certain anomalies, and reasons and solutions are discussed at the end.

More at:
https://colab.research.google.com/drive/16TkQXS8wqkoVg47df1RvOw8B9TmYyjUs?usp=sharing

---
## Time Perception

Roseboom et al build up the frame by frame feature change timeseries using the Euclidean distance between the feature vectors of each successive frame. If you take a closer look at their figures and supplementary material, you can see that this results in a very big Euclidean Distance scale difference across the timeseries from different layers.

Instead of the Euclidean distance, we are using 1 - PearsonR between each successive frame as a difference metric. This makes sure that the differences are normalized for each layer and are more comparable to one another.

Below, you can see how you can replicate both the static and dynamic thresholding for the timeseries we have created.

The static threshold is defined as (Fmax + Fmin)/2, where F is the layer specific feature difference timeseries

Should you consider using the dynamic threshold, please experiment with different scaling factors for the Tmax = (Fmax + Fmin)/2.

Both result in very similar accumulated perceptual changes.

You can then use the number of changes per layer to replicate their model.

Per video, Roseboom et. al. collect the number of times the change timeseries exceed the threshold, and use these numbers to train a model to predict the actual duration of the video.

Notice that to augment their data, they have divided videos (and therefore the change timelines) into uneven durations, creating a dataset with diverse real durations. Should you want to replicate their model, you should work on a pipeline that populates test and training sets like them.

To get the number of accumulated salient perceptual changes from both static and dynamic thresholds you can simply:

You can then use these to replicate their model which is trained to predict the the real duration of the video in seconds using the number of accumulated changes in each layer. The input to the model would have shape (n_videos, n_layers) and the true outputs can be calculated by simply dividing the number of frames (timepoints) by 24 (fps of the video).

If you would use each video in this dataset as a sample, you wont have enough samples, and the duration variation in your set would be too low. Instead, you need to create clips with varying durations from each video and use this augmented dataset.

This is the Dynamic Attention Threshold Class from Roseboom et. al. : [https://github.com/timestorm-project/time-without-clocks/blob/master/src/calculate_accumulators.py](https://github.com/timestorm-project/time-without-clocks/blob/master/src/calculate_accumulators.py)
