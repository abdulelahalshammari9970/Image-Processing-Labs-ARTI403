# Lab 10 — Image Segmentation and Feature Extraction

**Course:** ARTI 403 – Image Processing

## Overview

This lab applies edge detection, feature extraction and segmentation to
digital images using OpenCV, NumPy, Matplotlib and scikit-image in Python, as
covered in the Lab 10 procedural manual. It covers Canny edge detection, Harris
corner detection, simple binary thresholding and Otsu's automatic thresholding.

## Input Images

The input images (`camera`, `checkerboard` and `coins`) are sample images from
the [scikit-image](https://scikit-image.org/docs/stable/auto_examples/data/plot_general.html)
general-purpose image gallery. They are loaded directly in the notebook using
`skimage.data`, so no external image files are needed to run it.

## Tasks

### Procedural Steps

#### Task 1 — Canny Edge Detection

- Detect edges in the camera image using `cv2.Canny` with thresholds 100 and 200
- Display the original image and the edge image side by side

#### Task 2 — Harris Corner Detection

- Convert the checkerboard image to grayscale and apply `cv2.cornerHarris` (blockSize = 2, ksize = 3, k = 0.04)
- Keep the strong corners using a threshold of 0.01 × the maximum response
- Mark the detected corners with large red dots and display the result

#### Task 3 — Simple (Global) Binary Thresholding

- Apply a fixed binary threshold (T = 127) to the coins image using `cv2.threshold`
- Display the original and the thresholded images side by side

### Assessment

#### Task 1 — Otsu's Thresholding

- Segment the coins image using `cv2.threshold` with `THRESH_BINARY + THRESH_OTSU`, so the threshold is chosen automatically (T = 107)
- Display the original image, its histogram (with the Otsu threshold marked) and the thresholded image
