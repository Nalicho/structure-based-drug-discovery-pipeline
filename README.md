# Structure-Based Drug Discovery Pipeline

## Overview

A reproducible computational workflow for **structure-based drug discovery** integrating:

- Ligand preparation  
- Automated docking (AutoDock Vina)  
- Affinity ranking  
- Sequential ADMET filtering  

The pipeline supports early-stage **small-molecule prioritisation** and is adaptable to both CNS and non-CNS therapeutic contexts.

---

## Usage

### 1. Prepare Ligand Library

Place your multi-molecule SDF file in the repository root directory:

`ligand_library.sdf`

### 2. Run Docking Workflow

Open and execute:

`docking/structure_based_virtual_screening_vina_clean.ipynb`

This performs ligand preparation, batch docking, affinity extraction, and ranking.
Ensure the receptor structure (receptor.pdbqt) and config.txt are placed inside the docking/ directory before execution.

### 3. Run ADMET Filtering

Open and execute:

`admet/admet_drug_likeness_screening_clean.ipynb`

This applies sequential medicinal chemistry filtering and exports:

`final_prioritised_ligands.csv`

---

## Requirements

- Python 3.x  
- AutoDock Vina  
- Open Babel  
- Python packages listed in `requirements.txt`  

Ensure `vina` and `obabel` are accessible in your system PATH.
