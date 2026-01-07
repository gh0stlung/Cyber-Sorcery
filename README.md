<div align="center">

# NEURAL // CANVAS
### BROWSER-BASED VISION & GENERATIVE SYSTEM

[![License](https://img.shields.io/badge/LICENSE-MIT-000000.svg?style=for-the-badge&color=000000)](./LICENSE)
[![Platform](https://img.shields.io/badge/PLATFORM-WEB_ASSEMBLY-blue.svg?style=for-the-badge&color=007ACC)](./)
[![Privacy](https://img.shields.io/badge/PRIVACY-LOCAL_ONLY-green.svg?style=for-the-badge&color=2EA44F)](./)
[![AI](https://img.shields.io/badge/MODEL-YOLOv8_ONNX-purple.svg?style=for-the-badge&color=7028e0)](./)

<br/>

[ **🚀 LAUNCH SYSTEM** ]((https://gh0stlung.github.io/Cyber-Sorcery/)) 

</div>

---

## SYSTEM OVERVIEW

**NEURAL // CANVAS** is a local-first visual environment that bridges Computer Vision (CV) with generative logic. 

Built entirely on web standards, this system executes AI models (**YOLOv8** & **MediaPipe**) directly in the browser via WebAssembly (WASM). It transforms a standard webcam into an input device for spatial interaction and procedural art generation.

* **Real-Time Performance:** Inference happens entirely on the client device.
* **Privacy First:** Video feeds are processed in volatile memory and never leave the browser.
* **Implicit Logic:** Uses an internal node-style state machine to map vision data to visual outputs.

---

## CORE CAPABILITIES

### 🖐️ Neural Hand Tracking
* **Multi-Hand Detection:** Tracks skeletal landmarks for up to 2 hands.
* **Spatial Interaction:** Uses pinch-based and proximity-based triggers to manipulate elements.
* **Distance Heuristics:** Maps hand scale to Z-axis depth for pseudo-3D interaction.

### 👁️ Object Detection (YOLOv8)
* **WASM Inference:** Runs quantized YOLOv8 models via ONNX Runtime Web.
* **Context Awareness:** Identifies common object classes (e.g., cell phones, bottles) to influence visual generation.
* **Spatial Anchors:** Object bounding boxes act as repulsors or attractors for particle systems.
* **Automatic Fallback:** If the YOLO model fails to load or runs too slowly, the system automatically degrades to a "Hands-Only" mode to maintain framerate.

### 🎨 Generative Renderer
* **Reactive Visuals:** HTML5 Canvas rendering driven by the internal state machine.
* **Particle Systems:** Physics-based emitters influenced by hand velocity and object position.
* **Procedural Geometry:** Dynamic shapes generated based on landmark topology.

---

## INCLUDED MODEL

This repository includes a quantized version of the YOLOv8 Nano model, optimized for browser execution.

* **Path:** `models/yolov8n.onnx`
* **Format:** ONNX (Open Neural Network Exchange)
* **Optimization:** Quantized for reduced file size and faster CPU/WASM inference.

---

## RUN THE DEMO

1.  **Launch:** Open the live link (or open `index.html` on a local server).
2.  **Access:** When prompted, allow camera access.
3.  **Interact:**
    * Raise one or two hands to trigger particle arrays.
    * Hold objects (like a cell phone or bottle) to see object detection bounding boxes affecting the visuals.

---

## VISUAL LAYERS

The system cycles through distinct aesthetic states based on detection confidence and user interaction:

| Layer | Purpose | Aesthetic |
| :--- | :--- | :--- |
| **SORCERY** | Generative Art | **Cyber-Magic.** Rotating geometric arrays, neon trails, and reactive particles. |
| **DEBUG** | System Analysis | **Raw Data.** Bounding boxes, skeletal wireframes, and performance metrics. |

---

## TECH STACK

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![MediaPipe](https://img.shields.io/badge/MediaPipe-00aaaa?style=flat-square&logo=google&logoColor=white)
![ONNX Runtime](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)

---

## SYSTEM ARCHITECTURE

mermaid
graph TD
    A[🎥 CAMERA INPUT] -->|Video Frame| B[VISION ENGINE]
    
    subgraph PROCESSOR [WASM / JS RUNTIME]
        B -->|Landmarks| C(MediaPipe Hands)
        B -->|Inference| D(YOLOv8 ONNX)
        C & D --> E{STATE MACHINE}
    end
    
    E -->|Normalized Coordinates| F[IMPLICIT LOGIC]
    F -->|Draw Commands| G[CANVAS RENDERER]
    G --> H[🖥️ VISUAL OUTPUT]

 * Input: Raw webcam feed is captured.
 * Inference: Frames are processed; MediaPipe tracks skeleton, YOLOv8 scans for objects.
 * Logic: Coordinate data is normalized and passed to the internal state machine.
 * Render: The Canvas API draws the resulting visual state.
PRIVACY & SECURITY
NEURAL // CANVAS is designed with a "Sovereign Software" philosophy.
 * ✅ Offline Capable: The system requires no internet connection after initial load.
 * ✅ Sandboxed: No user data, video, or audio is ever transmitted to a cloud server.
 * ✅ Zero Tracking: No analytics or third-party monitoring scripts.
DEPLOYMENT & STRUCTURE
This project is optimized for static hosting (e.g., GitHub Pages).
Project Structure:
/root
├── index.html        # Single-file entry point (Logic + UI)
└── /models           # Quantized YOLOv8 ONNX weights

Requirements:
 * HTTPS: Browsers require a secure context (HTTPS) to access the webcam.
 * WebGL: A GPU-enabled browser is recommended for optimal inference speed.
USE CASES
 * Creative Coding: Prototyping gestural interfaces for installation art.
 * Experimental UI: Researching spatial interaction patterns.
 * Portfolio Demo: Showcasing heavy AI model optimization in web environments.
<!-- end list -->

