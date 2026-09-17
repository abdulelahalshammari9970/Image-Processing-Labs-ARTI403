# Lab 3 — Image Manipulations using OpenCV
**Course:** ARTI 404 – Image Processing

## Overview
This lab applies geometric and intensity transformations to a digital image using
the OpenCV library in Python, as covered in the Lab 3 procedural manual.

## Input Image
The input image (`images/input.jpg`) is the `astronaut` sample image from the
[scikit-image](https://scikit-image.org/docs/stable/auto_examples/data/plot_general.html)
general-purpose image gallery. It is saved to disk once at the start of the
notebook so the rest of the workflow reads/writes it like any other local image.

## Tasks

### Task 1 — Geometric Transformations
- Increase the size of the image (resized 1.5x using bicubic interpolation)
- Rotate the image by 120 degrees
- Perform a shear operation on the image

### Task 2 — Intensity Transformations
- Negative image
- Log transformation
- Power-law (gamma) transformation, gamma = 0.4

