# Lab 5 — Spatial Filtering (Smoothing and Sharpening)

**Course:** ARTI 403 – Image Processing

## Overview

This lab applies spatial filtering to digital images using OpenCV, NumPy,
Matplotlib and scikit-image in Python, as covered in the Lab 5 procedural
manual. It covers smoothing with box and Gaussian filters, and sharpening
with unsharp masking and the Laplacian filter.

## Input Images

The input images (`images/hubble.png`, `images/brick.png`, `images/ihc.png`
and `images/coins.png`) are sample images from the [scikit-image](https://scikit-image.org/docs/stable/auto_examples/data/plot_general.html)
general-purpose image gallery. They are saved to disk once at the start of the
notebook so the rest of the workflow reads/writes them like any other local
image. The `hubble` (Hubble Deep Field) image is used for the unsharp masking
task in place of `Parrot.png`, which is not part of scikit-image.

## Tasks

### Procedural Steps

#### Task 1 — Unsharp Masking

- Blur the image with a Gaussian filter (σ = 2)
- Sharpen it using `image + amount * (image - blurred)` with amount = 1.5
- Display the original, blurred and sharpened images

### Assessment

#### Task 1 — Box Filter

- Convolve the brick image with a 7×7 box filter using `cv2.filter2D`
- Display the original and smoothed images side by side

#### Task 2 — Gaussian Filter

- Apply a 5×5 and a 21×21 Gaussian filter to the immunohistochemistry image using `cv2.GaussianBlur`
- Display the original and the two filtered images side by side

#### Task 3 — Laplacian Sharpening

- Apply a 3×3 Laplacian filter to the coins image using `cv2.Laplacian`
- Sharpen the image using `np.clip(image_float - laplacian, 0, 1)`
- Display the original, Laplacian and sharpened images
