YOLO Object Detection – Hackathon2 Project
This document contains the README content for our YOLO-based object detection project. 

Dataset links:

https://drive.google.com/drive/folders/1nyc16o3klxFyyMpXBmy7Y2becvUx-4Im?usp=drive_link

📂 Project Structure

Hackathon2_scripts/
│

├── train/
       
     |-── images/                
     ├── labels/  

├── test/

     |-── images/                
     ├── labels/                

├── val/

     |-── images/                
     ├── labels/  

├── classes.txt            # Class names

├── train.py               # Script to train YOLO model

├── predict.py             # Script to run inference

├── visualize.py           # Script to display predictions visually

├── yolo_params.yaml       # YOLO configuration file

├── yolov8s.pt             # Pretrained YOLO model weights (if included)

├── setup_env.bat / .sh    # Optional environment setup script

└── README.md

⚙️ Requirements

- Python 3.8+
- pip
- Recommended: virtual environment
- GPU (optional but faster for training)

Install dependencies:
pip install -r requirements.txt

Typical YOLO requirements:
pip install ultralytics opencv-python numpy matplotlib

🏋️‍♂️ Training the Model

Edit yolo_params.yaml to match your dataset paths and classes. 
Then run:

python train.py
The model weights and logs will be saved automatically.

🔎 Running Inference

To predict on a single image:

python predict.py --source path_to_image.jpg
Or modify predict.py to point to your test images folder.

🎨 Visualizing Predictions

To open the built-in visualization window:

python visualize.py
This displays bounding boxes, class labels, and confidence scores.
To save the predictions to files, edit visualize.py and add:
cv2.imwrite('outputs/result.jpg', image_with_boxes)

📊 Output Examples

- Bounding boxes drawn on detected objects
- Confidence scores
- Class names displayed on images
(Include sample screenshots in the repo under a /results folder)

📝 Notes

- Make sure the classes.txt file matches the trained model’s classes.
- yolo_params.yaml must point to your dataset’s correct paths.
- If you’re using GPU (CUDA), ensure PyTorch/Ultralytics YOLO is installed with GPU support.

🙌 Acknowledgements

- Ultralytics YOLOv8: https://github.com/ultralytics/ultralytics
- OpenCV



