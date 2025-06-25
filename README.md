# Robust-Image-Captioning-and-Model-Analysis

**Course:** CS60010 - Deep Learning

This repository contains the official implementation for the project "Robust Image Captioning, Benchmarking, and Model Analysis". The project involves developing a custom image captioning model, evaluating its robustness against a modern Vision-Language Model (VLM), and building a classifier to perform model attribution.

## Table of Contents
- [Project Overview](#project-overview)
- [Methodology](#methodology)
- [Dataset](#dataset)
- [Setup and Installation](#setup-and-installation)
- [How to Run](#how-to-run)
- [Project Structure](#project-structure)
- [Key Results](#key-results)
  
## Project Overview

This project is divided into three main parts:

1.  **Part A: Custom Captioning Model:** Implementation and fine-tuning of a Transformer-based encoder-decoder model (ViT-GPT2) for image captioning. Its performance is benchmarked against a zero-shot Small Vision-Language Model (SmolVLM).

2.  **Part B: Robustness Analysis:** A systematic study of how the custom model and the baseline SmolVLM perform under various levels of input image degradation (patch-wise occlusion).

3.  **Part C: Model Attribution Classifier:** Development of a BERT-based text classifier to determine if a generated caption originated from our custom model or the SmolVLM, based on the text and occlusion level.

## Methodology

-   **Image Encoder:** A pre-trained Vision Transformer (`vit-small-patch16-224`) is used to extract features from input images.
-   **Text Decoder:** A pre-trained Transformer-based decoder (`GPT-2`) generates captions conditioned on the image features.
-   **Baseline Model:** The off-the-shelf `SmolVLM` is used for zero-shot performance comparison.
-   **Attribution Classifier:** A fine-tuned `bert-base-uncased` model is used for binary text classification.
-   **Frameworks:** The project is implemented primarily using `PyTorch` and the `Hugging Face Transformers` library.

## Dataset

The project uses a custom dataset provided for the assignment.

-   **Download Link:** [Dataset](https://drive.google.com/file/d/1FMVcFM78XZE1KE1rlkGBpCdcdI58S1LB/view?usp=sharing)
-   Please download the dataset and place it in a `data/` directory within the project root
