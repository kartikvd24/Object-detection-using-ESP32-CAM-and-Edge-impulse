
# 📦 obj_dec – Microcontroller & Sensor Detection using Object Detection (YOLO-style) on Edge Devices

This project detects and classifies different **integrated circuits (ICs), microcontrollers, and sensors** using **bounding boxes** and a camera-based **object detection model**. Built using [Edge Impulse](https://www.edgeimpulse.com), this system is perfect for lab inventory automation, educational demonstrations, or embedded vision systems.

🔗 [Live Project on Edge Impulse](https://studio.edgeimpulse.com/public/666430/live)

---

## 🧠 What It Detects

The object detection model can recognize the following components from an image:

| 🧩 Component       | Description                          |
|-------------------|--------------------------------------|
| ESP32             | Generic microcontroller board        |
| ESP32-CAM         | Camera-enabled ESP32 module          |
| Arduino Uno       | Popular dev board by Arduino         |
| DS18B20           | Digital waterproof temperature sensor|
| LoRa SX1278       | LoRa transceiver module              |
| Others (Optional) | Add more via training data           |

---

## 🎯 Project Features

- 📷 Real-time object detection with **bounding boxes**
- 💻 Runs on edge devices: ESP32-CAM, Raspberry Pi, or Linux with webcam
- 📦 Trained using **Edge Impulse Object Detection pipeline**
- 🧪 Useful for:  
  - Smart inventory systems  
  - Educational electronics demos  
  - Component detection in robotics kits

---

## 🔧 Hardware Requirements

| Component     | Role                                      |
|---------------|-------------------------------------------|
| ESP32-CAM     | Captures images and runs detection        |
| Raspberry Pi  | Alternative platform for model inference  |
| Webcam        | For PC testing using Edge Impulse runner  |

---

## 🧠 Model Details

| Feature               | Value                                |
|-----------------------|--------------------------------------|
| Input size            | 320x320 RGB image                    |
| Model Type            | Object Detection (FOMO / YOLO-lite) |
| Classes               | esp32, esp32_cam, arduino_uno, ds18b20, lora_sx1278 |
| Training Tool         | Edge Impulse Studio                  |
| Deployment Format     | .eim (Linux), Arduino lib (ESP32-CAM) |

📊 **Accuracy**: Replace with your actual validation accuracy  
📉 **Loss**: Replace with your loss value from training

---

## 🚀 How to Run

### 🖥️ Test with Edge Impulse CLI + Webcam
```bash
edge-impulse-linux-runner --clean --camera
```

> This opens your webcam and classifies live video frames with bounding boxes.

### 📷 Run on ESP32-CAM
1. Export the project as an **Arduino library** from Edge Impulse
2. Open Arduino IDE → Install the library → Use example sketch
3. Upload it to ESP32-CAM
4. Open the Serial Monitor or connect to the streaming IP to see results

---

## 🧪 Example Results

_Add a few screenshots or sample image files in the `/images/` folder showing bounding boxes around each component like ESP32, Arduino Uno, etc._

Example:
```
📸 Detected: ESP32-CAM [Box: x=34, y=48, w=90, h=100, Score: 0.92]
```

---

## 📂 Project Structure

```
obj_dec/
├── model/                # Exported .eim model files
├── esp32-cam/            # Arduino code for ESP32-CAM inference
├── images/               # Screenshots of detections
├── data/                 # Sample training images (optional)
└── README.md             # Project documentation (this file)
```

---

## 📈 Future Plans

- Add support for more components (e.g., NodeMCU, Raspberry Pi Pico, sensors)
- Improve detection in poor lighting/angles
- Add real-time alert system via Blynk/Firebase
- Optimize model size for faster performance on ESP32

---

## 🤝 Contributing

Want to improve or contribute?

```bash
git clone https://github.com/kartikd/obj_dec.git
```

- Submit PRs to add new images or boards
- Improve model performance
- Enhance Arduino streaming features

---

## 📄 License

Licensed under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0)

---

> Created with 💡 by Kartik D using Edge Impulse + embedded vision 🚀
