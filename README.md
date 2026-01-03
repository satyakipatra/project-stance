# Project Stance
This project uses computer vision to analyze badminton match videos and extract performance metrics such as player positions, speed, court coverage, rally duration, and shot patterns. The goal is to enable automated, data-driven insights for player performance analysis and training.
To implement this, a YOLO pre-trained model is used for player detection and a trained model (using >8k+ labelled image data) for accurate metric calculations. 


## Notebooks

| File Name              | Description |
|------------------------|-------------|
| 01_upload_file         | Handles video ingestion, validation, and preprocessing. Loads match footage, extracts metadata (FPS, resolution, duration), and prepares frames for downstream analysis. |
| 02_player_detection    | Detects badminton players in each frame using a trained YOLO-based object detection model. Outputs bounding boxes, confidence scores, and player class labels. |
| 03_player_tracking     | Assigns persistent IDs to detected players across frames using multi-object tracking, enabling continuous player trajectories throughout the rally and match. |
| 04_player_stats        | Computes player-level performance metrics such as movement speed, distance covered, court coverage heatmaps, and positional statistics derived from tracked trajectories. |
| 05_train_yolo          | Creates the trained model instance best.pt from the labelled data with only one class i.e. shuttlecock. This model will further be used for detection of shuttlecock in videos. |

### Player Tracking

![Screenshot 2025-12-31 011036](https://github.com/user-attachments/assets/68a6d02e-2de0-4ed2-aa5b-8eb5b4b9b8af)

### Player Statistics - Court Coverage

![Screenshot 2025-12-31 011804](https://github.com/user-attachments/assets/0436b823-a8d4-4838-8c78-ea5fc7987585)

### Model Training Performance
![Trained_Model_Performance](https://github.com/user-attachments/assets/d3ed7d19-fed4-4c00-8d0c-ac9c3fcdf44a)


Copyright (c) 2025 Satyaki Patra

All rights reserved.

This source code is proprietary and confidential.
Unauthorized copying, modification, distribution, or use of this code, in whole or in part, is strictly prohibited without prior written permission from the author.
