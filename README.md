# YOLOv8 Object Detection and Tracking

## 1. Project Overview

This project uses YOLOv8 to detect and track three object classes:

- Cat
- Dog
- Car

The model was trained using a custom dataset and tested on a 5-second video.

## 2. Model

- Model: YOLOv8n
- Pretrained weights: yolov8n.pt
- Epochs: 50
- Image size: 640
- Batch size: 16
- Training environment: Google Colab
- GPU: NVIDIA Tesla T4

## 3. Dataset

| Class | Number of Images |
|---|---:|
| Cat | 200 |
| Dog | 217 |
| Car | 151 |
| Total | 568 |

The dataset was divided into training, validation, and test sets.

## 4. Test Performance

| Class | Precision | Recall | mAP50 | mAP50-95 |
|---|---:|---:|---:|---:|
| Cat | 0.684 | 0.611 | 0.597 | 0.255 |
| Dog | 0.963 | 0.773 | 0.924 | 0.536 |
| Car | 0.937 | 0.869 | 0.921 | 0.745 |
| Overall | 0.861 | 0.751 | 0.814 | 0.512 |

## 5. Object Tracking

Object tracking was performed using the ByteTrack tracker.

- Input video duration: 5 seconds
- Resolution: 1280 × 720
- Frame rate: 30 FPS

The tracking results are available in `결과/combined_video_tracked.mp4`.

## 6. Results

The model showed good detection performance for dogs and cars. However, cat detection performance was relatively low.

Some dogs were incorrectly classified as cats, and cats in the demonstration video were not consistently detected.

## 7. Dataset Sources

- Cat: [Roboflow Universe - Cat](https://universe.roboflow.com/plywoodv1/cat-npklm/dataset/1)
- Dog: [Roboflow Universe - Dog](https://universe.roboflow.com/d6402990ws/dog-bfshs/dataset/1)
- Car: [Roboflow Universe - Car](https://universe.roboflow.com/fakiha/car-detection-sfgya/dataset/2)

The datasets are distributed under the CC BY 4.0 license.

## 8. Files

- `결과/best.pt`: Trained YOLOv8 model
- `결과/combined_video_tracked.mp4`: Object detection and tracking result
- `dataset/data.yaml`: Dataset configuration
