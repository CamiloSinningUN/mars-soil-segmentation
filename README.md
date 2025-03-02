# Martian Soil Segmentation: U-Net & Deep Learning Approaches

This repository contains the code, experiments, and documentation for a deep learning challenge (Polimi) project focused on semantic segmentation of Martian soil images. The project was developed as part of a Deep Learning course and showcases extensive experimentation with U-Net based architectures and various enhancements.

![image](https://github.com/user-attachments/assets/679ae63f-214a-403c-a2c1-ab9b998ecf00)


## Overview

- **Objective:**  
  Perform semantic segmentation of Martian soil images into five distinct categories using state-of-the-art deep learning methods.

- **Dataset:**  
  A collection of 12,637 grayscale Martian soil images (64x128 pixels) with a split of 2,615 training images and 10,022 test images.

- **Key Techniques:**  
  - **Data Preprocessing & Outlier Detection:**  
    Utilized PCA, t-SNE, DBSCAN, and K-Means to identify and remove images containing irrelevant features (e.g., alien artifacts).
  - **Data Augmentation:**  
    Employed Albumentations for rotation, flipping, cropping, and also incorporated CutMix from Keras_cv to diversify the limited training data.
  - **Model Architecture:**  
    Experimented with multiple U-Net variants including Attention U-Net and Squeeze-Excitation modules. The final model features an enhanced U-Net design with up to 600 MB in size, achieving a significant boost in performance.
  - **Loss Functions & Optimization:**  
    Tested various loss functions (e.g., Weighted Categorical Cross-Entropy, Dice Loss) and optimizers (Adam, AdamW, etc.), with AdamW and a modified loss yielding the best performance.
  - **Postprocessing:**  
    Applied test-time augmentation (TTA) to further improve predictions.

- **Performance:**  
  The final model achieved a mean IoU of **71.59%** on the public leaderboard.

## Folders

This repository has the following folders,

* **SparseCateogoricalCrossEntropy Arc**: This consists of most meaningful models developed under the SparseCateogoricalCrossEntropy loss function
* **WeightedCateogoricalCrossEntropy Arc**: This consists of most meaningful models developed under the WeightedCateogoricalCrossEntropy loss function

## Contributors
* [Matteo Panarotto](https://github.com/MatteoPana)
* [Camilo José Sinning López](https://github.com/CamiloSinningUN)
* [Oliver Stege](https://github.com/Smrevilo)
