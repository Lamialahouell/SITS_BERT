# SITS-BERT: Satellite Image Time Series Classification

This repository contains the implementation of **SITS-BERT**, a deep learning model for **Satellite Image Time Series (SITS)** classification. The model uses a **Transformer-based architecture** to capture temporal and spectral features in satellite image time series data. The implementation is based on the following paper:

[**SITS-BERT: A Transformer-Based Model for Satellite Image Time Series Classification**](https://ieeexplore.ieee.org/document/9252123)  
Published in the **IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing**.


```bibtex
@article{sitsbert2020,
  title={SITS-BERT: A Transformer-Based Model for Satellite Image Time Series Classification},
  author={Author Names},
  journal={IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing},
  volume={13},
  pages={X--Y},
  year={2020},
  doi={10.1109/JSTARS.2020.3032912}
}
```

## Overview

Satellite Image Time Series (SITS) data consists of multi-spectral images captured over time, which are widely used in applications like land cover classification, crop monitoring, and environmental change detection. Traditional methods often struggle to capture the complex temporal and spectral patterns in SITS data. SITS-BERT addresses this challenge by using a Transformer-based architecture to model long-range dependencies and extract meaningful features from the time series.

## Key Features

- **Transformer Encoder**: The model uses a Transformer encoder to process spectral and temporal features.
- **Positional Encoding**: Incorporates positional encoding to capture the temporal order of satellite images.
- **Pre-training and Fine-tuning**: The model is first pre-trained on a large dataset of unlabeled SITS data and then fine-tuned on a labeled dataset for specific tasks like land cover classification.
- **GPU Acceleration**: The implementation is optimized for GPU usage, ensuring fast training and inference.

## Dataset

The dataset used in this project consists of Sentinel-2 satellite images with 10 spectral bands. The data is preprocessed to normalize reflectance values and generate synthetic acquisition dates (Day of Year - DOY). The dataset is split into training, validation, and test sets for model evaluation.

## Model Architecture

The SITS-BERT model consists of the following components:

- **Observation Embedding**: Combines spectral embeddings with positional encoding to represent each time step.
- **Transformer Encoder**: A stack of Transformer layers to process the embedded time series.
- **Classification Head**: A linear layer for predicting class labels during fine-tuning.

## Results

The model achieves state-of-the-art performance on SITS classification tasks, with high accuracy and robustness to noise. Detailed results, including confusion matrices and misclassification analysis, are provided in the code.


## Acknowledgments

- The authors of the original paper for their groundbreaking work on SITS-BERT.
- The developers of PyTorch for providing an excellent deep learning framework.
- The Sentinel-2 mission for providing high-quality satellite imagery.
