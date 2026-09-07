
> **Integrated Forward–Inverse Machine Learning and Optimization Framework for Process Control in Wire Arc Additive Manufacturing**

## Scope

This repository package contains the manuscript source and graphical assets needed to document the proposed forward–inverse–optimization workflow for Wire Arc Additive Manufacturing (WAAM).

The study uses an experimental dataset comprising **796 WAAM depositions** across **ER70S-6** and **AISI 316** material systems. The framework contains:

1. **Forward prediction** — process parameters → bead geometry.
2. **Inverse estimation** — target bead geometry → feasible process parameters.
3. **Optimization refinement** — iterative forward-model evaluation to reduce target–prediction mismatch.
4. **Two-layer validation concept** — geometry-driven refinement of subsequent deposition.

## Repository contents

```text
.
├── README.md
├── CITATION.cff
├── DOI.md
├── SCHEMATICS.md
├── figures/
│   ├── K.png
│   ├── K4.png
│   ├── K2.png
│   ├── K5.png
│   ├── C.png
│   ├── B.png
│   ├── A.png
│   └── ...performance and optimization figures
└── manuscript/
    ├── main.tex
    └── references.bib
```

## Main computational formulation

The framework represents WAAM as a nonlinear process operator:

\[
\mathbf{y}= \mathcal{F}_{WAAM}(\mathbf{x})+\boldsymbol{\eta},
\]

where the process vector is

\[
\mathbf{x}=[V,\mathrm{WFS},\mathrm{TS},\mathrm{CTWD}]^T
\]

and the geometry vector is

\[
\mathbf{y}=[\bar h,\bar w,\sigma_h^2,\sigma_w^2]^T.
\]

The inverse model supplies an initial process vector and the optimization layer subsequently minimizes the mismatch between desired and forward-predicted geometry.

## Data and code status

The manuscript currently states that the 796-run dataset and custom machine-learning/optimization codes are available from the corresponding author upon reasonable request, with future public release through an appropriate repository.

**Important:** this repository package therefore does **not** claim to contain the full experimental dataset or executable training/optimization code unless those files are added separately.

## Reproducibility

For a complete public release, the repository should additionally include:

- the 796-run machine-readable dataset;
- data dictionary/schema;
- preprocessing and train/test split scripts;
- forward-model training scripts;
- inverse-model training scripts;
- optimization/refinement scripts;
- environment specification (`requirements.txt` or `environment.yml`);
- exact model hyperparameters;
- random seeds;
- evaluation scripts;
- a machine-readable results table;
- license information.

## DOI

No dataset/repository DOI is present in the supplied folder. A DOI should be assigned only after depositing the public repository in a DOI-minting archive such as Zenodo or an institutional repository.

Do **not** invent a DOI. Replace the placeholder in `DOI.md` and `CITATION.cff` after the repository has been formally deposited.

## License

No repository license is specified in the supplied manuscript package. A license should be selected before public release. For code and data, separate licenses may be appropriate.

## Citation

See [`CITATION.cff`](CITATION.cff). The citation metadata intentionally leaves the repository DOI as a placeholder until a real DOI is minted.

## Related manuscript

The manuscript source is provided under `manuscript/`. The figures used in the paper are retained under `figures/`.
