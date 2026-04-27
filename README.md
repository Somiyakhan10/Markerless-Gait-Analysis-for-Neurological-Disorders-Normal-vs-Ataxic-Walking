# GaitAnalysis — Normal vs Ataxic Gait Classification

## 3D Pose Estimation-Based Gait Analysis System for Neurological Assessment

**Python 3.8+** | **pandas** | **numpy** | **matplotlib** | **scipy**

---

⚠️ **Medical Disclaimer:** This tool is designed for research and educational purposes only. It is not intended for clinical diagnosis or regulatory decision-making. Always consult a qualified healthcare professional.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Dataset](#dataset)
- [Gait Metrics Analyzed](#gait-metrics-analyzed)
- [Results](#results)
- [Output Images](#output-images)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Author](#author)
- [License](#license)

---

## 🔬 Overview

**GaitAnalysis** is a Python-based system that compares **normal gait** versus **ataxic gait** patterns using 3D pose estimation data. The system processes biomechanical gait parameters including knee angles, hip angles, step length, walking speed, and symmetry indices to provide quantitative clinical assessment.

Ataxic gait is characterized by uncoordinated, unsteady movements typically associated with cerebellar dysfunction. This system enables objective, data-driven comparison between normal and pathological gait patterns for research purposes.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| **Dual File Comparison** | Compare normal vs ataxic gait CSV files |
| **3D Joint Angle Calculation** | Compute knee/hip angles from 3D coordinates |
| **10 Clinical Metrics** | Symmetry, GDS, FRI, Economy, Correlation, and more |
| **12 Visualizations** | Bar charts, time series, scatter plots, radar chart |
| **Clinical Scores** | Gait Dysfunction Score (GDS) and Fall Risk Index (FRI) |
| **Google Colab Compatible** | Run directly in browser |

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| Name | 3D Pose Estimation Gait Data |
| Normal Frames | 28,540 frames |
| Ataxic Frames | 34,651 frames |
| Frame Rate | 30 fps |
| Joints Tracked | 16 joints (Shoulder, Elbow, Wrist, Hip, Knee, Ankle) |

---

## 📈 Results

### Key Findings (Dataset-Specific)

| Metric | Normal | Ataxic | Difference |
|--------|--------|--------|------------|
| Walking Speed | 1.32 m/s | 1.17 m/s | 11.5% slower |
| Step Length | 0.590 m | 0.646 m | 9.4% longer |
| Knee Angle | 69.33° | 91.89° | 32.5% more flexed |
| Knee Symmetry | 0.15% | 1.94% | 13x worse |
| Speed-Step Correlation | +0.18 | -0.18 | Classic ataxia signature |

### Clinical Scores

| Score | Value | Classification |
|-------|-------|----------------|
| Gait Dysfunction Score (GDS) | 0.0807 | Mild Dysfunction |
| Fall Risk Index (FRI) | 5.9 | Mild Risk |
| Clinical Confidence | 87.5% | HIGH |

---

## 🖼️ Output Images

### Graph 1: Joint Angle Comparison

<img width="1088" height="648" alt="joint angles" src="https://github.com/user-attachments/assets/f1dc224e-3ab8-413c-ad22-2b35f738911c" />


*Bar chart showing Left/Right Knee and Hip angles for Normal vs Ataxic.*

---

### Graph 2: Knee Angle Time Series

<img width="1088" height="648" alt="joint angles" src="https://github.com/user-attachments/assets/b559e0ad-f0a1-430e-ab92-e37ac6cffc0a" />


*Knee angle variation over first 500 frames with mean value lines.*

---

### Graph 3: Step Length Comparison

<img width="758" height="649" alt="image" src="https://github.com/user-attachments/assets/f91a091a-cae3-4255-b853-cdbe7818add5" />


*Comparison of average step length between Normal and Ataxic.*

---

### Graph 4: Walking Speed Comparison
<img width="758" height="649" alt="image" src="https://github.com/user-attachments/assets/76278f69-4b21-46a6-a59b-ef6653cbcd88" />


*Comparison of average walking speed between Normal and Ataxic.*

---

### Graph 5: Gait Symmetry Index

<img width="978" height="649" alt="image" src="https://github.com/user-attachments/assets/72ca7be1-0731-44b2-a5b9-b3b2611171f8" />


*Knee and hip symmetry index (0% = perfect symmetry, higher = more asymmetric).*


---

### Graph 8: Speed-Step Correlation

![Correlation](graphs/graph08_correlation.png)

*Scatter plot showing correlation between walking speed and step length.*

---

### Graph 10: Clinical Scores Summary

<img width="978" height="648" alt="image" src="https://github.com/user-attachments/assets/09fa5890-882c-41a7-b5b0-0b8cb0ac452d" />


*Summary of GDS, FRI, and Confidence scores.*

---

### Graph 11: Normalized Metrics

![Normalized](graphs/graph11_normalised_metrics.png)

*Ataxic metrics as percentage of Normal (100% = Normal baseline).*

---

### Graph 12: Clinical Diagnosis Dashboard

![Dashboard](graphs/graph12_diagnosis_dashboard.png)

*Complete clinical report with key findings and recommendations.*

---

## 🧠 How It Works

### Processing Pipeline

| Step | Description |
|------|-------------|
| 1 | Upload Normal and Ataxic CSV files |
| 2 | Extract 3D joint coordinates (16 joints) |
| 3 | Calculate joint angles using vector mathematics |
| 4 | Convert to real-world units (m/s, meters, degrees) |
| 5 | Extract gait parameters (speed, step, angle) |
| 6 | Compute 10 clinical metrics |
| 7 | Generate 12 visualizations |
| 8 | Output clinical diagnosis with confidence score |

---

## 💻 Technology Stack

| Component | Technology |
|-----------|------------|
| Language | Python 3.8+ |
| Data Processing | pandas, numpy |
| Visualization | matplotlib |
| Statistics | scipy |
| Environment | Google Colab / Jupyter Notebook |

---

## 🔧 Installation

### Google Colab (Recommended)

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload `Gait_Analysis_Normal_vs_Ataxic.ipynb`
3. Run all cells
4. Upload your CSV files when prompted

### Local Installation

```bash
git clone https://github.com/yourusername/GaitAnalysis.git
cd GaitAnalysis
pip install pandas numpy matplotlib scipy
jupyter notebook Gait_Analysis_Normal_vs_Ataxic.ipynb
