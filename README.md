<div align="center">

<img width="100%" alt="Banner" src="https://github.com/ninjacode911/Github/raw/main/NAVNIT%20background.png" />

# HDS - Hemorrhoids Detection System

Real-time AI-powered hemorrhoids detection running **entirely in your browser**.

**Try it live:** [hdfs.vercel.app](https://hdfs.vercel.app/)

Currently deployed at **Healing Hands Clinic**, India's top proctology clinic.

</div>

---

## Features

- **Real-time detection** — Live camera feed with bounding box overlays at ~1-2 FPS inference
- **Privacy first** — All AI processing happens locally in the browser. No patient images are sent to any server
- **9 detection classes** — Grade I, Grade II, Grade III, Grade IV, External Thrombosis, Fissure, Polyp, Skin Tag, Normal
- **AI-generated reports** — PDF reports with Gemini AI narrative, embedded screenshots, and clinical recommendations
- **HMS integration** — Connects with Hospital Management Systems via URL parameters and webhook callbacks
- **Doctor's override** — Physicians can manually select findings that take priority over AI detections
- **Cross-platform** — Works on any modern browser with camera access

## How It Works

1. Click **"Start Session"** to enable the camera
2. The AI model detects conditions in real-time with color-coded bounding boxes
3. Use **Screenshot** or **Recording** to capture findings during the examination
4. The doctor can add or override findings using the **Doctor's Detection** panel
5. Click **"Generate PDF Report"** for an AI-assisted clinical report

## Technology

| Component | Technology |
|-----------|-----------|
| **AI Model** | YOLOv11 (custom trained on hemorrhoid dataset) |
| **Inference** | ONNX Runtime Web (WebAssembly) — runs entirely in-browser |
| **Frontend** | Vanilla JavaScript + Vite |
| **Reports** | Google Gemini API + jsPDF |
| **Deployment** | Vercel |

## Architecture

The system uses the **Xenova pattern** — the camera feed plays at 60 FPS via hardware-decoded `<video>`, while AI inference runs at ~1-2 FPS in a separate **Web Worker** thread. This keeps the UI fully responsive while the model processes frames in the background. Bounding boxes are CSS-positioned `<div>` overlays that auto-scale with the video container.

## Demo

<div align="center">

<img width="100%" alt="Demo Image 1" src="https://github.com/ninjacode911/Project-Hemorrhoids-Detection-System/raw/main/Demo%20Image%201" />

<br/><br/>

<img width="100%" alt="Demo Image 2" src="https://github.com/ninjacode911/Project-Hemorrhoids-Detection-System/raw/main/Demo%20Image%202" />

</div>

## Disclaimer

This tool is intended for use by **medical professionals practicing proctology**. It is an AI-assisted examination tool and does **not** constitute a final clinical diagnosis. All findings must be verified and confirmed by a qualified physician before any treatment decisions are made.

## License

This project is proprietary software. All rights reserved. See [LICENSE](LICENSE) for details.

The source code, trained machine learning models, and training data are the exclusive property of the author and may not be copied, modified, or distributed without explicit written permission.

---

<div align="center">

**Built by [ninjacode911](https://github.com/ninjacode911)**

</div>
