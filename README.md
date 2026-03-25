# Gait Analysis: Normal vs Ataxic Gait Comparison

## 📌 Project Overview
This project performs **markerless gait analysis** using pose estimation to compare normal walking patterns with ataxic gait (uncoordinated walking). The analysis extracts joint angles, step length, walking speed, and symmetry metrics to quantify gait abnormalities.

## 🎯 Objectives
- Extract 3D pose landmarks from walking videos using MediaPipe
- Compute knee, hip, and shoulder angles during gait cycles
- Compare spatiotemporal parameters between normal and ataxic gait
- Generate clinical interpretation for fall risk assessment

## 🛠️ Technologies Used
- **Python** - Programming language
- **MediaPipe** - Pose estimation
- **OpenCV** - Video processing
- **Pandas** - Data manipulation
- **NumPy** - Numerical computations
- **Matplotlib** - Visualization
- **Google Colab** - Cloud notebook environment

## 📊 Dataset
The dataset contains 3D joint coordinates extracted from walking videos:
- **Normal Gait**: 30 seconds of natural walking
- **Ataxic Gait**: 30 seconds of simulated ataxic gait

### Dataset Columns:
- X, Y, Z coordinates for: Shoulders, Elbows, Wrists, Hips, Knees, Ankles
- Calculated angles: ThetaShoulder, ThetaHip, ThetaKnee
- Gait parameters: StepLength, StepWidth, FeetClearance, StrideSpeed

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com)
2. Upload the notebook `gait_analysis.ipynb`
3. Run all cells
4. Upload your CSV files when prompted

### Option 2: Local Machine
```bash
# Clone the repository
git clone https://github.com/yourusername/gait-analysis-normal-vs-ataxic.git

# Install dependencies
pip install -r requirements.txt

# Run the script
python gait_analysis.py
