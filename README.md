# DDDM — Data-Driven Decision Making in Medicine

Jupyter notebooks and datasets for descriptive statistics and exploratory modeling across **five clinical data projects** in this repo.

## Projects (all included)

| Folder | Files in repo | Description | Main notebook |
|--------|---------------|-------------|---------------|
| [Respiratory Disesase Diagnosis](Respiratory%20Disesase%20Diagnosis/) | notebooks + CSV | Synthetic symptom dataset | `Respiratory Disease Diagnosis.ipynb` |
| [Drug Interactions](Drug%20Interactions/) | notebooks + CSV | DDInter drug–drug interaction pairs | `Drug Interactions.ipynb` |
| [DOSAGE](DOSAGE/) | notebooks + CSV | Antibiotic dosing rule tables | `DOSAGE Descriptive Statistics.ipynb` |
| [AI Medical Device Summary Database](AI%20Medical%20Device%20Summary%20Database/) | notebooks + FDA data + upstream repo | FDA AI/ML medical device summaries | `AI Medical Device Summary.ipynb` |
| [Parkinson's Diagnosis](Parkinson's%20Diagnosis/) | BIDS metadata + compiled tables + notebook | OpenNeuro ds008768 EEG + clinical modeling | `ds008768/PD Model.ipynb` |

Parkinson's looks like the largest share of files because ds008768 includes BIDS sidecars (JSON/TSD/TSV/VHDR) for every session — not because the other projects were omitted.

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
pip install pandas numpy scipy matplotlib seaborn jupyter
```

For the Parkinson EEG notebook, also install: `mne`, `pyarrow` (optional, for parquet).

## Data notes

- **Included:** All five project folders — notebooks, CSV/table data, BIDS metadata (JSON/TSV/VHDR), compiled modeling tables (CSV + Parquet), and the full `medical-ai-evaluation` upstream tree.
- **Excluded (GitHub size limits):** `.eeg` waveform binaries only (~46 GB). GitHub rejects individual files over 100 MB; the full EEG set cannot live in a normal repo. Download from [OpenNeuro ds008768](https://openneuro.org/datasets/ds008768) into `Parkinson's Diagnosis/ds008768/` to reproduce voltage features locally.
- **Excluded (internal):** `.git_backup/` folders from decoupled nested clones, Jupyter checkpoints, and local scratch scripts (`_*.py`).
- **DOSAGE** files are included under `DOSAGE/` (CC BY 4.0 — see `DOSAGE/README.md`).
- **Drug Interactions** CSVs are included under `Drug Interactions/`.
- **AI Medical Device** upstream data lives in `medical-ai-evaluation/database/`.

## Workflow pattern

Most notebooks follow the same descriptive pipeline:

1. Load raw data → `.head()` preview
2. One-hot or ordinal encoding where appropriate
3. Unified summary table (measurement level, central tendency, skew, IQR outliers)
4. Summary plots

## License

Each subproject may have its own data license. Check README files in subfolders before redistributing data.
