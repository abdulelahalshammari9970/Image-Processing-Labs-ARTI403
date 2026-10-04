# Lab 4 — Intensity Transformations and Filtering (Spatial Domain)

**Course:** ARTI 403 – Image Processing

## Overview

This lab applies thresholding and histogram-based intensity transformations to
digital images using OpenCV, NumPy, Matplotlib and scikit-image in Python, as
covered in the Lab 4 procedural manual.

## Input Images

The input images (`images/moon.png`, `images/rocket.png`, `images/chelsea.png`
and `images/camera.png`) are sample images from the [scikit-image](https://scikit-image.org/docs/stable/auto_examples/data/plot_general.html)
general-purpose image gallery. They are saved to disk once at the start of the
notebook so the rest of the workflow reads/writes them like any other local
image. The `camera` image is used for the thresholding task in place of
`Parrot.png`, which is not part of scikit-image.

## Tasks

### Procedural Steps

#### Task 1 — Thresholding

- Apply a fixed binary threshold with several threshold values (0, 50, 100, 150, 200)

#### Task 2 — Histogram Processing

- Contrast stretching of the moon image between the 2nd and 98th percentiles
- Display the image and its histogram before and after the stretch

### Assessment

#### Task 1 — Contrast Stretching

- Rescale the moon image intensities between the 3rd and 80th percentiles and plot the histogram

#### Task 2 — Histogram Equalization

- Flatten the histogram of the moon image using `exposure.equalize_hist`

#### Task 3 — Histogram Matching

- Match the histogram of the Chelsea image to the rocket image (reference) using `match_histograms`
