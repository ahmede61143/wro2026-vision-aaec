# AAEC System (Autonomous Archaeological Extraction and Conservation)
**Team Vision Robotics — WRO 2026 Future Innovators**

---

## 📖 Project Overview

Artifacts are links to the past, giving us valuable insight into how our ancestors lived, worked, and thrived. Therefore, the extraction and conservation of these artifacts are essential for uncovering history. 

Today, traditional artifact extraction is difficult, time-consuming, and often results in further fragmentation of fragile objects, as well as modern DNA and skin particle contamination. With the **AAEC (Autonomous Archaeological Extraction and Conservation) System**, we aim to accelerate and improve the reliability of archaeological excavation processes while keeping artifacts and researchers safe.

📄 **Full Documentation:** Read our complete engineering journey, research, and testing results in our [WRO Project Report](docs/project-report.pdf).

---

## ⚙️ How It Works

The AAEC System operates using two main robotic units working together over wireless communication:

### 1. The Tower (Site Surveillance & Localization)
* **Hardware:** An 80 cm-tall stationary tower equipped with **2 HuskyLens 1 AI cameras**.
* **Function:** Placed in any corner of the archaeological site, it provides a **90° field of view** across the excavation area. 
* **Processing:** Both camera feeds are sent to a **Python script** that triangulates and calculates the artifact's general coordinates on the site.

### 2. The Extractor (Precision Excavation & Retrieval)
* **Hardware:** A mobile rover equipped with **1 HuskyLens 1 AI camera** and **two 2-axis mechanical arms** (one fitted with a delicate brush, and one fitted with an extraction claw).
* **Surface Mode:** Receives the general coordinates from the Tower's Python script, navigates to the target, uses its onboard camera to pinpoint the exact location, and carefully brushes and extracts the artifact.
* **Underground / Cave Mode:** Operates autonomously without the Tower to explore tight or hazardous underground spaces, uncovering artifacts in its path and safely bringing them to the surface.

---

## 🛠️ Tech Stack & Hardware

* **Vision & AI:** DFRobot HuskyLens 1 (3x units total)
* **Microcontrollers & Compute:** Raspberry Pi, ESP32-S3
* **Programming Languages:** Python, C++ (Arduino)
* **Actuators:** Servo-driven 2-axis mechanical arms (Brush & Claw)
* **Design & Fabrication:** Custom 3D-printed chassis and mounts

---

## 📂 Repository Structure

```text
wro2026-vision-aaec/
├── docs/               # Official WRO Project Report (PDF) and system diagrams
├── hardware/           # 3D-printable STL files, wiring schematics, and pinouts
├── tower/              # Python localization scripts and Tower camera code
├── extractor/          # Mobile robot navigation, vision tracking, and arm control
├── LICENSE             # Non-commercial license terms
└── README.md           # Project overview and setup guide
```

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd wro2026-vision-aaec
   ```
2. **Install Python dependencies (for the Tower localization script):**
   ```bash
   pip install -r requirements.txt
   ```
3. **Upload microcontroller firmware:**
   * Flash the Tower and Extractor firmware files located in `/tower` and `/extractor` to their respective boards.

---

## 📜 License & Copyright

Copyright © 2026 **Team Vision Robotics**. All rights reserved.

This project is licensed for **personal and educational use only**. You may view, study, and run this code for non-commercial purposes provided that explicit credit is given to **Team Vision Robotics**. Commercial use, redistribution for profit, or claiming credit for this work is strictly prohibited. See the [LICENSE]

This README document was written with the use of Gemini AI and was based on the project report
(LICENSE) file for full details.

