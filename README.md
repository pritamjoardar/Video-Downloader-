# ⚡ VidFetch

<p align="center">
  <strong>High-Quality Multi-Threaded Video Downloader for Windows</strong>
</p>

<p align="center">
  <a href="https://vidfetch.pritamjoardar.com/"><strong>🚀 Visit Production Site: vidfetch.pritamjoardar.com</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%20%2F%2011-blue?style=for-the-badge&logo=windows" alt="Platform: Windows" />
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python" alt="Python 3.8+" />
  <img src="https://img.shields.io/badge/Next.js-15.0%2B-black?style=for-the-badge&logo=next.js" alt="Next.js Web" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License MIT" />
</p>

---

VidFetch is an advanced, free, and open-source video downloading suite. It features a high-performance **Python Desktop App** with a sleek dark UI, custom-animated progress bars, and parallel downloads, alongside a modern **Next.js Web Landing Page** to distribute the installer.

🚀 **Live Production Application:** [vidfetch.pritamjoardar.com](https://vidfetch.pritamjoardar.com/)

> [!IMPORTANT]
> **FFmpeg is fully bundled inside the desktop application!**
> Users do not need to install FFmpeg manually or configure environment PATH variables. Everything works out-of-the-box on the first launch.

---

## ✨ Features

### 🖥️ Desktop Application
*   **Parallel Downloads:** Multi-threaded downloader where each URL gets its own progress card and queue thread.
*   **Up to 4K Quality:** Download video streams up to 4K resolution (or select 1080p, 720p, 480p, etc.).
*   **Audio Extraction:** Convert any video to high-quality MP3 format.
*   **Pause & Resume:** Complete control to suspend, resume, or cancel active download tasks.
*   **Metadata & Subtitles:** Automatically download, embed subtitles, and merge video details.
*   **Thumbnail Embedding:** Downloads and embeds the video thumbnail into the audio/video media file.
*   **Proxy Support:** Integrated proxy settings (HTTP/SOCKS5) to bypass regional restrictions.
*   **Interactive Log:** Real-time log console showing detailed network and download stages.

### 🌐 Web Landing Page (`/vidfetch-web`)
*   **Premium Aesthetics:** A stunning glassmorphic dark interface with gradient highlights and micro-animations.
*   **Live Preview Mockup:** High-fidelity interactive CSS application preview showing how the download process works.
*   **SEO Optimized:** Handcrafted with meta descriptions, Google Fonts, and standard HTML structures.
*   **Google Tag Manager (GTM):** Configured via Next.js native Script tags for speed and SEO telemetry.

---

## 📂 Project Structure

```mermaid
graph TD
    Root[VidFetch Root Workspace] --> PyApp[Python Desktop Application]
    Root --> WebApp[Next.js Landing Page App]
    
    PyApp --> Main[downloader_app.py]
    PyApp --> Spec[VidFetch.spec]
    PyApp --> Nsi[VidFetch_Installer.nsi]
    PyApp --> BuildScript[Build Installer.bat]
    
    WebApp --> NextApp[vidfetch-web/app/]
    WebApp --> NextPublic[vidfetch-web/public/]
```

### Key Workspace Files
*   [`downloader_app.py`](file:///c:/Users/prita/Desktop/video%20downloaed/downloader_app.py): Core GUI and network controller built using standard Tkinter and `yt-dlp`.
*   [`VidFetch.spec`](file:///c:/Users/prita/Desktop/video%20downloaed/VidFetch.spec): PyInstaller specification configuration to pack the script, resources, and bundled FFmpeg.
*   [`VidFetch_Installer.nsi`](file:///c:/Users/prita/Desktop/video%20downloaed/VidFetch_Installer.nsi): NSIS compiler script that packages the standalone executable into a setup installation program.
*   [`vidfetch-web/`](file:///c:/Users/prita/Desktop/video%20downloaed/vidfetch-web/): Next.js web application root.

---

## 🛠️ Installation & Development

### 1. Running & Compiling the Desktop App

#### Requirements:
*   Python 3.8 or higher
*   Microsoft Windows OS (for GUI animations and suspension APIs)

#### Setup Environment:
```bash
# Clone the repository
git clone https://github.com/pritamjoardar/Video-Downloader.git
cd Video-Downloader

# Install required dependencies
pip install -r requirements.txt
pip install pillow psutil
```

#### Run the Dev Version:
```bash
python downloader_app.py
```

#### Build Standalone Executable & Installer:
To compile the Python application into a standalone `.exe` and package it into a Windows Setup installer, make sure you have [NSIS](https://nsis.sourceforge.io/) installed, then run the batch script:
```bash
"Build Installer.bat"
```
This script will:
1. Run PyInstaller via `VidFetch.spec` to create a bundled directory in `dist/`.
2. Compile `VidFetch_Installer.nsi` using `makensis` to create the final setup installer: `VidFetch_Setup.exe`.

---

### 2. Developing the Web Landing Page

#### Requirements:
*   Node.js v18.0.0 or higher
*   npm or yarn

#### Setup & Start:
```bash
cd vidfetch-web

# Install dependencies
npm install

# Run local development server
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) to view the landing page locally.

#### Build Web Server Production Bundle:
```bash
npm run build
```

---

## ⚙️ Technologies Used

| Technology | Purpose |
| :--- | :--- |
| **Python 3** | Desktop App Core |
| **Tkinter** | Native Desktop GUI Rendering |
| **yt-dlp** | Video Metadata Fetching & Network Engine |
| **FFmpeg** | Video merging, subtitles conversion, and MP3 extraction |
| **Next.js 15+** | Landing Page Web Framework (React/TypeScript) |
| **Vanilla CSS** | Core layout, animations, and typography styles |
| **PyInstaller** | Executable compiler packaging |
| **NSIS (Nullsoft)** | Windows Installer wizard compiler |

---

## 👤 Author

*   **Pritam Joardar** - *Lead Creator* - [Portfolio](http://pritamjoardar.com/)

---

*Made with ⚡ and 🧡 by Pritam Joardar.*
