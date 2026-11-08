# Lab 9 — Morphological Operations

**Course:** ARTI 403 – Image Processing

## Overview

This lab applies morphological image processing to binary images using OpenCV,
NumPy, pandas and Matplotlib in Python: erosion, dilation, opening, closing and
boundary extraction. It also investigates how the shape and the size of the
structuring element affect the processed images, as described in the Lab 9 task.

## Input Images

The input images are stored in the `Images/` folder:

- `Erosion.jpg` — used for the erosion and dilation demonstration
- `Open_Closing.jpg` — noisy binary image used for the opening demonstration
- `Opening2.jpg` — binary image with small gaps, used for the closing demonstration
- `BoundaryExtraction.jpg` — silhouette used for boundary extraction
- `Balls_1_.png` — binary image of 15 touching balls (black balls on a white
  background), selected for Task 1 and Task 2. It is inverted after Otsu
  thresholding so that the balls become the white foreground
- `Erosion2.jpg` — extra image provided with the lab (not used in the notebook)

## Tasks

### Lab Demonstration

- Erosion and dilation with 3×3, 7×7 and 11×11 square kernels
- Opening (5×5 kernel) and closing (45×45 kernel)
- Boundary extraction: morphological gradient, internal boundary and external boundary

### Task 1 — Apply Morphological Operations to a New Image

- Select the `Balls_1_.png` binary image and invert it so the balls are white
- Apply erosion, dilation, opening and closing with a 9×9 square kernel
- Display the original image and the result of each operation, with the number
  of white pixels

### Task 2 — Experiment with Structuring Elements

- Apply erosion and dilation using square, cross and ellipse structuring
  elements (`cv2.getStructuringElement`)
- Use kernel sizes 3×3, 5×5 and 7×7
- Display the structuring elements and the 3×3 comparison grids of results
- Compare the results with a table of white pixels and percentage change, and
  zoomed crops
- Conclusion: the square has the strongest effect, the cross the weakest, and
  the ellipse is in between; larger kernels give a stronger effect
