# 🎵 Single-Track Music Player

A lightweight, minimal HTML5 audio player dedicated to streaming a single audio cover track seamlessly inside web browsers.

## 🚀 Features
* **Native HTML5 Controls:** Built-in volume slider, tracking bar, time elapsed, and play/pause functions.
* **Streamlined Filenames:** Clean assets layout configured with an ultra-short name (`song.mp3`) to prevent folder routing errors.
* **No Cache Delay:** Clean metadata profile for immediate load speeds.

## 📁 Project Directory Setup
Ensure your workspace folders are nested exactly as shown below for the relative directory path to successfully load:
```text
music-player-project/
│
├── index.html          # Main webpage markup layout
├── music-cover.mp4     # Visual looping video element
├── song.mp3            # Your active music audio track file 
└── README.md           # This project information sheet
```

## 🛠️ Installation & Running Locally

### 1. Browser Direct Play
1. Navigate to your local computer directory containing the files.
2. Right-click on `index.html` and select **Open With** followed by your preferred browser (Chrome, Edge, Firefox).

### 2. Live Server Deployment (Recommended)
Running media assets over an active server bypasses strict modern browser context restrictions (`file:///` protocol blocks).
1. Open the project inside **Visual Studio Code**.
2. Click the **Go Live** anchor button at the lower right status tray bar.
3. The server will spin up and preview the player dynamically over:
   `http://127.0.0.1:3000/music-player-project/index.html?vscode-livepreview=true`

## ⚙️ Built With
* **HTML5** - Structuring using foundational `<audio>`, `<video>`, and `<source>` semantic tags.

## 🔮 Future Implementations

### RetroStream: 2D Pixel-Art Cloud Stereo
The long-term vision for this project is to scale it into a **Cloud-Decoupled Media Player**, replacing local storage requirements with cloud asset architecture and introducing an immersive visual style.

*   **Pixel-Art Aesthetic:** A retro, custom UI styled to look like a classic 80s/90s vintage cassette player and stereo system.
*   **Cloud-Decoupled Hosting:** Offloading heavy `.mp3` and `.mp4` files to cloud object storage (like Cloudflare R2 or AWS S3) to minimize local disk footprint.
*   **Optimal Web Payload:** Compressing the 2D pixel animations into short looping background video containers to eliminate browser buffering delays.

#### Planned System Architecture
```text
                       ┌──────────────────────────────────────┐
                       │       FRONTEND (User Interface)      │
                       │   Static HTML / Retro CSS Layout     │
                       └──────────────────────────────────────┘
                                          │
                        Fetches Asset URLs via HTTPS (with CORS)
                                          │
                                          ▼
                       ┌──────────────────────────────────────┐
                       │       BACKEND (Cloud Storage)        │
                       │    Cloudflare R2 or AWS S3 Bucket    │
                       └──────────────────────────────────────┘
                                   ╱              ╲
                                  ╱                ╲
          ┌────────────────────────┐              ┌────────────────────────┐
          │     music-cover.mp4    │              │        song.mp3        │
          │  (Animated Pixel Art)  │              │  (High-Fidelity Audio) │
          └────────────────────────┘              └────────────────────────┘
```
