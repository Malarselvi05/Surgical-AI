# 🔬 SurgicalAI 
### AI Arthroscopic Surgical Performance Evaluator
**Ceaser's Medathon 2026 — Problem Statement #1**  
*Dept. AI & Data Science · Coimbatore Institute of Technology*

[![Medathon-1st-Prize](https://img.shields.io/badge/🥇_Medathon_2026-1st_Prize_Winner-gold?style=for-the-badge&logo=award)](https://github.com/Malarselvi05/Surgical-AI)
[![Python-Version](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## 🏆 CHAMPION — 1st PRIZE WINNER
**We are proud to announce that SurgicalAI v3 secured the 1st Prize at Ceaser's Medathon 2026 for its groundbreaking approach to automating surgical training feedback.**

### 🌟 Why We Won: Key Innovations
- **ASSET-Standard Compliance**: Unlike generic motion trackers, SurgicalAI implements the *Arthroscopic Surgery Skill Evaluation Tool* (ASSET) standard, providing clinically valid 0-100 scores for Stability, Efficiency, Precision, and Speed.
- **Phase-Aware Intelligence**: The system doesn't just track motion; it identifies the specific surgical phase (e.g., *Suture Passage*, *Tendon Harvest*) to contextualize feedback.
- **Zero-Manual-Intervention**: Built-in support for YouTube URLs and automated frame extraction means a surgeon can go from a recording to a PDF report in 3 clicks.
- **Hybrid Classification**: Uses a combination of Support Vector Machines (SVM) and Percentile Ranking against the ArthroPhase dataset to ensure fair and accurate skill leveling.

## 🏆 Project Vision: Closing the Feedback Loop
Today, surgical training relies on subjective mentor feedback and inconsistent manual reviews. **SurgicalAI v3** transforms raw arthroscopic recordings into objective, ASSET-aligned performance data. 

**Zero new hardware. Zero manual labeling. Zero inconsistency.**

### Three Outputs — Ready for Submission
The system is built to provide verifiable, physical, and digital proof of performance:

1. **📊 Live Analytics Dashboard**: Real-time interactive Streamlit interface with radar charts, stability timelines, and skill badges.
2. **📄 Hospital-Grade PDF Report**: A professional A4 report generated via ReportLab, designed for the trainee’s official clinical file.
3. **🎯 Annotated Trajectory Frame**: Visual AI proof—every instrument tip coordinate is tracked and drawn over the raw surgical frames to verify tracking precision.

---

## 🚀 Quick Start (Windows / Mac / Linux)

| Step | Action | Command |
| :--- | :--- | :--- |
| **1** | Install Python 3.10+ | - |
| **2** | Install Dependencies | `pip install -r requirements.txt` |
| **3** | Launch Dashboard | `streamlit run app.py` |

> [!TIP]
> **Windows Users**: You can simply double-click `run.bat` to automate installation and launch.

---

## 🏗 The 8-Step Dynamic Pipeline
The core strength of v3 is its **Zero-Manual-Intervention** architecture. Every component is scriptable and runs end-to-end.

1. **Adaptive Frame Extraction**: Support for YouTube URLs, local `.mp4/.avi`, or the ArthroPhase dataset.
2. **Multi-Strategy Detection**: The AI tries 6 distinct color-family families to find the instrument in any lighting condition.
3. **Phase-Aware Alignment**: Automatically identifies the surgical phase (e.g., *ACL Reconstruction*, *Diagnosis*) to context-match feedback.
4. **ASSET Metric Engine**: Computes scale-normalized scores for **Stability, Efficiency, Precision, and Speed**.
5. **Statistical Baseline Mapping**: (Optional) Dynamically ranks the surgeon against the entire 27-surgery ArthroPhase dataset.
6. **Multi-Method Classification**: Skill level is assigned using either **ML (SVM)**, **Percentile Ranking**, or **Clinical Rule-Bands**.
7. **Dynamic Clinical Feedback**: Generates phase-aware clinical paragraphs. *No two reports are identical.* 
8. **Automated Documentation**: Final assembly of PDF report and visual trajectory overlays.

---

## 📈 Metrics & Skill Benchmarking
We utilize the **ASSET (Arthroscopic Surgery Skill Evaluation Tool)** standard for clinical validity.

| Metric | Factor | Importance |
| :--- | :--- | :--- |
| **📷 Stability** | Inverse CV of motion magnitude | 35% |
| **📐 Efficiency** | Path directness (Ideal Path / Actual Path) | 25% |
| **🎯 Precision** | Root-mean-square deviation from target | 25% |
| **⚡ Speed** | Velocity consistency and flow | 15% |

### Skill Equivalent Mapping
*   **Expert (≥ 80)**: Fellowship-trained consultant level.
*   **Advanced (≥ 60)**: Senior Trainee (PGY4-5).
*   **Intermediate (≥ 40)**: Junior Resident (PGY2-3).
*   **Novice (< 40)**: Medical Student / Foundation.

---

## 📂 Multi-Input Flexibility
- **Mode 1 — YouTube Intelligence**: Paste any surgical YouTube URL. The AI downloads, extracts frames, and analyzes without any local files required.
- **Mode 2 — Dataset Research**: Direct integration with the **ArthroPhase Dataset** (Zenodo 14288900). Supports processing entire directories of surgery segments.

---

## 🛠 Project Structure
```text
SurgicalAI_v3/
├── app.py                  # Core Streamlit Application
├── src/                    # Logic Engine
│   ├── extractor.py        # Computer Vision Tracking
│   ├── metrics.py          # ASSET Scoring Logic
│   ├── feedback.py         # Dynamic Feedback Engine
│   ├── report_generator.py # PDF A4 Generator
│   ├── classifier.py       # ML/Rule Skill Classification
│   └── video_processor.py  # YouTube/Video Handlers
├── outputs/                # Persistence Layer (PDFs & PNGs)
├── dataset/                # Analysis targets
└── run.bat                 # One-click Windows Launcher
```

---

## 🛠 Tech Stack
| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend/UI** | **Streamlit** | Real-time interactive dashboard & state management. |
| **Visualization** | **Plotly** | Vector-grade gauges, radar charts, and stability timelines. |
| **Computer Vision** | **OpenCV** | Frame extraction & adaptive color-space detection. |
| **Data Processing** | **Pandas / NumPy** | Metric computation & statistical baseline analysis. |
| **Report Generation** | **ReportLab** | High-fidelity, hospital-grade A4 PDF production. |
| **Machine Learning** | **Scikit-Learn** | SVM-based skill level classification & percentile ranking. |
| **Video Engine** | **yt-dlp** | Seamless YouTube sourcing & background downloading. |

---

## 🔄 Project Execution Flow (End-to-End)
How it works from clicking **Run** to the final **PDF**:

1.  **Sourcing**: The system accepts a YouTube link or local file and initializes a temporary extraction workspace.
2.  **Decompilation**: Video is broken down into discrete frames; surgical phases are automatically detected from ArthroPhase metadata if available.
3.  **Adaptive CV Tracking**: Our proprietary multi-strategy pipeline tries multiple color-space families (Hue/Saturation/Value) to trace the instrument path across 100% of frames.
4.  **Kinematic Calculation**: Raw (X,Y) coordinates are transformed into 5 ASSET-aligned metrics—calculating jitter, path directness, and precision deviation.
5.  **Benchmarking**: The surgeon’s composite score is mapped against active ArthroPhase baselines to determine clinical standing (e.g., *Novice to Expert*).
6.  **Instructional Synthesis**: The Feedback Engine matches scores to clinical rules to generate specific, actionable practice recommendations.
7.  **Final Assembly**:
    -   **GUI**: Dashboard updates with dynamic charts.
    -   **Vision**: An annotated frame overlay is created as tracking proof.
    -   **Document**: A professional PDF is rendered, combining metrics, charts, and analysis into a one-page printable report.

---

## 📖 Citation & Research Base
- **ArthroPhase Dataset**: BahariMalayeri et al. (Balgrist University Hospital, 2024). DOI: `10.5281/zenodo.14288900`.
- **Clinical Standards**: ASSET (PMID: 31948719) and DASS (Anetzberger et al., 2022).

---
*Created by the CIT Dept. AI & Data Science Team for Ceaser's Medathon 2026.*
