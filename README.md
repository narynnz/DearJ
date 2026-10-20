# พฤติการณ์ที่ตาย (Manner of Death: Dear. J)

**Interactive Mystery Short Film Web Experience**  
Senior Project (CMM 499) • Division of Computer and Information Technology • KMUTT

> **"Manner of Death (Dear. J)"** is an interactive short film web experience in the investigative/mystery genre. Viewers take on the role of police officer "J" investigating the death of his lover "Dear", choosing investigative actions under time constraints to uncover the truth behind her demise.

---

### Project Overview
- **Project Type**: Senior Project (CMM 499)
- **Institution**: Division of Computer and Information Technology, Faculty of Industrial Education and Technology, King Mongkut’s University of Technology Thonburi (KMUTT)
- **Architecture**: Single-Page Static Web Application (Zero-Build)
- **Core Stack**: HTML5, Vanilla JavaScript (ES6+), Tailwind CSS (CDN)
- **Media Delivery**: High-Throughput Video & Audio Streaming via BunnyCDN
- **Copyright & License**: [Copyright © 2026 KMUTT](COPYRIGHT) (All rights reserved)

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [About Dear. J Website](#about-dear-j-website)
3. [Key Features](#key-features)
4. [Tech Stack](#tech-stack)
5. [Requirements](#requirements)
6. [Getting Started (Local Development)](#getting-started-local-development)
7. [Available Scripts](#available-scripts)
8. [Project Structure](#project-structure)
9. [Project Credits & Academic Attribution](#project-credits--academic-attribution)
10. [Copyright & License](#copyright--license)

---

## About Dear. J Website

### Synopsis
The interactive short film **"Manner of Death (Dear. J)"** centers on **J**, a 28-year-old police investigator who is suddenly confronted with the untimely, mysterious death of his lover **Dear**, a 25-year-old graphic designer. 

The website simulates the perspective of J as he conducts an urgent investigation to differentiate between the **Manner of Death** (*พฤติการณ์ที่ตาย*) and the **Cause of Death** (*สาเหตุการตาย*). Viewers (termed **"Viewsers"**) are presented with on-screen branch points where they must decide which clues to examine and which interrogation lines to pursue within a strict time limit. 

At the conclusion of the experience, the system evaluates the viewer's deductions through critical case questions. Viewers who complete the investigation receive a personalized digital movie ticket that can be downloaded and shared across social media, followed by an audience evaluation survey.

---

## Key Features

- **Pre-Release Countdown Screen**: Built-in countdown timer overlay with smooth fade-out and automatic expiration checking.
- **Parallax Welcome Screen**: Dual-column looping poster reels (`animate-scroll-up` / `animate-scroll-down`) with smooth entrance transitions.
- **Custom HTML5 Video Player**: Seamless custom controls featuring play/pause, interactive progress seek bar, volume toggle, and fullscreen support.
- **Interactive Timed Choices**: Floating interactive decision buttons with 15-second and 30-second animated progress bars. If the timer expires, the primary branch is automatically selected.
- **Video Preloading Pipeline**: Intelligently pre-fetches upcoming video branch assets in the background to ensure instantaneous playback transitions.
- **3D Flipping Educational Cards**: Interactive 3D flip cards explaining the 5 categories of Manner of Death as defined by NAME (National Association of Medical Examiners) and Thai legal statutes:
  1. **Suicide** (*การฆ่าตัวตาย / อัตวินิบาตกรรม*)
  2. **Homicide** (*ถูกผู้อื่นทำให้ตาย*)
  3. **Natural** (*ตายโดยธรรมชาติ*)
  4. **Accident** (*เสียชีวิตจากอุบัติเหตุ*)
  5. **Undetermined** (*ไม่ปรากฏเหตุแน่ชัด*)
- **Flashlight Character Relation Map**: Dynamic radial gradient mask following the cursor across the character relationship diagram for an investigative searchlight effect.
- **Commemorative Ticket Generator & Download**: Generates a souvenir movie ticket at the end of the film with programmatic blob download and fallback tab opening.
- **Ambient Audio Control**: Background soundtrack (BGM) toggle that gracefully pauses during video playback and resumes appropriately.

---

## Tech Stack

This project is built as a pure, zero-build client-side static web application:

| Layer | Technology | Usage |
| :--- | :--- | :--- |
| **Markup & Structure** | **HTML5** | Semantic web layout and native `<video>` / `<audio>` integration |
| **Styling & UI** | **Tailwind CSS** (via CDN) | Utility-first responsive design (`https://cdn.tailwindcss.com`) |
| **Interactivity** | **Vanilla JavaScript (ES6+)** | State machines, time-based choices, event listeners, blob downloads |
| **Typography** | **Google Fonts (Athiti)** | Clean Thai & Latin typography |
| **Iconography** | **Google Material Icons** | UI icons for playback controls |
| **Content Delivery** | **BunnyCDN** | High-throughput video, audio, and high-resolution asset streaming |
| **Feedback Survey** | **Google Forms** | Academic research and audience satisfaction survey integration |

---

## Requirements

To run and experience the project locally, you will need:

1. **Modern Web Browser**:
   - Google Chrome (recommended for optimal video autoplay and fullscreen support)
   - Microsoft Edge
   - Mozilla Firefox
   - Apple Safari
2. **Device Recommendation**:
   - **PC or Laptop** is strongly recommended for widescreen cinematic aspect ratios and precision cursor interactions.
3. **Network Connection**:
   - High-speed broadband or Wi-Fi connection is recommended because all cinematic video clips stream directly from BunnyCDN.
4. **Local HTTP Server** *(Recommended)*:
   - Any basic static file server (e.g., VS Code Live Server or Python 3) to prevent browser `file://` cross-origin restrictions when downloading ticket blobs.

---

## Getting Started (Local Development)

### 1. Clone the Repository
Clone the repository to your local machine using Git:

```bash
git clone https://github.com/narynnz/DearJ.git
cd DearJ
```

### 2. Run Locally

Choose any of the following methods to serve the project:

#### Method A: VS Code Live Server (Recommended)
1. Open the project folder in **Visual Studio Code**.
2. Install the **Live Server** extension (by Ritwick Dey) if you haven't already.
3. Right-click on `index.html` in the file explorer.
4. Select **"Open with Live Server"**.
5. Your default browser will automatically open `http://127.0.0.1:5500/index.html`.

#### Method B: Python 3 Built-in Server
If Python 3 is installed on your system, run:

```bash
python -m http.server 3000
```

Then open your browser and navigate to:
```text
http://localhost:3000
```

#### Method C: Direct Browser Launch
You can double-click `index.html` or open it directly in any browser:
```text
file:///path/to/DearJ/index.html
```
> [!NOTE]
> While most features work via direct file access, running through a local web server (Method A or B) is recommended to prevent browser security policies from restricting asynchronous media fetching and ticket downloads.

---

## Available Scripts

This project is architected as a pure, lightweight static web application. 

- **Build Commands**: There is **no build or compilation step required**. All styling, scripts, and media are linked and executed directly in the browser.
- **Execution**: To run the project, simply start any local static HTTP server as described in [Getting Started](#getting-started-local-development).

---

## Project Structure

The repository maintains a clean, minimalist structure:

```text
DearJ/
├── COPYRIGHT        # Senior project copyright and institutional rights notice
├── index.html       # Complete Single-Page Application (HTML, CSS, JS, CDN links)
└── README.md        # Comprehensive project documentation
```

### Asset Delivery Architecture
To keep the Git repository lightweight, all heavy media files (MP4 video scenes, MP3 audio tracks, and high-resolution JPEG/PNG artwork) are hosted on **BunnyCDN**.

---

## Routes

### In-Page Anchor Navigation
The application uses smooth-scrolling anchor links for its primary navigational sections:

| Anchor | Section | Description |
| :--- | :--- | :--- |
| `#home` | **Landing & Cinema** | Welcome overlay, hero banner, tutorial video, and interactive film player |
| `#manner` | **Manner of Death** | 3D flip card showcase detailing the 5 NAME & Thai legal manners of death |
| `#character` | **Character Map** | Interactive relationship chart with searchlight cursor effect |
| `#member` | **Production Team** | Senior project creators and faculty advisor credits |

---

### Production Considerations
- **HTTPS Enforcement**: Always deploy with HTTPS enabled. Modern browsers require secure contexts for autoplaying muted video and for accessing certain media permissions.
- **CORS Configuration**: If you host your own media or ticket assets, ensure that the origin server or CDN sends appropriate `Access-Control-Allow-Origin: *` headers to allow blob downloads via JavaScript.

---

## Project Credits & Academic Attribution

This project is part of a **Senior Project (CMM 499)** conducted at:
- **Division of Computer and Information Technology**
- **Faculty of Industrial Education and Technology**
- **King Mongkut’s University of Technology Thonburi (KMUTT)**

### Production Team
| Name | Role |
| :--- | :--- |
| **Kanwara Prikkong** (กัญญ์วรา พริกคง) | Producer & UX/UI Designer |
| **Nalinrat Mahakunakorn** (นลินรัตน์ มหาคุณากร) | Director & Developer |

### Project Advisor
- **Aj. Natthapong Prasertsang** (อาจารย์ ณัฐพงษ์ ประเสริฐสังข์) Project Advisor

---

## Copyright & License

Copyright © 2026 King Mongkut’s University of Technology Thonburi. All rights reserved.

This software, documentation, media assets, and related files are proprietary to King Mongkut's University of Technology Thonburi and the project authors. No part of this software or related media may be reproduced, distributed, or transmitted in any form without prior written permission from the copyright owners. For full terms, refer to the [COPYRIGHT](COPYRIGHT) file.
