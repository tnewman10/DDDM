# Resting-State EEG in Parkinson's Disease and Healthy Controls

## Overview

This dataset contains human resting-state electroencephalography (EEG) recordings collected from individuals with Parkinson's disease (PD) and healthy controls (HC). Recordings were acquired during eyes-open resting-state conditions.

The dataset includes 358 resting-state EEG recordings from 312 unique participants. Some participants have recordings from multiple sessions, allowing for longitudinal analyses.

## Participants

The dataset includes participants with Parkinson's disease and healthy control participants. Participant-level demographic information is provided in `participants.tsv`.

Participant-level variables include:

- Age at the first resting-state EEG session
- Sex
- Education
- Race
- Group (PD or Control)

Session-specific clinical and acquisition information is provided in each participant's `_sessions.tsv` file.

Session-level variables include:

- Age at the time of recording
- Montreal Cognitive Assessment (MoCA) score
- UPDRS Part III score
- Parkinson's disease duration
- Levodopa equivalent daily dose (LEDD)
- Resting-state condition
- De-identified acquisition date
- Days since the participant's first session

## EEG Data

EEG recordings are provided in BrainVision format (`.vhdr`, `.vmrk`, and `.eeg`) and organized according to the Brain Imaging Data Structure (BIDS) specification.

The majority of recordings were acquired at 500 Hz. A subset of recordings was acquired at 25,000 Hz. Original sampling frequencies have been retained.

EEG recordings use Pz as the reference electrode. Recordings contain between 63 and 64 EEG channels, with some recordings additionally containing auxiliary channels such as audio or respiratory measurements. These channels have been retained where available.

Recordings were collected using eyes-open resting-state conditions.

## Dataset Organization

The dataset follows BIDS version 1.11.1.

At the dataset level:

- `participants.tsv` contains one row per participant.
- `participants.json` describes the participant-level variables.
- Participant-specific `_sessions.tsv` files contain session-level demographic, clinical, and acquisition information.
- Participant-specific `_sessions.json` files describe the session-level variables.
- EEG recordings and associated metadata are contained within participant/session directories.

## De-identification

Acquisition dates have been de-identified for public release. Dates were altered while preserving the exact intervals between sessions within each participant. Therefore, the absolute acquisition dates should not be interpreted as the original dates of data collection.

## Contributing Studies

The recordings were collected as part of multiple research projects. The dataset combines these recordings into a common BIDS-formatted dataset for public reuse. The contributing project identifiers used during data curation are not treated as separate source datasets in this release.

## Missing Data

Missing demographic or clinical values are represented as `n/a` in accordance with BIDS conventions.

## License

This dataset is released under the Creative Commons CC0 1.0 Universal dedication.

## Contact

For questions regarding the dataset, please contact:

Nandakumar Narayanan  
nandakumar-narayanan@uiowa.edu
University of Iowa