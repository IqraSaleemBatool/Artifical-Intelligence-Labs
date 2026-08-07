
# Autoencoder-Based Anomaly Detection

##  Overview
This Jupyter notebook implements an **autoencoder-based anomaly detection** system using deep learning. The model is trained on normal data patterns and identifies anomalies based on reconstruction error.

##  Objective
Detect anomalous patterns in network traffic/embedded system data using an **autoencoder neural network** trained exclusively on normal samples.

##  Dataset
- **Embedded System Network Security Dataset**
- Features: Network traffic metrics
- Labels: Normal (0) vs Anomalous (1)
- Training: Only normal samples (outcome = 0)

##  Model Architecture

### Autoencoder
```
Encoder: Input → 256 → 128 → 64 → 32 → Bottleneck
Decoder: Bottleneck → 64 → 128 → 256 → Output
```
- **Layers**: Dense layers with BatchNorm & Dropout
- **Activation**: ReLU
- **Loss Function**: Mean Squared Error (MSE)
- **Optimizer**: Adam

### Key Techniques
- **Training**: Only on normal data to learn "normal" patterns
- **Anomaly Detection**: Samples with high reconstruction error are flagged as anomalies
- **Regularization**: Dropout & BatchNorm to prevent overfitting
- **Early Stopping**: Prevents overtraining
- **Optional**: PCA dimensionality reduction

##  Results

| Metric | Value |
|--------|-------|
| Accuracy | Up to 90% |
| Threshold Optimization | F1-score based |
| ROC AUC | Shows separation capability |

##  Dependencies
```
pandas, numpy, scikit-learn
torch, matplotlib, seaborn
requests
```

##  Usage
```bash
jupyter notebook autoencoder_based_anomaly_detection.ipynb
```

### Workflow
1. Load and preprocess dataset
2. Train autoencoder on normal data only
3. Set anomaly threshold using validation data
4. Detect anomalies on test data
5. Evaluate and visualize results

##  Files
- `autoencoder_based_anomaly_detection.ipynb` - Main notebook

##  Key Features
- **Unsupervised Learning**: No labels needed for training
- **Threshold Tuning**: Optimized using validation set
- **Visualization**: Reconstruction error distribution & ROC curves
- **Scalable**: Works with various feature dimensions
