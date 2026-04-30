# Unscented Kalman Filter Project Starter Code
Self-Driving Car Engineer Nanodegree Program

---

## Dependencies

* cmake >= v3.5
* make >= v4.1
* gcc/g++ >= v5.4

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./UnscentedKF path/to/input.txt path/to/output.txt`. You can find
   some sample inputs in 'data/'.
    - eg. `./UnscentedKF ../data/obj_pose-laser-radar-synthetic-input.txt`

## Editor Settings

We've purposefully kept editor configuration files out of this repo in order to
keep it as simple and environment agnostic as possible. However, we recommend
using the following settings:

* indent using spaces
* set tab width to 2 spaces (keeps the matrices in source code aligned)

## Code Style

Please stick to [Google's C++ style guide](https://google.github.io/styleguide/cppguide.html) as much as possible.
# Traffic Light Classifier

This repository contains a deep learning traffic light classifier designed for integration into a self-driving car capstone project[cite: 1]. The model utilizes a Convolutional Neural Network (CNN) to classify images into four categories: **Red**, **Yellow**, **Green**, and **None**[cite: 1, 3].

## Project Structure

*   **`traffic_light_classifier.py`**: Contains the `TrafficLightClassifier` class which defines the deep network architecture and loss functions[cite: 1, 3].
*   **`traffic_light_dataset.py`**: Provides the `TrafficLightDataset` class for handling data loading, normalization, and augmentation[cite: 1, 4].
*   **`train.py`**: The main entry point for training the model using the mixed dataset[cite: 1, 5].
*   **`test.py`**: A utility script to perform inference and test the model using pretrained weights[cite: 1, 2].
*   **`README.md`**: Documentation for the project[cite: 1].

## Dataset

The classifier is trained on a combination of two datasets totaling 2,475 frames[cite: 1]:
*   **Simulator Dataset**: 1,324 frames at 800x600 resolution[cite: 1].
*   **Udacity Circuit Dataset**: 1,151 real-world frames at 800x600 resolution[cite: 1].

## Getting Started

### Training
To train the model from scratch, ensure your dataset is prepared in `.npy` format and run[cite: 5]:
```bash
python train.py
