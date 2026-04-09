# ✋ Air Whiteboard

**A purely browser-based, AI-powered spatial drawing application.** 
Teach, create, and express yourself using nothing but your hands — no styluses, no tablets, and no special hardware required!

Air Whiteboard leverages the power of Google's MediaPipe hand-tracking models mapped against an HTML5 Canvas to let you "draw" directly in the air through your webcam.

---

## 🌟 Key Features

- **🪄 Intelligent Hand Tracking**: Powered by MediaPipe, perfectly mapping your index finger to an on-screen cursor in real-time.
- **🎨 Dynamic Gesture Engine**: Switch seamlessly without pressing any buttons:
  - `Hover` with a single finger
  - `Draw` by pointing with two fingers
  - `Erase` by extending three fingers
  - `Clear` by waving your open palm 👋
- **🎛️ Spatial UI Interface**: A fully hidden heads-up-display that smoothly fades in when your hand hovers near the right side of your screen. 
- **🌗 AR & Board Modes**: Draw over a clean `#1a1a2e` digital whiteboard, or toggle on the real-world **AR Mode** to sketch directly on top of your live webcam feed!
- **📸 Snapshot System**: Save your creative notes and sketches locally as a lightweight PNG.
- **⚡ Frontend Native**: Fully vanilla! Built strictly relying on pure HTML, CSS, and JS. 

---

## 🕹️ The Gesture Dictionary

Our system reads specific landmark constraints on your hand skeleton to automatically trigger tools!

| Gesture | Action | Description |
| ------- | ------ | ----------- |
| ☝️ **1 Finger** | **Hover** | Acts as an uncommitted pointer. Hold it over the UI sidebar for ~0.65s to click colors or change tools via spatial selection. |
| ✌️ **2 Fingers** | **Draw** | Commits strokes to the canvas mimicking your chosen brush color and size. |
| 🖖 **3 Fingers** | **Erase** | Expands the radius of your brush and acts as a localized transparent eraser. |
| 👋 **Wave** | **Clear Board** | Wipe the entire board clean instantly by waving your flat, open palm side-to-side. |

---

## 🚀 How to Run

Because Air Whiteboard is built entirely on client-side vanilla web technologies, there's no complex build pipeline or backend needed!

**Instructions:**
1. Clone or download this project to your machine.
2. Serve the `index.html` file over a local HTTP server to avoid strict browser CORS/Webcam permission errors.
   - *Via Python:* Open your terminal in this folder and run `python3 -m http.server 8000`
   - *Via VSCode:* Click `Go Live` using the Live Server extension.
3. Open `http://localhost:8000` in your browser.
4. Your browser will prompt you for **Camera permissions**. Accept them.
5. The Mediapipe Object Tracking model takes roughly ~3 seconds to download and parse its weights. Wait for the `START DRAWING` button on the splash screen!

---

## 🛠️ Built With

* Vanilla Javascript ES5/6
* Vanilla CSS3 / HTML5 `<canvas>` API for multi-layered rendering
* [Google MediaPipe (Hands)](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)
* Google Fonts (Nunito & Bangers)

---
*Developed with love for spatial computing & AI interfaces.*