---
title: "Video Interpolation using Optical Flow"
excerpt: "<img src='/images/of1.gif'>"
permalink: /projects/video_interpolation_using_of
collection: projects
---

Codes are not yet made public.

## About the project
The aim of this project was to interpolate frames in the video by only using optical flow calculated from frames right before and right after the target frame. I did not use any DL methods because of lack of computational resources and time.

## Method
The entire algorithm is described in the figure below.

<img src='/images/alg1.png'>

<img src='/images/alg2.png'>

The input is two consecutive frames from the original and the background image. The background image is the image where no moving object is in the frame, which was obtained from the end of the video.

Then background subtraction is used to detect the moving objects, which is filtered by a threshold using distance from center of gravity of the detected points to remove any outliers. Then optical flow is calculated using grayscaled images.

Finally, the pixels are estimated and is added with the background image to generate the interpolating frame.

## Result
The input video was first thinned out so that the frame rate was 1/4 of the original video.

<img src='/images/of2.gif'>
<!-- <video src='/images/comparison_2 copy.mp4'> -->

The result above is when 3 frames were generated between the original 2 frames. On the left is the original video and the right one is the generated video.

We can see that the generated video is very similar to the original movie.
