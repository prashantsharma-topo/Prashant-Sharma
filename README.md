# 🎵 Topological Data Analysis of Music Signals (Notebook Version)

This project applies **Topological Data Analysis (TDA)** to audio signals using a Jupyter Notebook workflow. It extracts meaningful structural features from music data and performs clustering to analyze similarities between different genres.

The pipeline converts audio signals into **MFCC-based point clouds**, computes **persistent homology**, and generates **Betti curves** and **Persistence Images**, which are further used for clustering and visualization.

---

## 📂 Project File

- `final.ipynb` → Complete pipeline including:
  - Audio processing
  - Topological feature extraction
  - Visualization
  - Clustering and analysis

---

## 📦 Libraries Used

The following libraries are used in this project:

- **librosa** → Audio loading and MFCC feature extraction  
- **numpy** → Numerical operations  
- **pandas** → Data handling and CSV generation  
- **matplotlib** → Plotting graphs  
- **seaborn** → Heatmaps and visual analysis  
- **ripser** → Persistent homology computation  
- **persim** → Persistence diagrams, Wasserstein distance, persistence images  
- **scikit-learn** → K-Means clustering, PCA, scaling  
- **scipy** → Scientific computations  

---

## 🚀 Workflow

The notebook follows this step-by-step pipeline:

### 1. Audio Input
- Accepts:
  - `.mp3`
  - `.wav`
  - `.zip` (multiple audio files)

---

### 2. Feature Extraction
- Extracts **MFCC (Mel-Frequency Cepstral Coefficients)** using `librosa`
- Normalizes features
- Represents each audio file as a **point cloud**

---

### 3. Persistent Homology
- Computes persistence diagrams using `ripser`
- Focus on:
  - \( H_0 \) (connected components)
  - \( H_1 \) (loops)

---

### 4. Topological Features
- **Betti Curves** → capture evolution of topological features  
- **Persistence Images** → convert diagrams into vectors  
- **Wasserstein Distance** → measure similarity between samples  

---

### 5. Clustering and Visualization
- Feature vectors are:
  - Standardized  
  - Clustered using **K-Means**  
- PCA is used to:
  - Reduce dimensions  
  - Visualize clusters  

---

## How to Run

### Step 1: Install Dependencies

```bash
pip install librosa ripser persim scipy matplotlib seaborn pandas numpy scikit-learn
