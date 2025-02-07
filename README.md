# YoloObjection
A collage project
# YOLO Object Detection using Deep Learning

## 📌 Project Overview
This project implements **YOLO (You Only Look Once) object detection** to detect and classify objects in images and videos in real time. The YOLO model is known for its speed and accuracy, making it ideal for real-world applications such as surveillance, self-driving cars, and automated inspection systems.

This implementation uses **YOLOv3** with pre-trained weights and supports detection of **80 different object classes** from the COCO dataset.

---

## 📂 Dataset & Model Files
- The model uses **pre-trained YOLOv3 weights** trained on the COCO dataset.
- The following files are required for YOLO object detection:
  - `yolov3.cfg` → Configuration file for YOLOv3 network.
  - `yolov3.weights` → Pre-trained weights file.
  - `coco.names` → List of 80 class labels.

These files will be automatically downloaded if not found in the project directory.

---

## ⚙️ Model Setup
The project ensures that the necessary YOLOv3 files are present using the following logic:
```python
if not os.path.exists(yolo_folder_path):
    os.makedirs(yolo_folder_path)

    # Download YOLO files if not found
    !wget -O "{yolo_folder_path}/yolov3.cfg" https://raw.githubusercontent.com/pjreddie/darknet/master/cfg/yolov3.cfg
    !wget -O "{yolo_folder_path}/yolov3.weights" https://pjreddie.com/media/files/yolov3.weights
    !wget -O "{yolo_folder_path}/coco.names" https://raw.githubusercontent.com/pjreddie/darknet/master/data/coco.names
```
This ensures that users do not need to manually download the required files.

---

## 🚀 How to Run
1. **Clone the repository:**
   ```sh
   git clone https://github.com/A86374/YoloObjection.git
   cd YoloObjection
   ```
2. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
   If `requirements.txt` is missing, install manually:
   ```sh
   pip install opencv-python numpy matplotlib requests
   ```
3. **Run the object detection script:**
   ```sh
   python detect.py --image path/to/image.jpg
   ```
4. **Run object detection on a video:**
   ```sh
   python detect.py --video path/to/video.mp4
   ```

---

## 📊 Results
The model detects objects in images and videos and draws bounding boxes around them.

### Example Output:
- Processed video output is saved in the **`output`** folder of the repository.
- Example output files:
  - `overpass_output.avi` (Processed video file)
  - `sample_frame.jpg` (Example frame from processed video)

---

## 🔧 Future Improvements
- Implementing **YOLOv5** for better performance.
- Deploying as a **web application** for real-time object detection.
- Adding support for custom datasets and fine-tuning.

---

## 📜 License
This project is open-source and available under the **MIT License**.

---

## 👨‍💻 Author
- **TATTA AC KIRAANN**  
  📧 Email: uk1976003@gmail.com  
  🌍 LinkedIn: [Your LinkedIn Profile](https://www.linkedin.com/in/your-profile/)  
  🏗 GitHub: [Your GitHub Profile](https://github.com/A86374/)

