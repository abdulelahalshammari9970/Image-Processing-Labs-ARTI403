# Lab 7 — Laplacian Filter and Mathematical & Statistical Filters

**Course:** ARTI 403 – Image Processing

## Overview

This lab is split into two notebooks. Lab 7(A) sharpens images with the
Laplacian filter, and Lab 7(B) adds different types of noise to an image and
removes them with mean and order-statistic filters, using OpenCV, NumPy,
pandas and Matplotlib in Python.

## Input Images

The input images are stored in the `Images/` folder:

- `moon.jpg` — used for Laplacian sharpening in Lab 7(A)
- `noise.jpg` — clean test image (square and circle); Gaussian, salt & pepper,
  exponential, uniform, salt-only and pepper-only noise are added to it in Lab 7(B)
- `person.jpg` — real image that already contains salt & pepper noise
- `dome.jpg` — real image with large salt & pepper noise dots

## Tasks

### Lab 7(A) — Laplacian Filter

#### Method 1 — Manual Laplacian Kernel

- Apply the 3×3 Laplacian kernel with `cv2.filter2D` and add the absolute
  Laplacian to the original image
- Use `cv2.add` (saturating) instead of `+` to avoid `uint8` overflow

#### Method 2 — Gaussian Blur + `cv2.Laplacian`

- Reduce noise with a 3×3 Gaussian blur before applying `cv2.Laplacian`

#### Additional Comparisons

- 4-neighbour vs. 8-neighbour Laplacian kernel
- Standard sharpening `g = f − ∇²f` vs. adding the absolute Laplacian

### Lab 7(B) — Mathematical and Statistical Filters

#### Adding Noise

- Gaussian, salt & pepper, exponential, uniform, salt-only and pepper-only noise

#### Filters

- Arithmetic mean (built-in `cv2.blur` and manual kernel)
- Geometric mean and harmonic mean
- Contra-harmonic mean with Q = 1.5 (pepper) and Q = −1.5 (salt)
- Median, max, min and midpoint filters

#### Comparison and Real Images

- PSNR table of every filter on every noise type, with the best filter highlighted
- Median filtering of the real noisy images `person.jpg` and `dome.jpg` with
  different kernel sizes
