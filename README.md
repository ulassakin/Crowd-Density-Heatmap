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
## 🚀 Usage

### Video Input
```bash
python heatmap.py \
  --engine models/edgeyolo.engine \
  --video data/crowd.mp4 \
  --save results/output_detection.mp4
```

### Arguments
| Argument            | Description |
|---------------------|-------------|
| `--engine`          | Path to TensorRT `.engine` file (required) |
| `--meta`            | Path to sidecar JSON with metadata (auto-detected if empty) |
| `--video`           | Input video path (required) |
| `--width`           | Target width (default 1280) |
| `--height`          | Target height (default 720) |
| `--fps`             | Target FPS if input missing metadata |
| `--conf-thres`      | Confidence threshold (default 0.30) |
| `--iou-thres`       | IoU threshold for NMS (default 0.50) |
| `--nms-mode`        | `agnostic` or `aware` |
| `--save`            | Output video filename |
| `--density-metric`  | Density calculation: `max` or `mean` |
| `--sigma`           | Gaussian blur sigma for heatmap |

---
