# DermaLite AI: Edge-AI Skin Disease Screening prototype

## Team Details
* [cite_start]**Team Name**: Ctrl+Alt+Del [cite: 93]
* [cite_start]**Team Leader**: Lokesh Kiruala [cite: 94]
* [cite_start]**Project**: AMD Slingshot 2026 Submission [cite: 88, 96]

## Project Overview
[cite_start]DermaLite AI is a hybrid edge-AI skin disease detection system designed for real-time, image-based analysis[cite: 95, 99]. [cite_start]Unlike traditional cloud-dependent tools, our solution performs fast, privacy-preserving inference directly on-device[cite: 100, 109]. [cite_start]It is specifically built to support early detection in low-resource and rural settings where constant internet connectivity is unavailable[cite: 95, 111].

## The Problem
[cite_start]Most existing dermatology AI tools rely heavily on cloud servers[cite: 108]. This creates two major issues:
1. [cite_start]**Privacy Risks**: Sensitive medical images must be uploaded to external servers[cite: 109].
2. [cite_start]**Accessibility**: Rural regions with low bandwidth cannot access these tools effectively[cite: 111].

## The Solution
[cite_start]DermaLite AI solves these challenges by utilizing **AMD Ryzen AI** hardware for local inference. By running models locally, we ensure:
* [cite_start]**Offline Capability**: Works in remote areas without internet[cite: 103, 111].
* [cite_start]**Privacy-First**: No mandatory image uploads to the cloud[cite: 109, 132].
* [cite_start]**Speed**: Real-time results using hardware acceleration[cite: 95, 121].

## Key Features
* [cite_start]**Real-time Classification**: Predicts disease categories from skin images[cite: 99, 125].
* [cite_start]**Risk Assessment**: Categorizes results into Low, Moderate, or High risk levels[cite: 126].
* [cite_start]**Explainable AI (XAI)**: Generates Grad-CAM heatmaps to show the "attention" areas of the model[cite: 110, 128].
* [cite_start]**AMD Optimization**: Uses ONNX Runtime optimized for AMD Ryzen AI NPUs[cite: 194, 195].

## Technical Stack
| Component | Technology |
| :--- | :--- |
| **Model Architecture** | [cite_start]MobileNetV2 / EfficientNet-Lite [cite: 155, 188] |
| **Framework** | [cite_start]PyTorch [cite: 188] |
| **Optimization** | [cite_start]ONNX Runtime (AMD Execution Provider) [cite: 176, 188] |
| **Interface** | [cite_start]Streamlit [cite: 178, 188] |
| **Explainability** | [cite_start]Grad-CAM [cite: 121, 188] |
| **Local Storage** | [cite_start]SQLite [cite: 183, 188] |

## System Architecture
1. [cite_start]**Frontend**: Streamlit-based local application[cite: 178, 188].
2. [cite_start]**Preprocessing**: Image resizing and normalization[cite: 139, 174].
3. [cite_start]**Inference Engine**: ONNX Runtime leveraging AMD Ryzen AI[cite: 176, 195].
4. [cite_start]**Logic Layer**: Risk classification and XAI heatmap generation[cite: 181, 182].

## How to Run
1. [cite_start]Ensure you have an AMD Ryzen AI-enabled device for optimal performance[cite: 195].
2. Install the necessary dependencies:
   ```bash
   pip install onnxruntime-directml streamlit torch
