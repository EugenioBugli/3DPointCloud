# 3DPointCloud 

This Repository contains code for reconstructing 3D point clouds using the Occupancy Predictions of a small and sparse subsets of points.
This work is based on Lionar, Stefan, et al. "Dynamic Plane Convolutional Occupancy Networks" Proceedings of the IEEE/CVF Winter Conference of Applications of Computer Vision, 2021.

## Table of Contents
- [Installation](#installation)
- [Architecture](#architecture)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/EugenioBugli/3DPointCloud.git
2. Install dependencies:
    ```bash
    pip install -r <Folder>/3DPointCloud/requirements.txt
3. You can run the Code directly from the [Notebook](PointCloud3D.ipynb)

## Architecture
![Alt Text](./media/architecture.png)
The Architecture used has an Encoder-Decoder structure :

### Encoder
   1. ResNetPointNet
   2. Plane Predictor
   3. UNet
### Decoder
  1. ResNet
  2. Occupancy Predictor

The obtained occupancy predictions are then used to reconstruct the mesh by using the Multiresolution IsoSurface Extraction (MISE) and the Marching Cubes algorithm
