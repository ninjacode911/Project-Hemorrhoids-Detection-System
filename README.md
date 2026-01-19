---
title: HDS - Hemorrhoids Detection System
emoji: 🩺
colorFrom: red
colorTo: pink
sdk: static
pinned: false
license: mit
---

#  HDS - Hemorrhoids Detection System

Real-time AI-powered hemorrhoids detection running **entirely in your browser**.

## Features
- **Zero latency** - Uses WebGPU for GPU-accelerated inference
- **Privacy first** - All processing happens locally, no data leaves your device
- **Cross-platform** - Works on any modern browser (Chrome 113+, Edge recommended)
- **9 detection classes** - Grades I-IV, external thrombosis, skin tag, fissure, polyp, normal

## How to Use
1. Click **"Start Session"** to enable your camera
2. Point the camera at the target area
3. Detections appear in real-time with bounding boxes
4. Use **Screenshot** or **Recording** to capture findings

## Technology
- **Model**: YOLOv11 (custom trained)
- **Runtime**: ONNX Runtime Web with WebGPU acceleration
- **Frontend**: Vanilla JS + Vite

## Performance
| Browser | Acceleration | Expected FPS |
|---------|-------------|--------------|
| Chrome 113+ | WebGPU | 15-30 FPS |
| Edge | WebGPU | 15-30 FPS |
| Firefox | WASM | 5-10 FPS |
| Safari | WASM | 5-10 FPS |

## Disclaimer
This tool is for educational and research purposes only. It is NOT a substitute for professional medical diagnosis. Always consult a qualified healthcare provider.The tool is intended to be used by doctors practicing proctology.
