# References and reused components

## Research papers

1. Heckler-Kram et al. **The MVTec AD 2 Dataset: Advanced Scenarios for
   Unsupervised Anomaly Detection.** IJCV, 134, article 175, 2026.
   [Publisher](https://link.springer.com/article/10.1007/s11263-026-02743-0).
   Provides the dataset and native lighting-shift setting.
2. Batzner, Heckler and König. **EfficientAD: Accurate Visual Anomaly Detection
   at Millisecond-Level Latencies.** WACV 2024.
   [Paper](https://openaccess.thecvf.com/content/WACV2024/html/Batzner_EfficientAD_Accurate_Visual_Anomaly_Detection_at_Millisecond-Level_Latencies_WACV_2024_paper.html).
   Provides the strong baseline.
3. Thomine and Snoussi. **Single-Layer Distillation with Fourier Convolutions
   for Texture Anomaly Detection.** WACV 2025.
   [Paper](https://openaccess.thecvf.com/content/WACV2025/html/Thomine_Single-Layer_Distillation_with_Fourier_Convolutions_for_Texture_Anomaly_Detection_WACV_2025_paper.html).
   Motivates compact distillation and texture-error analysis. Implementing
   SingleNet is outside the study scope.

## Software, data and weights

- [Official MVTec AD 2 dataset and license](https://www.mvtec.com/research-teaching/datasets/mvtec-ad-2).
- [Researcher repository linking the mirror](https://github.com/yuxin-jiang/Anomagic).
- [Pinned AnomVerse mirror](https://huggingface.co/datasets/yuxinjiang11/AnomVerse/tree/47809f7e8f0ec9991cc03083aeeba82d83cd3abf).
- [Anomalib EfficientAD source reviewed for the proposal](https://github.com/open-edge-platform/anomalib/tree/dac2a62544d17f5cfef8152dc40f4ccafdc01df6/src/anomalib/models/image/efficient_ad).
- [EfficientAD pretrained teacher release](https://github.com/open-edge-platform/anomalib/releases/tag/efficientad_pretrained_weights).
- [Imagenette auxiliary dataset](https://github.com/fastai/imagenette).

Record the package versions, asset hashes, pretraining provenance and licenses
used in the actual pilot. The source snapshot above is a reference for setup;
it is not evidence that a model has run in the project environment.
