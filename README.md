

# Aerial Image Segmentation with PyTorch

## Overview

This project implements a pipeline for aerial image segmentation using deep learning techniques with PyTorch. The model is designed to segment roads from aerial imagery using a subset of the Massachusetts Roads Dataset.
## Dataset

The dataset consists of a subset of 200 aerial images and their corresponding masks from the Massachusetts Roads Dataset, which contains a total of 1,171 aerial images of Massachusetts, each sized 1500×1500 pixels. The images cover an area of approximately 2.25 square kilometers.

**Full Dataset:**
You can find the complete dataset [here](https://www.cs.toronto.edu/~vmnih/data/).

**Citation:**
```bibtex
@phdthesis{MnihThesis,
  author = {Volodymyr Mnih},
  title = {Machine Learning for Aerial Image Labeling},
  school = {University of Toronto},
  year = {2013}
}
```

## Installation

To set up the environment, install the required libraries using the following commands:

```bash
!pip install segmentation-models-pytorch
!pip install -U git+https://github.com/albumentations-team/albumentations
!pip install --upgrade opencv-contrib-python
```

## Usage

1. Clone the repository:
    ```bash
    !git clone https://github.com/parth1620/Road_seg_dataset.git
    ```

2. Import necessary libraries and load the dataset.
3. Configure training parameters including batch size, learning rate, and image size.
4. Set up data augmentation techniques for training and validation(using Albumentation which performed the same augmentation for both satallite images and their masks).
5. Create a custom dataset class for loading images and masks.
6. Initialize the model and set it to the appropriate device (GPU/CPU).
7. Implement training and validation functions.
8. Train the model on the dataset and evaluate its performance.

## Training

The model can be trained using the provided training loop, which leverages the `SegmentationModel` class. The training process includes calculating loss using both Dice Loss and Binary Cross-Entropy with Logits Loss.

## Inference

Once trained, the model can be used for inference on new aerial images to predict segmentation masks.

## Credits

This project is an implementation of a guided project by [pdhameliya](https://www.linkedin.com/in/pdhameliya).
