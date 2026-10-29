# Team responsibilities

Team 1: Bavishna Ashok Kumar, Chao Zheng, Jim He and Nithya Anantharaman.
The team will assign the four role slots below. Listing names here does not
assign a role.

| Owner | Role | Tasks | Deliverables |
| --- | --- | --- | --- |
| [Team member 1] | Data and reference model | Verify data and split/scene records; build the image loader and tiling; train the reference autoencoder for three seeds per category. | Shared loader, split manifest, autoencoder code and saved models. |
| [Team member 2] | EfficientAD baseline | Set up EfficientAD-S, pretrained teacher and auxiliary data; implement standard training/calibration; train S00 for three seeds per category. | Reusable baseline code, saved models and training logs. |
| [Team member 3] | Lighting experiments | Use baseline code to add S10, S01 and S11; run the planned seeds with fixed controls; record configurations and runtime. | Augmentation code, configurations, saved models and run logs. |
| [Team member 4] | Evaluation and analysis | Evaluate all saved models using the fixed protocol; calculate metrics/uncertainty; measure latency; inspect errors. | Evaluation code, tables, figures and findings. |

## Handoffs

Member 1 supplies the shared data loader. Member 2 supplies working EfficientAD
code to member 3. Members 1–3 supply saved models and run records to member 4.
Each area has one primary owner.

## Required verification and contributions

Each member writes the methods and results for their area, reviews another
member's work, understands the full system and can explain one experiment.
The team will assign one cross-review per person.

A non-author must reproduce one reported evaluation using the README and saved
artifacts. Record the command, configuration, result and any discrepancies or
fixes. Keep individual contribution statements and confidential peer assessments
as required by the course. All four members speak in the final presentation.
