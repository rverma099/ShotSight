# ShotSight : Golf Ball & Hole Detection with YOLOv11

**ShotSight** is a computer vision project that detects the precise moment a golf ball enters the hole — the perfect putt. Using YOLOv11 and annotated video data, this project recognizes and tracks both the golf ball and golf hole in real time, overlaying a clear message when the shot is made:

- Detects **Golf_ball** and **Golf_hole** using a custom-trained YOLOv11 model
- Calculates the distance between the ball and the hole
- Dynamically displays:  
  🎯 `"The putt is achieved"` when the ball enters the hole  
- Saves and visualizes detection results in the output video

1. Dataset Preparation (Roboflow)
- Create a project on [Roboflow]
- Define two classes:
  - `Golf_ball`
  - `Golf_hole`
- Upload this [golf video] at 20 FPS
- Annotate all frames and label every Golf_ball and Golf_hole

### 2. Export the Dataset
- Download the dataset as a ZIP file in **YOLO format**

### 3. Model Training
- Train using YOLOv11s (Ultralytics)
- Try parameters like:
- `batch=04`
- `imgsz=640`
- `epochs=30`
- Evaluate performance and fine-tune if needed

### 4. Run Inference on the Video
- Load your trained model (`best.pt`)
- Detect Golf_ball and Golf_hole in each frame
- Check if ball center lies inside the hole's bounding box
- If it does, overlay:



