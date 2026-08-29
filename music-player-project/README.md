# 🎵 Single-Track Music Player

A lightweight, minimal HTML5 audio player dedicated to streaming a single audio cover track seamlessly inside web browsers.

## 🚀 Features
* **Native HTML5 Controls:** Built-in volume slider, tracking bar, time elapsed, and play/pause functions.
* **Streamlined Filenames:** Clean assets layout configured with an ultra-short name (`song.mp3`) to prevent folder routing errors.
* **No Cache Delay:** Clean metadata profile for immediate load speeds.

## 📁 Project Directory Setup
Ensure your workspace folders are nested exactly as shown below for the relative directory path to successfully load:
```text
WebDev/
│
├── music-player-project/
│   ├── index.html        # Main webpage markup layout
│   └── song.mp3          # Your active music audio track file 
│
└── README.md             # This project information sheet
```

## 🛠️ Installation & Running Locally

### 1. Browser Direct Play
1. Navigate to your local computer directory containing the files.
2. Right-click on `index.html` and select **Open With** followed by your preferred browser (Chrome, Edge, Firefox).

### 2. Live Server Deployment (Recommended)
Running media assets over an active server bypasses strict modern browser context restrictions (`file:///` protocol blocks).
1. Open the project inside **Visual Studio Code**.
2. Click the **Go Live** anchor button at the lower right status tray bar.
3. The server will spin up and preview the player dynamically over `http://127.0.0.1:5500`.

## ⚙️ Built With
* **HTML5** - Structuring using foundational `<audio>` and `<source>` semantic tags.
