<a target="_blank" href="https://colab.research.google.com/github/SarahHannes/computational-drug-discovery/blob/main/computational_drug_discovery.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

### Goal:
- Predict molecular compound's pIC50 on target protein

### Target protein:
- Replicase polyprotein 1ab

### Organism:
- Severe acute respiratory syndrome coronavirus 2

### What I have done:
- Scraped for protein of interest & bioactivity data via Chembl API.
- Preprocessed to only include {active, inactive} compounds at pIC50 on target protein.
- Calculated Lipinski descriptors for druglike properties.
- Calculated molecular descriptors using PaDEL.
- Perform Mann-Whitney statistical analysis and found 2 out of 4 lipinski descriptors show same distribution between active and inactive compounds at IC50.
- Trained multiple baseline models
- Did a few feature extraction techniques:
  - Removing low variance features
  - Feature transformation
  - Dimensionality reduction
- Performed hyperparameter search for xgboost, lightgbm models
- Current best model is blending model with weights (bayesian ridge 0.4, lightgbm 0.7), with r2 score 0.62377145.

<img width="637" alt="image" src="https://github.com/user-attachments/assets/6951909a-6a27-4437-bb37-c4669abd354b">

### What could be improved:
- Try more feature engineering techniques (UMAP, Ivis, T-sne)
- Try more complex model architectures

### References & Credit:
Referenced <a href="https://youtu.be/plVLRashaA8?si=cRq4rxBGerQKeRuY">tutorial from Data Professor</a> with some updates:
  - Different target protein
  - Explored more models and did additional feature extractions techniques
