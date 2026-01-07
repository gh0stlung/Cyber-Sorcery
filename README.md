<div align="center">

# CYBER SORCERER
### NEURAL // INTERFACE // AR

[![Version](https://img.shields.io/badge/VERSION-1.0-neon.svg?style=for-the-badge&color=A020F0)](./)
[![Stack](https://img.shields.io/badge/TECH-MEDIAPIPE-blue.svg?style=for-the-badge&color=00ffcc)](./)
[![Privacy](https://img.shields.io/badge/PRIVACY-LOCAL_ONLY-green.svg?style=for-the-badge&color=44cc11)](./)

<br/>

[ **🚀 LAUNCH INTERFACE** ](./index.html)

</div>

---

### ::: SYSTEM OVERVIEW

**CYBER SORCERER (V1.0)** is a browser-based Augmented Reality (AR) interface designed to overlay Dr. Strange-inspired visual effects onto reality using neural hand tracking.

* 🚫 **No Backend:** Runs entirely client-side.
* 🚫 **No Install:** Works instantly in the browser.
* ⚡ **High Performance:** Powered by GPU-accelerated Canvas API.

This system acts as a "digital magic layer," translating physical hand gestures into particle physics and vector graphics in real-time.

---

### ::: CORE MODULES

#### 🔮 SORCERY ENGINE (Visuals)
* **Mandala Generator:** Procedural generation of rotating runes and geometric rings.
* **Dynamic Scaling:** Effects adhere to palm depth and orientation.
* **Chromatic Aberration:** "Cyber" filters applied to the raw video feed.

#### ⚡ PARTICLE PHYSICS (Simulation)
* **Spark System:** Gravity-based particle emission for "Peace" gestures.
* **Float Logic:** Anti-gravity floating particles for "Heart" gestures.
* **Decay Engine:** Auto-cleanup of visual artifacts to maintain 60 FPS.

---

### ::: GESTURE LIBRARY

The system recognizes 4 distinct neural command patterns:

| Gesture | Command | Visual Output |
| :--- | :--- | :--- |
| **🖐 OPEN PALM** | `CAST_SPELL` | Rotating orange mandala arrays rooted to palm center. |
| **✊ FIST** | `CHARGE_ENERGY` | Arrays contract, turn red, and vibrate (screen shake). |
| **✌️ PEACE** | `EMIT_SPARKS` | Welding sparks emit from index and middle fingertips. |
| **🫶 TWO HANDS** | `SYNC_HEART` | Floating magenta hearts spawn between hands. |

---

### ::: TECH STACK

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![MediaPipe](https://img.shields.io/badge/MediaPipe-00aaaa?style=flat-square&logo=google&logoColor=white)
![Canvas API](https://img.shields.io/badge/Canvas_API-CC6699?style=flat-square)

---

### ::: SYSTEM ARCHITECTURE

```mermaid
graph TD
    A[🎥 USER WEBCAM] -->|Raw Feed| B(MediaPipe Hands)
    B -->|Landmark Data| C{GESTURE LOGIC}
    C -->|Fist Detected| D[Trigger: Shake/Red]
    C -->|Palm Detected| E[Trigger: Mandala]
    C -->|Peace Detected| F[Trigger: Particles]
    D & E & F --> G[🎨 CANVAS RENDERER]
    G --> H[🖥️ FINAL DISPLAY]
