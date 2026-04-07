# 🚀 SurgicalAI — Setup & Execution Guide

This guide provides detailed instructions on how to set up and run the SurgicalAI v3 Performance Evaluator.

---

## 📋 System Requirements
- **Python**: 3.10 or higher.
- **Tools**: `pip` (Python package manager), `git` (optional for cloning).
- **Video Library**: `ffmpeg` (recommended for frames extraction if using local video files).

---

## 🛠 Installation Steps

### 1. Clone the Repository
```bash
git clone https://github.com/Malarselvi05/Surgical-AI.git
cd Surgical-AI
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 🏃 Running the Application

To launch the interactive Streamlit dashboard, run the following command in your terminal:

```bash
streamlit run app.py
```

### Windows Users (One-Click Launch)
You can simply double-click the `run.bat` file in the root directory to automate environment detection and launch.

---

## 🎮 How to Use the Dashboard

### 1. Choose Input Mode
- **📂 Local Dataset**: Direct integration with the **ArthroPhase** dataset. Enter the archive path in the sidebar.
- **🎥 Video / YouTube**: Paste any surgical YouTube URL or a path to a local `.mp4` file.

### 2. Enter Surgeon Details
- Update the **Surgeon Name** and **ID** for the final PDF report.

### 3. Select Analysis Options
- Enable/Disable **PDF Generation**.
- Toggle **Expert Comparison** (visual overlays).
- (Optional) **Compute Baseline** to compare results against the entire 27-surgery ArthroPhase archive (takes 1-2 minutes).

### 4. Click 'Run Analysis'
The AI will execute its **8-step dynamic pipeline**:
- Frame Extraction → CV Tracking → Phase Identification → ASSET Metrics Calculation → Skill Classification → Clinical Feedback Generation → Visual Annotation → PDF Compilation.

---

## 📂 Project Outputs
After the analysis completes, check the `/outputs` folder for:
1.  **📊 Dashboard Update**: Real-time radar charts and stability timelines.
2.  **📄 PDF Report**: Professional A4 clinical assessment.
3.  **🎯 Trajectory PNG**: Frame overlay proving AI tracking accuracy.

---

*Winner of Ceaser's Medathon 2026 — CIT Dept. AI & Data Science Team*
