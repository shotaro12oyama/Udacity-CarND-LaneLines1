# **Finding Lane Lines on the Road** 

## Writeup Report


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/pipeline_image.jpg “Example”

---


### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 

First, I converted the images to grayscale. 

Second, I applied Gaussian Filter to reduce the noise included in the images.

Third, I set polygon mask in order to make focus on the probable area in the images, then applied Canny Edge detection, to detect the edge lines of each object in the images.

Fourth, I applied Hough Transform, to detect Lane lines. Then, I draw the lines on the masked image.

Fifth, I add the lines on the original images.


In order to draw a single line on the left and right lanes, I modified the draw_lines() function.

I separated the group of lines to right lanes & left lanes by the value of slope. Especially, I adjusted the value condition of the slope to +-0.55, taking into the probable slope value. Then, I took the mean of the start / end plot of the lines. Finally, I extend the lines to the bottom of images by calculating the new plot based on the mean plot & slope.


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are several colors on the road between the two lanes, due to some reason such as maintenance for asphalt.
 

Another shortcoming could be happened when we come to an intersection or tunnel.




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to define the separated polygon and edge detection from right and left side in order to eliminate misleading objects / colors in the images.

