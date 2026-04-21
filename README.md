#  Topological Data Analysis on Music + Clustering

This project applies **Topological Data Analysis (TDA)** to audio signals to extract structural features and performs **unsupervised clustering** to analyze similarities between different music samples.

The pipeline converts audio into **MFCC-based point clouds**, computes **persistent homology**, and generates features such as **Betti curves** and **Persistence Images**, which are then used for clustering and visualization.

---

##  Project Files

- `tda_on_music.py` → Main pipeline for feature extraction and topological analysis  
- `clustering.py` → Performs clustering and PCA visualization on generated features  

---

##  Libraries and Their Roles

This project relies on the following Python libraries:

- **librosa** → Audio processing (loading audio, extracting MFCC features)  
- **numpy** → Numerical computations and array handling  
- **pandas** → Storing and exporting feature data (CSV files)  
- **matplotlib** → Plotting graphs (Betti curves, persistence diagrams)  
- **seaborn** → Heatmaps for Wasserstein distance matrix  
- **ripser** → Fast computation of persistent homology  
- **persim** → Visualization and vectorization (persistence diagrams, images, Wasserstein distance)  
- **scikit-learn** → Clustering (K-Means), scaling, PCA  
- **scipy** → Scientific computations (used indirectly by TDA tools)  

---

##  Workflow

### Step 1: Feature Extraction + TDA (`tda_on_music.py`)

1. Load audio file(s) (MP3/WAV/ZIP)
2. Extract **MFCC features** using `librosa`
3. Represent MFCCs as a **point cloud**
4. Compute **persistent homology** using `ripser`
5. Extract:
   - Persistence Diagrams (PD)
   - Betti Curves
   - Persistence Images (PI)
6. Compute **Wasserstein distances** between samples
7. Save outputs as CSV and plots

---

### Step 2: Clustering (`clustering.py`)

1. Load feature CSV (Betti or PI)
2. Handle missing values (mean imputation)
3. Standardize features (`StandardScaler`)
4. Apply **K-Means clustering**
5. Reduce dimensions using **PCA**
6. Visualize clusters and save results

---

##  How to Run

### Install Dependencies

```bash
pip install librosa ripser persim scipy matplotlib seaborn pandas numpy scikit-learn
