
# Lab 7: PCA & MLP Ransomware Classification

This project classifies ransomware using PCA (Principal Component Analysis) and MLP (Multi-Layer Perceptron) classifiers on a dataset of API call frequencies and string features from PE files.

## Dataset

- **Source:** Ransomware Dataset 2016
- **Records:** 1,524
- **Features:** 30,969 (API calls and string features)
- **Targets:** Binary classification (Goodware/Malware) and multi-class classification (11 ransomware families)
- **Link:** [rissgrouphub/ransomwaredataset2016](https://github.com/rissgrouphub/ransomwaredataset2016)

## Technologies

- Python
- Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## Steps

1. **Data Preprocessing:** Cleaned data, handled null values, removed constant columns.
2. **Feature Reduction:** Applied PCA to reduce 23,616 features to 100 principal components.
3. **Modeling:** Trained MLP classifiers on:
   - Binary classification (with/without PCA)
   - Multi-class classification (with/without PCA)
4. **Evaluation:** Compared models using accuracy, precision, recall, F1-score, and confusion matrices.

## Key Results

- **Binary Classification:** MLP with PCA achieved **98.03% accuracy** vs **96.72%** without PCA.
- **Multi-class Classification:** Models showed high overall accuracy (~96%) but struggled with rare ransomware families.
- **Insights:** PCA improved performance, reduced training time, and enabled effective data visualization.

## How to Run

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook "PCA & MLP-based Ransomware Classification (1).ipynb"
   ```
