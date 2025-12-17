<div align="center">

# Leaf Doctor
### Precision Plant Diagnosis. Powered by Gemini.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg?style=flat-square)
![Flutter](https://img.shields.io/badge/Flutter-3.8.1+-02569B.svg?style=flat-square&logo=flutter)
![Dart](https://img.shields.io/badge/Dart-3.0+-0175C2.svg?style=flat-square&logo=dart)
![License](https://img.shields.io/badge/license-MIT-green.svg?style=flat-square)

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#interface-gallery">Interface</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#installation">Installation</a>
</p>

</div>

---

**Leaf Doctor** redefines agricultural care by combining advanced artificial intelligence with a seamless, human-centric user experience. Instantly analyze plant health, receive professional-grade treatment recommendations, and access a curated marketplace of essential products—all from your pocket.

## Overview

Leaf Doctor is engineered to bridge the gap between complex agricultural science and everyday utility.

### ✨ Intelligent Analysis
Harnessing the neural capabilities of **Google Gemini AI**, Leaf Doctor detects plant pathologies with exceptional accuracy. Simply capture a photo to receive immediate, confidence-graded insights that empower informed decision-making.

### 🌿 Curated Ecosystem
Beyond mere diagnosis, the application provides a holistic care plan. From step-by-step treatment guides to deep integration with the **SPU AI CLUB Recommended** marketplace, every interaction is designed to restore plant health effortlessly.

### 📄 Professional Reporting
Generate high-fidelity diagnostic reports in Thai or English with a single tap. The dedicated **PDF Engine** renders documents perfect for archival, research, or professional consultation.

---

## Interface Gallery

Experience the clean, intuitive design language of Leaf Doctor, optimized for clarity and efficiency.

| **Dashboard** | **Analysis** | **Marketplace** | **Archive** |
|:---:|:---:|:---:|:---:|
| <div style="width:200px; height:400px; background:#f0f0f0; display:flex; justify-content:center; align-items:center;">Command Center</div> | <div style="width:200px; height:400px; background:#f0f0f0; display:flex; justify-content:center; align-items:center;">Precision Insights</div> | <div style="width:200px; height:400px; background:#f0f0f0; display:flex; justify-content:center; align-items:center;">Curated Selections</div> | <div style="width:200px; height:400px; background:#f0f0f0; display:flex; justify-content:center; align-items:center;">Digital Records</div> |
| *Fluid Navigation* | *Visual Diagnostics* | *Seamless Commerce* | *History Management* |

> **Note**: For the full visual experience, please refer to the `assets/images` directory.

---

## Architecture & Engineering

Leaf Doctor is built on a modular architecture designed for scalability and maintainability. The codebase enforces strict separation of concerns to facilitate rapid iteration.

### Core Components

* **`main.dart` (The Nucleus)**
    <br>Handles application lifecycle, routing, state management, and the primary UI orchestration.

* **`ui_components.dart` (Atomic Design System)**
    <br>A library of reusable, stateless widgets ensuring visual consistency across the app (e.g., `showProductDetails`, `isValidUrl`).

* **`pdf_service.dart` (Document Engine)**
    <br>A dedicated service layer responsible for generating pixel-perfect PDF documents utilizing the native print subsystem.

### Extensibility Guide

#### 1. Marketplace Expansion
To integrate new certified products or modify the "Official" recommendations:
* Navigate to: `GeminiService._getPrompt`
* **Action:** Refine the system instructions to request specific JSON structures, or implement a local data repository in `_ProductPageState` for static catalog management.

#### 2. Intelligence Tuning
To calibrate the diagnostic persona or adjust language nuances:
* Locate: `GeminiService` class in `main.dart`
* **Action:** Modify the `_getPrompt(bool isDeepMode)` method.
* *Warning: Maintain the strict JSON output schema to ensure parser integrity.*

#### 3. Report Styling
To customize the visual identity of exported documents:
* Open: `lib/pdf_service.dart`
* **Action:** Update `generateDiagnosisPdf` using the generic layout engine to adjust typography, branding assets, and grid systems.

---

## Quick Start

### Prerequisites
* **Flutter SDK**: 3.8.1 or later
* **Dart SDK**: Compatible version
* **IDE**: Xcode (macOS) or Android Studio

### Installation

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/leaf-doctor.git](https://github.com/your-username/leaf-doctor.git)
    cd leaf-doctor
    ```

2.  **Resolve Dependencies**
    ```bash
    flutter pub get
    ```

3.  **Configuration**
    Inject your Google Gemini API credentials in `lib/main.dart`:
    ```dart
    // Security Note: Use environment variables for production builds
    final String _apiKey = 'YOUR_API_KEY_HERE';
    ```

4.  **Build & Run**
    ```bash
    flutter run
    ```

---

<div align="center">

### Designed and Engineered by SPU AI CLUB
*Innovation for a Greener Future.*

[Website](https://www.spuaiclub.com) • [GitHub](https://github.com/spuaiclub)

</div>
