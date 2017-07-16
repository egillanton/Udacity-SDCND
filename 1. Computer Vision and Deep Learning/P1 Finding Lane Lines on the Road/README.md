# **Project 1. Finding Lane Lines on the Road** 

<img src="CarND-P1.jpg" alt="Title Image" />

## Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.
In this project I detected lane lines in images using Python 3 and OpenCV.

---

## [My Code | Jupiter Notebook](https://github.com/egillanton/Udacity-SDCND/blob/master/1.%20Computer%20Vision%20and%20Deep%20Learning/P1%20Finding%20Lane%20Lines%20on%20the%20Road/P1.ipynb)

---

## Reflection

### 1. My Pipeline
In the first part of the assignment was to create a pipline function **process_image()** that takes in an image and returns another image that has hightlighted lane lines. My pipeline consisted of 5 steps:

#### Original Image
<img src="display_images_output/original_image.jpg" alt="Original Image" height="250" />

#### Step 1. Convert the image to grayscale.

This is done to  be able to find lines of any color.

##### Grayscale Image
<img src="display_images_output/gray_image.jpg" alt="Grayscale Image" height="250"  />

#### Step 2. Blur the grayscaled image using Gaussian  blurring

This is done to suppress noise

##### Blurred Image
<img src="display_images_output/blurred_image.jpg" alt="Grayscale Image" height="250"  />

#### Step 3. Use Canny Edge Detection on the blurred image

This is done to extract edges within the image

##### Edged Image
<img src="display_images_output/edged_image.jpg" alt="Edged Image" height="250"  />

#### Step 4. Create a trapozoid mask for the area of interest

This is to narrow down the area that we will be focusing on.

##### Region of Interest Mapped Image
<img src="display_images_output/roi_img.jpg" alt="Region of Interest Mapped Image" height="250"  />


#### Step 5. Apply Hough Transformation on our masked edged image.

This will highlight the lines of interest.

##### Hough Transformed Image
<img src="display_images_output/houghed_image.jpg" alt="Hough Transformed Image" height="250"  />


#### Step 6. Mask Hough transformed mage over the original image.

##### Final Image
<img src="display_images_output/final_image.jpg" alt="Hough Transformed Image" height="250"  />

### 2. Potential shortcomings

### 3. Possible improvements
