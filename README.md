# Spatio-Temporal Analysis and Visualisation of Persistent Road Traffic Collision Hotspots in Great Britain

MSc Data Science dissertation project using Department for Transport STATS19 police-reported personal-injury collision data from 2020–2024.

## Project scope

The project combines data cleaning, spatial projection, a fixed 5 km grid, annual hotspot classification, temporal persistence analysis, statistical modelling, next-year hotspot classification, explainable AI and Power BI visualisation.

## Important interpretation

The outputs identify **recorded collision concentration**, not exposure-adjusted road risk. Consistent traffic-volume or vehicle-kilometre exposure data were not available at the required grid-year level.

## Key project figures

- Original collision records: **503,475**
- Spatially valid records: **503,410**
- Spatial reference system: **EPSG:27700**
- Grid size: **5 km × 5 km**
- Historically active grid cells: **7,606**
- Grid-year observations: **38,030**
- Persistent grid cells: **554**
- Grid cells classified as hotspots in all five years: **481**

## Final predictive model

Balanced Logistic Regression was retained as a high-recall screening configuration.

2024 holdout result:

- True positives: **622**
- False negatives: **7**
- False positives: **264**
- True negatives: **6,713**
- Recall: **98.9%**
- Precision: **70.2%**
- Hotspot F1: **82.1%**
- ROC-AUC: **0.997**

The persistence baseline remained highly competitive. The balanced model reduced missed hotspots from 65 to 7 while increasing false positives. This is an operational trade-off rather than universal model superiority.

## Repository contents

This FULL package preserves **all files from the original project ZIP** and adds only repository-support files such as this README, `.gitignore`, `.gitattributes`, `requirements.txt`, and an upload guide.

The original notebooks, output CSV files, figures, GeoPackages, model artefacts and the source STATS19 CSV are all retained.

## GitHub and large files

Several project files exceed GitHub's normal Git file limits. This repository is therefore configured for **Git LFS**. Install Git LFS before pushing the full project.

See `GITHUB_UPLOAD_CHECKLIST.md` for the exact commands.

## Main notebooks

The project includes the original staged notebooks, including:

- `data_cleaning.ipynb`
- `05_Grid_Year_Summary.ipynb`
- `06_Hotspot_and_Persistence_Scoring_Student_Working.ipynb`
- `07_Statistical_Modelling_Student_Working.ipynb`
- `08_Predictive_Modelling_Completed_Student.ipynb`
- `09_Explainable_AI_Interpretation_Student_Working.ipynb`

Other project notebooks contained in the original ZIP are also preserved.

## Reproducibility

Install the Python dependencies with:

```bash
pip install -r requirements.txt
```

The notebooks were developed in Google Colab/Jupyter-compatible Python environments.
