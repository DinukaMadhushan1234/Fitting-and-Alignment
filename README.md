# EN3160 - Image Fitting and Alignment Assignment

## Overview
This repository contains the code and materials for the EN3160 assignment on image fitting and alignment. The assignment explores blob detection, RANSAC-based line and circle fitting, homography computation for image overlay, and image stitching using SIFT feature matching.

### Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Task Breakdown](#task-breakdown)
  - [Q1: Blob Detection](#q1-blob-detection)
  - [Q2: Line and Circle Fitting](#q2-line-and-circle-fitting)
  - [Q3: Homography for Image Overlay](#q3-homography-for-image-overlay)
  - [Q4: Image Stitching](#q4-image-stitching)
- [Results](#results)
- [How to Run](#how-to-run)
- [References](#references)

## Project Structure
- Codes/Alignment.ipynb # Homography-based image alignment (Q3)
- Blobs_detection.ipynb # Blob detection using Laplacian of Gaussian (Q1)
- Fitting.ipynb # RANSAC-based line and circle fitting (Q2)
- Image_Superimposition.ipynb # Image superimposition using homography (Q3)
- images/ # Input images used in the tasks
- output_images/ # Output images generated after the tasks
- .gitignore # Git ignore file
- README.md # This file
- report.pdf # Final report for the assignment

## Requirements
Make sure you have the following dependencies installed before running the code:
```bash
pip install opencv-python numpy matplotlib
```
## Task Breakdown

### Q1: Blob Detection
**Goal:** Detect blobs in the provided sunflower field image using the Laplacian of Gaussian (LoG) method.

**Approach:** The image was filtered at multiple scales, and the largest detected circle's parameters were extracted and visualized.

**Relevant File:** Blobs_detection.ipynb

### Q2: Line and Circle Fitting
**Goal:** Fit a line and circle to a noisy dataset using the RANSAC algorithm.

**Approach:** A line was fitted first, followed by fitting a circle to the remaining points.

**Relevant File:** Fitting.ipynb

### Q3: Homography for Image Overlay
**Goal:** Superimpose an overlay image (e.g., ENTC logo) onto a base image (billboard) by calculating a homography.

**Approach:** Four points were selected on the base image to compute the homography matrix, followed by warping and blending the overlay image.

**Relevant File:** Image_Superimposition.ipynb

### Q4: Image Stitching
**Goal:** Stitch two Graffiti images by matching SIFT features and computing a homography.

**Approach:** SIFT features were matched, and a homography matrix was computed using RANSAC. The images were then stitched together.

**Relevant Files:** Alignment.ipynb

## Results
All tasks were successfully completed with the expected outputs. You can find the results in the output_images/ directory.

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/DinukaMadhushan1234/Fitting-and-Alignment.git
```
2.Install the necessary dependencies:
```bash
pip install -r requirements.txt 
```
3.Open the Jupyter notebooks in the Codes/ directory and run them.

## References
- SIFT Documentation
- RANSAC Algorithm
- Homography Matrix
