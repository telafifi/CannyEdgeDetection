# Python Canny Edge Detector
Canny edge detection is an image processing method that uses a multi-stage algorithm to detect edges in an image while suppressing noice. 

# Canny Edge Detection Algorithm

## Overview of Steps
1)    Grayscale conversion - Convert an image from RGB to grayscale
2)    Noise Reduction - Apply Gaussian Filter to blur the image
3)    Gradient Calculation - Determine the gradient matrix.
4)    Non-Maximum Suppression - convert pixel magnitudes to a boolean as to whether the pixel is considered an edge or not
5)    Double Threshold - Compare the magnitudes of each edge pixel to two separate thresholds to determine if the edge has a large enough magnitude
6)    Edge Hysteresis -  Connect the weak edges to their strong neighbour.

Using this process we would be able to convert the following image conversions:
Original Image             |  Edge Map
:-------------------------:|:-------------------------:
![BlueBird Image normal](Images/BlueBird.jpg)  |  ![BlueBird Canny Edge](/Results/BlueBird_Result.png)
![Burj Khalifa normal](Images/BurjKhalifa.jpg)  |  ![Burj Khalifa Canny Edge](/Results/BurjKhalifa_Result.png)
![Zebra Image normal](Images/Zebra.jpg)  |  ![Zebra Canny Edge](/Results/Zebra_Result.png)

## Step 1: Grayscale conversion
This algorithm is based on grayscale images. Therefore, the pre-requisite to begin the edge-detection is to convert the image from it's original RGB configuration to a grayscale image

## Step 2: Noise Reduction
The mathematics involved in this algorithm are mainly based on derivatives, this makes the results incredibly sensitive to image noise. One way to reduce noise is by applying a Gaussian blur to smooth the image. 
  
