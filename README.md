# Deep Neural Network Based Direct Measurement from Laser Feedback Signals

**Final Year Design Project (2025)**  
**Authors**: Zoha Ahmed (381477), Huma Tahir (378286)  
**Advisor**: Dr. Usman Zabit  
**Co-Advisor**: Dr. Wajahat Hussain  
**Institution**: School of Electrical Engineering and Computer Science, NUST

## Abstract

This project explores direct displacement estimation from laser feedback interferometry signals using deep neural networks. We propose and evaluate two innovative architectures:
- **Temporal Fusion Transformer (TFT)** - First application to SMI signal processing
- **CNN+LSTM Hybrid** - Novel feature engineering approach

Both models achieve sub-micrometer accuracy in displacement reconstruction under variable optical feedback and noise conditions.

## Key Innovations

- **First TFT application** to self-mixing interferometry (no prior work in photonics)
- **Novel feature engineering** combining domain knowledge with deep learning
- **Robust performance** under variable optical feedback and speckle noise
- **Real-time capability** with lightweight inference (5.3ms per sample)

## Results Summary

| Model | Dataset | MAE (μm) | MSE (μm²) | % Error |
|-------|---------|----------|-----------|---------|
| TFT | Training | 0.0598 | 0.0620 | 2.39% |
| TFT | Experimental | 0.0864 | 0.0121 | 3.46% |
| CNN+LSTM | Test | 0.0141 | 0.0173² | - |

## Architecture Overview

### Temporal Fusion Transformer
- Gated Residual Networks for variable selection
- Multi-head attention for long-term dependencies  
- Novel features: CrossedMean & PowerDerivative

### CNN+LSTM Hybrid
- 1D CNN for local feature extraction
- Bidirectional LSTM for temporal modeling
- Three-channel input: P_signal, & features extracted through feature engineering
