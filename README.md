# Recurrent and Non-Recurrent Delay Decomposition — Westbound SR-60 at the SR-57/60 Confluence

Analysis code and supporting files for the paper *"An All-Day Structural Bottleneck:
Decomposing and Costing Recurrent and Non-Recurrent Delay on the Westbound SR-60
Approach to the SR-57/60 Confluence"* (Diamond Bar, California).

## What this repository contains
- `00_setup.ipynb` — the full analysis notebook: delay computation, recurrent/non-recurrent
  decomposition, baseline-percentile and free-flow sensitivity, SWITRS crash matching,
  USDOT-based monetization, and the eastbound robustness check.
- `station_crosswalk.csv` — the six westbound mainline detector stations (VDS, name,
  postmile, lanes).
- `pems_column_map.md` — the PeMS 5-minute file column reference used in the analysis.
- `results/` — computed result summaries (JSON) and Figure 1.

## Data sources (not re-hosted here)
The underlying data are publicly available from their original sources and are not
redistributed in this repository:
- **Traffic data:** Caltrans Performance Measurement System (PeMS), https://pems.dot.ca.gov
  (District 7, station 5-minute data, Sep 1 – Dec 9, 2022).
- **Crash data:** SWITRS via the Transportation Injury Mapping System (TIMS),
  https://tims.berkeley.edu.
- **Truck volumes:** Caltrans 2022 Truck AADT,
  https://dot.ca.gov/programs/traffic-operations/census.

## Reproducing the analysis
1. Download the PeMS District 7 station 5-minute files for Sep 1 – Dec 9, 2022 from PeMS.
2. Place them in a `data/raw/` folder.
3. Run `00_setup.ipynb`. The notebook regenerates all intermediate datasets and the
   result summaries in `results/`.

## Notes
- One station (VDS 776657, Grand Ave) returned no valid detector samples during the study
  window and is represented by PeMS imputation; it contributes ~3.6% of total delay. See
  the paper's data section for details.
- Analysis was performed in Python (pandas) using PeMS version 20.0.1 data.

## Citation
If you use this code, please cite the associated paper (citation to be added upon publication).
