# Tesla6CamViewer
Tesla 6 Camera Viewer - Web Browser Viewer
# Steve's TeslaCam Viewer

A simple, standalone, local web app for viewing Tesla Dashcam and Sentry Mode multi-camera recordings in your browser. No installation, no server, no data upload — everything runs locally.

## Features

- **Synchronized multi-camera playback**  
  Displays up to 6 cameras in a grid: Front, Back, Left Repeater, Right Repeater, Left Pillar, Right Pillar.

- **Event information**  
  If an `event.json` file is present in the clip folder, it shows:
  - Timestamp
  - Location (city and road name)
  - Event reason and type
  - One-click button to open the estimated GPS location in Google Maps (satellite view).

- **Playback controls**
  - Playback speeds: 0.5×, 1×, 2×, 4×
  - Play/pause, ±10 second seek, previous/next clip
  - Clickable timeline with progress bar
  - Auto-advance to next clip when current clip ends (toggleable)

- **UI touches**
  - Camera labels appear on hover
  - Special blur overlay on the back camera view
  - Toggleable event info panel

## How to Use

1. **Save the file**  
   Save the provided HTML code as `index.html` (or any name ending in `.html`) on your computer.

2. **Open in a browser**  
   Double-click the file or open it in a modern browser.  
   **Recommended**: Google Chrome or Microsoft Edge (required for folder selection support).

3. **Load your TeslaCam folder**
   - Click **"Open TeslaCam Folder"**.
   - Select the **root TeslaCam folder** that contains subfolders with your saved/sentry clips (e.g., the `TeslaCam` folder on your USB drive, or a copied folder on your computer).
   - The app will scan for clips (identified by files ending in `-back.mp4`) and populate the dropdown.

4. **Select and watch**
   - Choose a clip from the dropdown, or it will auto-load the first one.
   - Videos will load and start playing in sync.
   - Use the buttons or timeline to control playback.

**Note**: Due to browser security restrictions, the folder selection is not saved — you must re-select the folder each time you open the page.

## Folder Structure Expected

The app works with the standard TeslaCam folder layout:

```
TeslaCam/
├── SentryMode_2025-12-19_10-30-15/
│   ├── 2025-12-19_10-30-15-front.mp4
│   ├── 2025-12-19_10-30-15-back.mp4
│   ├── 2025-12-19_10-30-15-left_repeater.mp4
│   ├── 2025-12-19_10-30-15-right_repeater.mp4
│   ├── 2025-12-19_10-30-15-left_pillar.mp4
│   ├── 2025-12-19_10-30-15-right_pillar.mp4
│   └── event.json (optional)
├── SavedClips_2025-12-18_...
└── ...
```

![Uploading opera_bBnR5x5A6A.jpg…]()


Clips are automatically grouped by their containing folder and sorted chronologically.

## Limitations & Tips

- Works entirely offline after loading.
- Large folders with many clips may take a moment to index.
- Video loading speed depends on your computer and drive speed.
- Folder selection (`webkitdirectory`) is only supported in Chromium-based browsers (Chrome, Edge, Opera). Firefox and Safari do not support it yet.
- No audio playback (TeslaCam videos are typically silent anyway).

## Credits

Created by Steve_Eggson
