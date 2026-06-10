# TFT Compact Modeling Paper Artifact

This folder contains the lightweight data and manuscript files supporting the paper:

```text
PINN-Assisted Compact Modeling and Residual Diagnosis for IGZO TFT SPICE Simulation
```

The artifact is intentionally small. It includes summary tables and paper figures, but does not include large intermediate pointwise prediction files or trained neural-network weights.

## Contents

```text
artifact/tft_pinn_modeling/
  data/
    measurements_summary.csv
    wl_holdout_summary.csv
    torch_pinn_wl_holdout_summary.csv
    residual_interpretability_by_curve.csv
    residual_interpretability_bias_overall.csv
  figures/
    representative_80_10_holdout_curves.png
    residual_holdout_curve_reduction.png
    residual_holdout_bias_heatmap.png
  paper/
    tft_pinn_compact_modeling.tex
    references.bib
```

## Data Files

- `measurements_summary.csv`: summary of the measured IGZO TFT dataset.
- `wl_holdout_summary.csv`: traditional global compact-model channel-length holdout results.
- `torch_pinn_wl_holdout_summary.csv`: length-only parameter PINN holdout results.
- `residual_interpretability_by_curve.csv`: residual PINN curve-level interpretation table.
- `residual_interpretability_bias_overall.csv`: residual PINN bias-region interpretation table.

## Figures

- `representative_80_10_holdout_curves.png`: representative output and transfer holdout curves comparing measurement, global compact fit, and parameter PINN.
- `residual_holdout_curve_reduction.png`: residual PINN curve-level error reduction.
- `residual_holdout_bias_heatmap.png`: residual PINN bias-region diagnostic heatmap.

## Full Project Reproduction

The full project contains scripts for:

- measured data preparation,
- compact-model fitting,
- ngspice consistency checks,
- traditional channel-length scaling,
- length-only PyTorch parameter PINN training,
- residual PINN training,
- residual interpretability analysis.

For full reproduction, use the project root and run the scripts documented in `context_README.md` and `Task.md`.

## Excluded from This Lightweight Artifact

The following files are not included here by default:

- large pointwise prediction CSV files,
- trained `.pt` model weights,
- temporary terminal logs,
- raw unprocessed measurement files.

These files can be regenerated or added separately if a reviewer requires exact end-to-end reproduction.

## Suggested Repository Statement

If this artifact is uploaded to GitHub, the paper can use a conservative availability statement:

```text
The processed data and analysis scripts used to generate the figures are available in the project repository.
```

If the repository is not public before submission, use:

```text
The processed data and analysis scripts are available from the authors upon reasonable request.
```
