# Grapevine Disease Detection

An educational machine learning project exploring image classification of grapevine diseases using TensorFlow.

The project focuses on building and evaluating a convolutional neural network for grapevine disease detection within a Dockerized workflow. Results are intended for learning purposes and are NOT intended for production use.

## Overview

- Image classification using TensorFlow
- Training and evaluation environment with Docker for reproducibility
- CNN model trained on a grapevine disease dataset from Hugging Face
- Evaluating performance using classification metrics

## Results

### Training Loss

![Training Loss](loss_curve.png)

### Training Accuracy

![Training Accuracy](accuracy_curve.png)

## Report

Below is a report which includes: the dataset, methodology, implementation, and results.

[CSE 168 Lab 3 - Grapevine Disease Detection](./CSE%20168_%20Lab%203%20-%20Grapevine%20Disease%20Detection.pdf)

## Repository Structure

- `train.py`: model training
- `evaluation.py`: model evaluation
- `Dockerfile`: Docker container
- `notebooks/`: experimentation and analysis
- `data/`: Hugging Face dataset
