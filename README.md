#  Weed Detection System

A **Computer Vision** and **Machine Learning** project designed to detect weeds in agricultural fields.  
This system helps farmers and researchers identify weed growth automatically, reducing manual effort and improving crop productivity.

---

##  Overview

The **Weed Detection System** uses deep learning models trained on agricultural field images to distinguish between crops and weeds.  
It supports both **image-based** and **live camera feed** detection, making it suitable for smart farming applications.

**Key Highlights:**
- Automatic weed identification from crop images.
- Real-time detection via webcam or camera feed.
- Model training and evaluation pipeline included.
- Easy deployment on local machines or edge devices (Raspberry Pi, Jetson, etc).
- Modular structure: dataset, training, inference, and model utilities are clearly separated.

---

## Repository Structure

```
├── Crop_weed_detection_training/     # Model training notebooks and scripts
├── Data/                             # Dataset folder (crop & weed images, annotations)
├── performing_detection/             # Inference and real-time detection scripts
├── weed_detection/                   # Core detection module and utilities
├── requirements.txt                  # Python dependencies
└── README.md                         # Project documentation
```

---

##  Features

 Image preprocessing (resizing, augmentation, normalization)  
 CNN-based weed classification and detection  
 Real-time detection from camera feed  
 Custom dataset support  
 Ready for deployment on low-power devices  

---

##  Getting Started

###  Prerequisites
- Python 3.8 or higher  
- pip installed  
- GPU recommended (optional but speeds up training)

###  Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/mdarshan1810/weed_detection_system.git
cd weed_detection_system
pip install -r requirements.txt
```

---

##  Usage

###  Train the Model
1. Place your dataset in the `Data/` directory with subfolders for each class (`weed/`, `crop/`, etc.).  
2. Open and run the notebook in `Crop_weed_detection_training/` or execute the training script:
   ```bash
   python train.py
   ```
3. The trained model will be saved (e.g., `weed_detector.pth` or `model.h5`).

---

###  Run Detection
For **image-based detection:**
```bash
cd performing_detection/
python detect.py --model path/to/model.pth --input path/to/image.jpg
```

For **live camera feed:**
```bash
python live_detect.py --model path/to/model.pth
```

---

##  Model & Dataset Details

- **Model Type:** Convolutional Neural Network (CNN) or similar architecture (e.g., ResNet, MobileNet).  
- **Dataset:** Consists of annotated agricultural images — categorized as *crop* and *weed*.  
- **Training:** Uses standard augmentation and learning-rate scheduling techniques.  
- **Goal:** Achieve high accuracy in differentiating weeds from healthy crops.

---

##  Why It Matters

Manual weeding is **labor-intensive and time-consuming**.  
This system aims to:
- Automate the weed detection process.  
- Reduce excessive pesticide/herbicide usage.  
- Support **precision agriculture** and **sustainable farming**.  

---

##  Future Enhancements

- Add **semantic segmentation** for pixel-level weed identification.  
- Integrate with **drones** or **mobile robots** for field-scale weed monitoring.  
- Deploy optimized models using **TensorRT**, **ONNX**, or **TFLite**.  
- Build a **mobile/web app interface** for farmers.


---

##  Contributing

Contributions are welcome!  
If you'd like to improve this project:
1. Fork the repo  
2. Create a feature branch (`git checkout -b feature-name`)  
3. Commit your changes  
4. Push to your branch and open a Pull Request  
