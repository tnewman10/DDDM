# DDDM — Data-Driven Decision Making in Medicine

Jupyter notebooks and datasets for descriptive statistics and exploratory modeling across several clinical data sources.

## Projects

| Folder | Description | Main notebook |
|--------|-------------|---------------|
| [Respiratory Disesase Diagnosis](Respiratory%20Disesase%20Diagnosis/) | Synthetic symptom dataset | `Respiratory Disease Diagnosis.ipynb` |
| [Drug Interactions](Drug%20Interactions/) | DDInter drug–drug interaction pairs | `Drug Interactions.ipynb` |
| [DOSAGE](DOSAGE/) | Antibiotic dosing rule tables | `DOSAGE Descriptive Statistics.ipynb` |
| [AI Medical Device Summary Database](AI%20Medical%20Device%20Summary%20Database/) | FDA AI/ML medical device summaries | `AI Medical Device Summary.ipynb` |
| [Parkinson's Diagnosis](Parkinson's%20Diagnosis/) | OpenNeuro ds008768 EEG + clinical modeling | `ds008768/PD Model.ipynb` |

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
pip install pandas numpy scipy matplotlib seaborn jupyter
```

For the Parkinson EEG notebook, also install: `mne`, `pyarrow` (optional, for parquet).

## Data notes

- **Included in this repo:** CSV/table data, BIDS metadata (JSON/TSD/TSV), compiled modeling tables, and notebooks.
- **Excluded (too large for GitHub):** `.eeg` waveform files (~44 GB). Clone [OpenNeuro ds008768](https://openneuro.org/datasets/ds008768) into `Parkinson's Diagnosis/ds008768/` to reproduce voltage features locally.
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
