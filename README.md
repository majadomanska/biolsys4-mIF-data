# Project 4: Spatial Niches in mIF Data

## Project overview

This project investigates the spatial organisation of the lung tumour microenvironment using multiplex immunofluorescence (mIF) data. The analysis focuses on three tasks:

- D1: Immune-cell infiltration profiles
- D2: Moran’s I spatial clustering
- D3: Patient stratification from spatial features

---

## Input data

The analysis requires the tabular mIF dataset provided during the course.

Expected location:

```text
unzipped/tsv/cells_properties/
```

---

## Environment setup

Create a virtual environment:

```bash
python -m venv sysbio4
source sysbio4/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

(Optional) Register a Jupyter kernel:

```bash
pip install ipykernel

python -m ipykernel install \
    --user \
    --name sysbio4 \
    --display-name "Python (sysbio4)"
```

---

## Running the analysis

Open Jupyter Notebook and

Run all notebook cells from top to bottom.

The notebook performs:

### D1: Immune-cell infiltration profiles

- tumour–stroma border distance calculation
- T-cell infiltration profiles
- patient ranking by infiltration score
- classification into infiltrated, mixed and immune-excluded groups

### D2: Moran’s I spatial clustering

- k-NN graph construction
- Moran’s I implementation
- permutation-based null model
- clustering analysis for all cell types
- comparison of T-cell clustering across patients

### D3: Patient stratification

- spatial niche identification using neighbourhood composition
- niche fraction calculation
- niche self-adjacency calculation
- feature matrix construction
- PCA
- patient clustering
- biological interpretation of patient groups

---

## Main outputs

The analysis is performed entirely within the Jupyter notebook. Results are displayed directly in the notebook and are not automatically exported to separate files.

The notebook generates:

- border-distance distribution plots
- T-cell infiltration profiles
- Moran’s I clustering figures
- niche composition heatmaps
- PCA visualisations
- patient clustering plots
- summary tables used for biological interpretation

All figures, tables and interpretations are produced interactively during notebook execution.

---

## Reproducibility

## Reproducibility

All analyses are performed directly from the input tabular data files. Running the notebook from the first cell to the last cell reproduces all reported results, figures and tables directly within the notebook.
