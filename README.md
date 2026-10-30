# Effects of Lighting Augmentation on Industrial Anomaly Detection

DATA 255, Team 1, Fall 2026.

We will study whether additional brightness and contrast augmentation helps
EfficientAD detect defects under changed lighting while preserving performance
under regular lighting. The study uses the Rice and Walnuts categories of
MVTec AD 2.

## Current status

The group project is confirmed. This repository contains the proposal, planned
experiment settings, data access instructions and team responsibilities. Model
implementation and measured pilot results will be added next. Dependency
versions will be recorded after the pilot establishes a working environment.

The downloaded dataset is stored separately from this repository. Raw images,
model weights and local environment files are excluded from Git.

## Study

| Part | Planned approach |
| --- | --- |
| Reference baseline | Small convolutional autoencoder trained on normal images |
| Strong baseline | EfficientAD-S using Anomalib |
| Investigation | Extra brightness and contrast augmentation during training |
| Main comparison | Combined augmentation (S11) versus original EfficientAD (S00) |
| Ablations | Remove brightness (S01) or contrast (S10) from the combined setting |
| Seeds | 11, 22 and 33, paired across settings |
| Primary metric | Image AUROC pooled over shifted lighting within each category, averaged equally across categories |

Preserve official splits. Use normal validation data for calibration and
thresholds, and freeze choices before final test evaluation. Keep lighting views
of each physical scene together when estimating uncertainty.

The full plan has 30 training runs across Rice and Walnuts. The Rice-only minimum
has 15. The proposed compute budget is an allocation, not a measured runtime;
the 1,000-step pilot will determine feasibility.

## Repository layout

- `docs/proposal.pdf`: proposal for team review and course submission.
- `docs/proposal.docx`: editable version of the same proposal.
- `docs/team.md`: technical responsibilities; owners remain unassigned.
- `docs/references.md`: dataset, paper, implementation and pretrained-model sources.
- `docs/assistance.md`: record of material AI assistance.
- `configs/study.json`: planned settings; training code does not consume it yet.
- `data/README.md`: download instructions and dataset location convention.
- `notebooks/`: future data, training and evaluation notebooks.
- `src/`: future reusable helpers for those notebooks.
- `results/`: small result summaries and figures after experiments run.

## Getting the data

Follow [data/README.md](data/README.md). Copy `.env.example` to `.env` and set
`MVTEC_AD2_ROOT` to the extracted dataset root. To export it in a local shell:

```sh
set -a
source .env
set +a
```

Do not copy the dataset into a tracked directory or commit local `.env` files.

## Team workflow

Choose an owner for each role in [docs/team.md](docs/team.md). Implement each
component on a separate branch and review changes through pull requests. Keep
notebook output concise; record configurations, seeds and final checkpoints
outside Git, with access instructions alongside reported results.

Every member contributes code, analysis and writing for their assigned area,
reviews another member's work, and understands the full system. Before final
submission, a member who did not write the evaluation component must reproduce
one reported evaluation from the README and saved artifacts.

## Data license and attribution

MVTec AD 2 is licensed under CC BY-NC-SA 4.0. Follow its attribution,
noncommercial and share-alike terms. The dataset is not distributed in this
repository. Credit reused software, pretrained models and auxiliary data under
their respective terms; see [docs/references.md](docs/references.md).
