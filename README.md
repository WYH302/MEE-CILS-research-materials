# MEE: EEM probability fusion research materials

Research materials for **Adaptive probability fusion of overlapping EEM representations under protocol-defined perturbations**.

This repository distributes the study's code, predefined validation splits, prediction outputs and statistical results. It is not a mirror of the third-party raw spectral datasets and does not imply journal acceptance.

## Download the research materials

[MEE_CILS_Research_Materials.zip](https://github.com/WYH302/MEE-CILS-research-materials/releases/download/v1.0.0/MEE_CILS_Research_Materials.zip) (about 27 MB compressed).

SHA-256: `b4777be34562769fcab824bb757be7746f58c439c460f46f207503f9a3d5b6a5`.

The ZIP contains 584 files (about 227 MB uncompressed) under `CILS_research_materials/`:

- `src/`, `scripts/`, `tests/`: processing, modelling and analysis code and tests.
- `config/`: study configurations.
- `runs/`: predefined group-disjoint splits, observation-level three-class predictions, fold metrics and execution records.
- `analysis/`: target-level and source-level summaries, paired comparisons and perturbation analyses.
- `figures/`: analysis figure inputs and outputs.
- `data/`: original-source download inventory and JODA concentration-table provenance.
- `requirements-reproduction.txt`: recorded Python package requirements.

The primary suite covers 831 public EEM records, 16 target tasks, five outer folds and three inner folds. MEE-C and MEE-S use different temperature-selection objectives for the same probability-allocation mechanism.

## Reproduce from the archived release

Start with the [versioned release](https://github.com/WYH302/MEE-CILS-research-materials/releases/tag/v1.0.0), rather than expecting the Git checkout to contain `src/`. Verify the SHA-256 above before extracting. Read `CILS_research_materials/README.md` and `requirements-reproduction.txt` inside the archive; retain the archived configurations and predefined splits.

The archived source layout is appropriate for a future readable Git release, but extracting every file into the default branch would also publish generated material and historical paths. Curate the source and preserve the release checksum rather than silently replacing the archive.

## Real-world Robustness & Edge Deployment

The release contains protocol-defined perturbation analyses and observation-level predictions. Interpret those results under the archived perturbation definitions and group-disjoint splits; they are not newly captured field measurements.

For spectral inputs, test relevant intensity changes, measurement noise and missing wavelength regions under a frozen protocol. A photograph-style occlusion test is not automatically meaningful for EEM data. No edge-device latency, peak-memory, power or exported-model parity report is provided in this repository.

## Original spectral data

Obtain the original datasets from their providers under the applicable terms:

| Source | Provider page |
|---|---|
| Designed | https://ucphchemometrics.com/designed-fluorescence-data/ |
| Dorrit | https://ucphchemometrics.com/dorrit-eem/ |
| Organic micropollutants | https://ucphchemometrics.com/micropol/ |
| JODA | https://ucphchemometrics.com/joda/ |

The [download manifest](OFFICIAL_DOWNLOAD_MANIFEST.csv) records the original archive filenames, URLs and checksums used for the study. The [JODA provenance note](JODA_CONCENTRATION_PROVENANCE.md) describes the separately transcribed experimental concentrations.

Please cite the original data sources, including Acar et al. (2014), *Structure-revealing data fusion*, https://doi.org/10.1186/1471-2105-15-239, and Bro, Rinnan and Faber (2005), *Standard error of prediction for multilinear PLS. 2. Practical implementation in fluorescence spectroscopy*, https://doi.org/10.1016/j.chemolab.2004.04.014, where applicable.

## Getting started

1. Download and extract the research ZIP.
2. Inspect the configurations and recorded environment before running code.
3. For analysis of reported outcomes, start with the CSV files in `analysis/` and predictions in `runs/`.
4. For reconstruction from raw spectra, obtain the source archives using the manifest and use the included source-processing scripts. Retain the predefined group assignments when comparing with the paper's reported results.

The archived configuration and provenance files retain the execution identifiers used to connect outputs to their generating code. Do not treat historical local filesystem paths as portable installation instructions.

## Rights and scope

Third-party datasets remain subject to their original providers' terms. No additional blanket license is asserted over those datasets. The repository does not assign an open-source license on behalf of contributors; consult the authors about reuse permissions where no explicit license applies.

The public release preparation checks archive integrity and common credential patterns. It does not constitute a new execution of all experiments.
