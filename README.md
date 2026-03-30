# DermaLite AI: Edge-AI Skin Disease Screening prototype

## Team Details
* **Team Name**: Ctrl+Alt+Del [cite: 93]
* **Team Leader**: Lokesh Kiruala [cite: 94]
* **Project**: AMD Slingshot 2026 Submission [cite: 88, 96]

## Project Overview
DermaLite AI is a hybrid edge-AI skin disease detection system designed for real-time, image-based analysis. [cite_start]Unlike traditional cloud-dependent tools, our solution performs fast, privacy-preserving inference directly on-device. It is specifically built to support early detection in low-resource and rural settings where constant internet connectivity is unavailable.

## The Problem
Most existing dermatology AI tools rely heavily on cloud servers. This creates two major issues:
1. **Privacy Risks**: Sensitive medical images must be uploaded to external servers.
2. **Accessibility**: Rural regions with low bandwidth cannot access these tools effectively.

## The Solution
DermaLite AI solves these challenges by utilizing **AMD Ryzen AI** hardware for local inference. By running models locally, we ensure:
* **Offline Capability**: Works in remote areas without internet.
* **Privacy-First**: No mandatory image uploads to the cloud.
* **Speed**: Real-time results using hardware acceleration.

## Key Features
* **Real-time Classification**: Predicts disease categories from skin images.
* **Risk Assessment**: Categorizes results into Low, Moderate, or High risk levels.
* **Explainable AI (XAI)**: Generates Grad-CAM heatmaps to show the "attention" areas of the model.
* **AMD Optimization**: Uses ONNX Runtime optimized for AMD Ryzen AI NPUs.

## Technical Stack
| Component | Technology |
| :--- | :--- |
| **Model Architecture** | MobileNetV2 / EfficientNet-Lite  |
| **Framework** | PyTorch [cite: 188] |
| **Optimization** | ONNX Runtime (AMD Execution Provider)  |
| **Interface** | Streamlit  |
| **Explainability** | Grad-CAM  |
| **Local Storage** | SQLite  |

## System Architecture
1. **Frontend**: Streamlit-based local application.
2. **Preprocessing**: Image resizing and normalization.
3. **Inference Engine**: ONNX Runtime leveraging AMD Ryzen AI.
4. **Logic Layer**: Risk classification and XAI heatmap generation.

## How to Run
1. Ensure you have an AMD Ryzen AI-enabled device for optimal performance.
2. Install the necessary dependencies:
   ```bash
   pip install onnxruntime-directml streamlit torch
3. Run the application:
   ```bash
   streamlit run app.py
