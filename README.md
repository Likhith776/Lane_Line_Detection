
# Lane Line Detection

This repository contains a project for detecting lane lines in images and videos using various image processing techniques and computer vision algorithms. The main objective is to accurately identify the lane markings on roads in different conditions.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
- [Results](#results)

## Installation

To run this project, you need to have Python installed along with some additional libraries. You can install the required libraries using `pip`:

```bash
pip install numpy matplotlib opencv-python moviepy
```

## Usage

### Detect Lane Lines in Images

To detect lane lines in images, place your images in the `test_images` directory and run the following command:

```python
python lane_line_detection.py
```

### Detect Lane Lines in Videos

To process videos, place your videos in the `test_videos` directory and run the script:

```python
python process_video.py
```

This will process the videos and save the output in the `output_videos` directory.

## Project Structure

- `main.py`: Contains the main logic for processing images to detect lane lines.
- `test_images/`: Directory containing test images.
- `test_videos/`: Directory containing test videos.
- `output_videos/`: Directory where output videos will be saved.

## Methodology

The project involves the following steps to detect lane lines:

1. **Color Selection**: Apply color masks to select white and yellow colors which correspond to lane lines.
2. **Grayscale Conversion**: Convert the image to grayscale.
3. **Gaussian Blur**: Apply Gaussian blur to the grayscale image to smooth it.
4. **Canny Edge Detection**: Use the Canny edge detection algorithm to detect edges in the image.
5. **Region of Interest Selection**: Define and mask the region of interest where lane lines are likely to be.
6. **Hough Transform**: Use the Hough transform to detect lines in the edge-detected image.
7. **Lane Line Averaging**: Average the detected lines to form a single line for the left and right lanes.
8. **Drawing Lines**: Draw the lane lines onto the original image.

## Results

### Images
![Lane Line Detection](results/image_results.png)

### Videos
Processed videos will be saved in the `output_videos` directory.
