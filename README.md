# ScreenTextTranslator

ScreenTextTranslator is a lightweight Python tool designed for viewers who watch foreign language content without official subtitle support. Using high-speed screen capture and AI-powered OCR, it detects text on your screen in real-time and overlays a translated English subtitle bar.



Key Features:

-Dual-Engine OCR: Uses separate high-accuracy models for Korean and Japanese to ensure maximum detection precision.
-Google Lens Style: Capable of automatic language detection—just point it at the text and it translates.
-Low Latency: Powered by dxcam for ultra-fast screen grabbing and GPU-accelerated EasyOCR.
-Thread-Safe Overlay: A transparent, click-through PyQt6 window that stays on top of your video player without interfering with controls.
-Noise Reduction: Built-in bilateral filtering and contrast enhancement to read text even against complex video backgrounds.

Performance Optimization:
To ensure the pace matches your movies/series:
-Targeted Scanning: Scans specific screen regions to reduce CPU/GPU load(will try to make it robust so that it will be able to view the whole screen).
-Throttled API Calls: Intelligent request management to prevent Google Translate rate-limiting.
-Non-Blocking Logic: Background threading for heavy model loading to keep the UI fluid.

Installation:
Clone the repo:

Bash:
git clone https://github.com/YourUsername/ScreenTextTranslator.git
cd ScreenTextTranslator
Install dependencies:

Bash:
pip install opencv-python dxcam easyocr googletrans==4.0.0-rc1 PyQt6 keyboard
Important Configuration:
For the OCR to "see" your video, you must disable Hardware Acceleration in your browser (Chrome/Edge/Brave) or Media Player (VLC).

Hotkeys:
Ctrl+1: Latin Mode
Ctrl+2: Japanese Mode
Ctrl+3: Korean Mode
Ctrl+4: Chinese Mode
Ctrl+5: Hindi Mode


Disclaimer:
This tool is intended for personal use and accessibility purposes. All translations are powered by the Google Translate API. Performance may vary based on GPU capabilities.
