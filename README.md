# digitaria-insularis-ecological-data
Ecological niche modeling of Digitaria insularis using PCA-based environmental predictors implemented in the ENMTML framework.
Modeling the climatic suitability of Digitaria insularis under climate change

This repository contains the data processing scripts, ecological niche modeling workflows, and spatial analyses used in the study:

**Modeling the climatic suitability of Digitaria insularis, a global invasive species, under climate change scenarios**

The study evaluates the current and future climatic suitability of Digitaria insularis (sourgrass), a globally invasive and herbicide-resistant C₄ grass, under different climate change scenarios using ecological niche modeling (ENM).

### Occurrence data
- Curated global occurrence records of *Digitaria insularis*
- Data sources: GBIF, SpeciesLink, NYBG
- Records filtered using CoordinateCleaner and temporal constraints
- Final occurrence dataset used for modeling

- ### Environmental data
- WorldClim v2.1 bioclimatic variables (current climate)
- Future climate projections (EC-Earth3-Veg, MPI-ESM1-2-HR)
- Scenarios: SSP126 and SSP585
- Time horizons: 2030 (2021–2040) and 2090 (2081–2100)

- ### Variable selection
- Principal Component Analysis (PCA) used to reduce collinearity
- PCA layers (PC1–PCn) used as predictors in ENMTML models
- PCA outputs provided to document environmental space representation

### Ecological niche modeling
- Modeling performed using the ENMTML R package
- Algorithms: Bioclim, Maxent, Random Forest, SVM
- Model evaluation metrics: AUC, TSS, Kappa, Jaccard, Sorensen, OR
- Ensemble projections generated using the MEAN method

### Extrapolation and novelty analyses
- MOP extrapolation maps
- Maps provided to document areas of environmental novelty
- Used to assess model transferability under future scenarios

- ### Spatial outputs
- Continuous suitability maps
- Binary maps (MAX_TSS threshold)
- Scenario comparison maps:
  - Gain (future only)
  - Loss (current only)
  - Stable (current and future)
