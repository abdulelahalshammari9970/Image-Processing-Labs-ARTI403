# Lab 6 — Frequency Domain Filtering

**Course:** ARTI 403 – Image Processing

## Overview

This lab applies filtering in the frequency domain to digital images using
NumPy's FFT, Matplotlib, SciPy and scikit-image in Python, as covered in the
Lab 6 procedural manual. Instead of convolving in the spatial domain, the image
spectrum is multiplied by the filter's frequency response and transformed back
with the inverse FFT.

## Input Images

The input images (`Images/camera.png` and `Images/page.png`) are sample images
from the [scikit-image](https://scikit-image.org/docs/stable/auto_examples/data/plot_general.html)
general-purpose image gallery. They are saved to disk once at the start of the
notebook so the rest of the workflow reads/writes them like any other local
image. The `camera` (Cameraman) image is the one required by the manual, and
the `page` image (a scanned book page) is used as an additional example.

## Tasks

### Procedural Steps

#### Task 1 — Laplacian Filtering in the Frequency Domain

- Build the Laplacian frequency response `H(u, v) = -4π²(u² + v²)` using `np.fft.fftfreq`
- Multiply it with the FFT of the Cameraman image and apply the inverse FFT
- Display the original image, the Laplacian spectrum and the spatial output

### Assessment

#### Task 1 — Sobel Filters in the Frequency Domain

- Zero-pad the 3×3 Sobel X and Sobel Y kernels to the image size, centre them and apply `ifftshift` before the FFT (`center_embed_kernel`)
- Multiply the image spectrum by each filter's spectrum and apply the inverse FFT
- Display the Sobel filter spectra, Sobel X, Sobel Y and the gradient magnitude `√(gx² + gy²)`
- Verify the result against spatial convolution (`scipy.ndimage.convolve` with `mode='wrap'`); both results match to floating-point precision
- Apply the same Sobel filtering to the `page` image as an additional example
