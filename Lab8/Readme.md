# Lab 8 — Edge Detection

**Course:** ARTI 403 – Image Processing

## Overview

This lab applies and compares edge detection methods using OpenCV, NumPy and
Matplotlib in Python, and investigates how the Canny thresholds affect the
detected edges, as described in the Lab 8 task.

## Input Image

The input image (`Images/butterfly.jpg`) is a monarch butterfly on green leaves.
It was chosen because it contains many kinds of edges: strong wing borders,
small white dots, thin veins and a textured background. The image from the
original notebook (`kid1.jpg`) is not used.

## Tasks

### Task 1 — Apply Edge Detection Methods

- Convert the image to grayscale and apply a 5×5 Gaussian blur
- Sobel edge detector with `cv2.Sobel` (x, y and gradient magnitude)
- Prewitt edge detector with manual kernels and `cv2.filter2D`
- Canny edge detector with `cv2.Canny` (thresholds 100 and 200)
- Display the original image and the three edge maps

### Task 2 — Effect of Canny Thresholds

- Apply Canny with the threshold pairs (30, 90), (50, 150) and (100, 200)
- Display the three edge maps side by side, with the number of edge pixels
- Zoom on part of the wing to compare small details
- Explain how the thresholds affect the number of detected edges and the
  visibility of image details
