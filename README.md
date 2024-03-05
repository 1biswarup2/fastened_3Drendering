# FastNeRF Project

## Overview

`FastNeRF` is a neural radiance field (NeRF) implementation optimized for speed and efficiency, leveraging PyTorch for high-performance GPU acceleration. This project aims to provide a fast, scalable solution for 3D scene rendering using deep learning.

## Features

- Positional encoding layer for high-dimensional input data.
- Separate networks for positional and directional components.
- Efficient data loading for training on large datasets.
- Customizable network architecture to adapt to various dataset sizes.

## Installation

Clone this repository and install the required dependencies.

```bash
git clone https://github.com/your_github/fastenerf.git
cd fastenerf
pip install -r requirements.txt

...

## Synthetic Data Generation

This project includes a script for generating synthetic data to test the NeRF model. The data simulates a 3D scene composed of various elements, which can be customized as per requirements.

```python
import numpy as np

# Define parameters
num_images = 10  # Number of images
image_size = (100, 100)  # Image dimensions
num_pose_params = 6  # Number of pose parameters

# Generate synthetic data
images, poses, focal_lengths = generate_synthetic_data(num_images, image_size, num_pose_params)

# Save data to .npz file
np.savez('synthetic_dataset.npz', images=images, poses=poses, focal=focal_lengths)

