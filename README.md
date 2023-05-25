# Image Edge Detection and Noise Calculation

This repository contains Python code for performing edge detection on an image using the Canny, Sobel, and Log Sobel methods. It also calculates the noise in the detected edges.

## Overview

The code uses the OpenCV library to read an input image and apply edge detection algorithms to detect edges. The following edge detection methods are implemented:

1. **Canny Edge Detection**: The Canny algorithm is a popular edge detection technique that applies gradient-based methods and hysteresis thresholding to detect edges in an image.

2. **Sobel Edge Detection**: The Sobel algorithm utilizes gradient calculations in the x and y directions to identify edges. It calculates the gradient magnitude and direction at each pixel, highlighting edges with high gradient values.

3. **Log Sobel Edge Detection**: The Log Sobel algorithm combines the Laplacian of Gaussian (LoG) operator and Sobel operator to detect edges. It first applies Gaussian blurring to the image and then calculates the Laplacian to identify edges.

The code provides functions to perform edge detection using the above methods and display the resulting edge images. Additionally, it calculates the noise in the detected edges by comparing them with the original image.

## Usage

1. Install the required libraries: OpenCV, NumPy, and Matplotlib.

2. Import the necessary modules and functions in your Python script.

3. Load an image using `cv2.imread()` and specify the path to the image file.

4. Apply edge detection by calling the respective functions:
   - `canny_edge_detection(image, lower_threshold, upper_threshold)` for Canny edge detection.
   - `sobel_edge_detection(image, ksize, scale, delta)` for Sobel edge detection.
   - `log_sobel_edge_detection(image, ksize, scale, delta)` for Log Sobel edge detection.

5. Display the original image and the detected edge images using `matplotlib.pyplot.imshow()`.

6. Calculate the noise in the detected edges by calling `calculate_noise(image, edges)`.

7. Print the noise values for each edge detection method.

## Results

The code provides visual outputs of the original image and the detected edges using the Canny, Sobel, and Log Sobel algorithms. Additionally, it prints the noise values for each edge detection method, indicating the level of noise present in the detected edges.
