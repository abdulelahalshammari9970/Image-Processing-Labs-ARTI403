# ARTI403 – Image Processing

## Lab 1: Loading, Visualizing, and Storing Images

**Student Name:** Abdulelah Alshammari
**Student ID:** 2240005261

## Overview

This lab introduces the basics of image processing with Python. It demonstrates how digital images can be loaded, displayed, saved, and represented as NumPy arrays using OpenCV and PIL.

## Lab Objectives

* Load and display an image using OpenCV.
* Load and display an image using PIL.
* Save images to the disk.
* Convert a PIL image into a NumPy array.
* Display image dimensions, pixel values, and data types.
* Perform basic NumPy operations on image arrays.

## Libraries Used

* NumPy
* OpenCV
* Pillow (PIL)
* Matplotlib

## Installation

Install the required libraries using:

```bash
pip install numpy opencv-python pillow matplotlib
```

## Images Used

The following grayscale images are stored inside the `images` folder:

* `cameraman.tif`
* `lena_gray_256.tif`

## Tasks Completed

### Task 1: Python Environment Setup

The required Python libraries were installed and imported into the Jupyter Notebook.

### Task 2: Loading and Visualizing Images

* The first image was loaded using `cv2.imread()`.
* The second image was loaded using `Image.open()`.
* Both images were displayed using Matplotlib.

### Task 3: Storing Images

* The OpenCV image was saved using `cv2.imwrite()`.
* The PIL image was saved using the `save()` method.

### Task 4: Displaying Images as Arrays

* The shape and pixel values of the OpenCV image were displayed.
* The PIL image was converted into a NumPy array.
* The array shape, data type, and pixel values were displayed.

### Additional NumPy Operations

The following operations were performed:

* Calculating minimum and maximum pixel intensity.
* Calculating mean intensity and standard deviation.
* Creating an image negative.
* Increasing image brightness.
* Cropping the image.
* Flipping the image horizontally.

## Project Structure

```text
Lab01/
├── ARTI403_Lab1_2240005261.ipynb
├── README.md
└── images/
    ├── cameraman.tif
    └── lena_gray_256.tif
```

## How to Run

1. Open `ARTI403_Lab1_2240005261.ipynb` using Jupyter Notebook or VS Code.
2. Make sure the `images` folder is in the same directory as the notebook.
3. Run the notebook cells in order.
4. The processed images and array information will appear below the cells.

## Conclusion

In this lab, images were successfully loaded, displayed, and stored using OpenCV and PIL. The images were also represented as NumPy arrays, allowing different operations to be applied directly to their pixel intensity values.
