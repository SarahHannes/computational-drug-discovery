# computational-drug-discovery
### Goal:
Predict molecular compound's pIC50 on target protein

### Target protein:
Replicase polyprotein 1ab

### Organism:
Severe acute respiratory syndrome coronavirus 2

### What we have achieved:
- Scrape for protein of interest & bioactivity data via Chembl API.
- Preprocess to only include {active, inactive} compounds at pIC50 on target protein.
- Calculated Lipinski descriptors for druglike properties.
- Calculated molecular descriptors using PaDEL.
- Perform Mann-Whitney statistical analysis and found 2 out of 4 lipinski descriptors show same distribution between active and inactive compounds at IC50.
- Trained 3 models (Bayesian Ridge, XGBoost, LightGBM), however all of the trained models have subpar performance ~50%.

### What could be improved: 
- Perform more feature extraction, perhaps using PCA.
