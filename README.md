# 3D Object Detection Using YOLO Algorithm on LiDAR Dataset

This repository demonstrates 3D object detection and visualization using the Lyft Level 5 dataset for autonomous vehicles. It utilizes LiDAR point cloud data and renders 3D visualizations with annotations for object detection and analysis. The project provides insights into preprocessing, rendering, and visualizing LiDAR data using tools such as the Lyft SDK and custom rendering utilities.

---

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Workflow and Code Details](#workflow-and-code-details)


---

## Overview

The goal of this project is to leverage the Lyft Level 5 dataset to:
- Process and visualize LiDAR point cloud data.
- Render 3D bounding boxes and projections for annotated objects.
- Explore attributes, instances, and annotations associated with the LiDAR data.

The dataset includes LiDAR scans, camera images, annotations for objects, and metadata about sensors and vehicles.

---

## Dataset

### Lyft Level 5 Dataset
- **Source**: [Kaggle 3D Object Detection for Autonomous Vehicles](https://www.kaggle.com/c/3d-object-detection-for-autonomous-vehicles/data).
- **Contents**:
  - LiDAR point cloud data.
  - Annotated 3D bounding boxes.
  - Sensor metadata and ego vehicle pose.

---

## Key Features

1. **Interactive Visualizations**:
   - Render LiDAR point clouds in 3D space with object annotations.
   - Plot point cloud projections (XY, XZ, YZ planes).
   - Display camera sensor data and associated annotations.

2. **Data Preprocessing**:
   - Conversion of raw LiDAR data into usable 3D plots.
   - Transformation to ego vehicle coordinates for accurate alignment.

3. **Rendering and Animation**:
   - Sequential rendering of LiDAR frames to create animations of point cloud data.
   - Save visualizations as images or animated GIFs for further analysis.

4. **Attribute and Instance Exploration**:
   - Inspect object attributes, categories, and instances using the Lyft SDK.

---

## Workflow and Code Details

### Step 1: Dataset Loading and Exploration
- Loaded the Lyft Level 5 dataset using the `LyftDataset` class.
- Explored categories, attributes, and scenes to understand the data structure.

### Step 2: Preprocessing LiDAR Point Clouds
- Extracted LiDAR data (`LIDAR_TOP`) for individual frames.
- Transformed points to the ego vehicle's reference frame using calibration and pose metadata.

### Step 3: Rendering and Visualization
- Implemented:
  - 3D point cloud visualizations.
  - 2D projections on different axes (XY, XZ, YZ).
- Used Matplotlib's 3D plotting capabilities to render annotated bounding boxes.

### Step 4: Animation Creation
- Sequentially rendered LiDAR frames in a scene.
- Combined frames into an animated GIF to visualize the movement of the ego vehicle and surrounding objects.

---

