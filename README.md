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





# Run the script
python gait_analysis.py
