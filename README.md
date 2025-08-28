# Crowd Density Heatmap Tool

A Python-based tool that combines **object detection** (via TensorRT YOLO engine) with **density heatmap visualization** for crowded scenes.  
The script processes video input, detects people, generates a dynamic heatmap overlay, and tracks **people counts and density metrics over time**.


---

## ✨ Features
- ⚡ **TensorRT-powered YOLO inference** for high-speed detection  
- 🔥 **Density heatmap overlay** with Gaussian smoothing  
- 📊 **Real-time statistics**: person count, density score (max/mean), temporal graph  
- 🎥 **Video file support** (MP4)  
- 🖥️ **Live visualization** with OpenCV window + saved output  

---

## 📦 Installation

```bash
git clone https://github.com/ulassakin/crowd-density-heatmap.git
cd crowd-density-heatmap
pip install -r requirements.txt
```
