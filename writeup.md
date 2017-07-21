# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: /Users/oyama/Documents/GitHub/CarND-LaneLines-P1/test_images_output/pipeline_image.jpg “Example”

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 

First, I converted the images to grayscale. 

Second, I applied Gaussian Filter to reduce the noise included in the images.

Third, I applied Canny Edge detection, to detect the edge lines of each object in the images.

Fourth, I applied Hough Transform, to detect Lane lines. Then, I draw the lines on the masked image.

Fifth, I add the lines on the original images.


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by 


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
