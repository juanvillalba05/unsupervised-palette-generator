# Color Palette Generator from Artwork Images

Automatic extraction of dominant color palettes from paintings and artworks using unsupervised machine learning.

## Overview

This project develops a method to automatically identify the dominant colors in an image and generate a representative color swatch. Applied to a curated set of artworks spanning different artistic styles, the pipeline combines clustering with dimensionality reduction to both produce the palette and visualize the color distribution of each image.

## Pipeline
```
Image → Preprocessing → K-Means Clustering → Color Palette + t-SNE Visualization
```

## Key steps

- **Data collection:** 6–10 paintings selected from different artistic styles and painters
- **Preprocessing pipeline:** Image resizing, pixel array reshaping, normalization
- **Clustering model:** K-Means with hyperparameter search to determine the optimal number of clusters (k) per image using silhouette score — k is not fixed, it adapts to each image
- **Palette generation:** Each cluster centroid is mapped to its representative RGB color and displayed as a color swatch
- **Dimensionality reduction:** t-SNE projects the pixel color space into 2D for visual exploration of color distribution

## Results

The method successfully extracts coherent and aesthetically representative palettes across images with very different color profiles — from warm, golden compositions to cool, high-contrast works.

## Tech stack

- Python
- scikit-learn (K-Means, silhouette score)
- scikit-learn / openTSNE (t-SNE)
- NumPy, Pillow
- Matplotlib, Seaborn
- Jupyter Notebook

## How to run
```bash
git clone https://github.com/tu-usuario/color-palette-generator-kmeans
cd color-palette-generator-kmeans
pip install -r requirements.txt
jupyter notebook
```

## Context

Project developed as part of the Unsupervised Machine Learning course — Master's in Artificial Intelligence.
