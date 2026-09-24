# Acoustic Binary Image Transmission -- Simulation Data
### IEEE CIACON 2026 | Paper ID: 865 |Dr. B. C. Roy Engineering College, Durgapur

---

> [!CAUTION]
> **Copyright (c) 2026 Kingsuk Majumdar. All rights reserved.**
> This repository contains simulation output data only. Redistribution,
> commercial use, and incorporation into other datasets are **strictly
> prohibited** without explicit written permission from the copyright
> holder. See [LICENSE](LICENSE) for full terms.

---

> [!IMPORTANT]
> If you use this data in your research, please cite:
>
> K. Majumdar, S. Sarkar, T. H. Mondal, P. Khanra, T. Mondal and S. Roy, “Acoustic Binary Image Transmission with Adaptive RLE Compression and Hamming Error Correction: System Design and Performance Analysis,” *2026 International Conference on Computing, Intelligence, and Applications (CIACON)*, Durgapur, India, 2026, pp. 1–6. [doi:10.1109/CIACON70148.2026.11688539](https://doi.org/10.1109/CIACON70148.2026.11688539). [IEEE Xplore](https://ieeexplore.ieee.org/document/11688539)

---

## About This Repository

This repository contains [GitHub Link](https://github.com/KingsukMajumdar/2026-03-23-C01_AcousticImageTx/blob/main/README.md) the simulation output data associated with the
paper (__Paper ID: 865__) submitted to **IEEE CIACON 2026** (2nd International Conference on
Computing, Intelligence, and Applications), organised by the Department
of Computer Science and Engineering, Dr. B. C. Roy Engineering College,
Durgapur, with technical sponsorship by IEEE Kolkata Section.

The data covers two image resolution stages:
- **Stage 1:** 16 x 16 pixel binary image (256 bits payload)
- **Stage 2:** 32 x 32 pixel binary image (1024 bits payload)

---


## Contents

| Folder | Description | Link |
|--------|-------------|------|
| `Results_16x16/` | Figures and CSV data for 16x16 px simulation | [clikc here ](https://github.com/KingsukMajumdar/2026-03-23-C01_AcousticImageTx/tree/main/16x16OUTPUT) |
| `Results_32x32/` | Figures and CSV data for 32x32 px simulation | [clikc here ](https://github.com/KingsukMajumdar/2026-03-23-C01_AcousticImageTx/tree/main/32x32OUTPUT) |



---

## Author

| Field | Details |
|-------|---------|
| **Name** | Kingsuk Majumdar, Ph.D. (Engg.) |
| **Designation** | Assistant Professor |
| **Department** | Electrical Engineering |
| **Institute** | Dr. B. C. Roy Engineering College (Autonomous), Durgapur |
| **ORCID** | [0000-0001-7224-4862](https://orcid.org/0000-0001-7224-4862) |
| **GitHub** | [KingsukMajumdar](https://github.com/KingsukMajumdar) |
| **YouTube** | [Learn With Kingsuk](https://www.youtube.com/@LearnWithKingsuk) |

---

## Repository Structure

```
2026-03-23-C01_AcousticImageTx/
├── LICENSE
├── README.md
├── Results_16x16/
│   ├── Fig1_BER_SNR_AWGN.png
│   ├── Fig2_BER_SNR_Multipath.png
│   ├── Fig3_ECC_Comparison.png
│   ├── Fig4_Image_Quality_SNR.png
│   ├── Fig5_RLE_Compression.png
│   ├── Fig6_Image_Mosaic.png
│   ├── Fig_Combined_BER_Comparison.png
│   ├── exp1_ber_snr_awgn.csv
│   ├── exp2_ber_snr_multipath.csv
│   ├── exp3_ecc_comparison.csv
│   ├── exp4_image_quality.csv
│   ├── exp5_rle_compression.csv
│   └── simulation_summary.txt
└── Results_32x32/
    ├── (same figures and CSV files for 32x32 run)
```

---

## Output File Descriptions

| File | Description |
|------|-------------|
| `Fig1_BER_SNR_AWGN.png` | BER vs SNR -- FSK vs BPSK (AWGN channel) |
| `Fig2_BER_SNR_Multipath.png` | BER vs SNR -- FSK vs BPSK (Multipath + AWGN) |
| `Fig3_ECC_Comparison.png` | Hamming(7,4) ECC benefit over uncoded FSK |
| `Fig4_Image_Quality_SNR.png` | PSNR and SSIM vs SNR |
| `Fig5_RLE_Compression.png` | Adaptive RLE compression ratio for four test patterns |
| `Fig6_Image_Mosaic.png` | Image reconstruction at six SNR levels |
| `Fig_Combined_BER_Comparison.png` | Combined FSK vs BPSK comparison figure |
| `exp1_ber_snr_awgn.csv` | Numerical BER data -- AWGN channel |
| `exp2_ber_snr_multipath.csv` | Numerical BER data -- Multipath channel |
| `exp3_ecc_comparison.csv` | BER with and without Hamming ECC |
| `exp4_image_quality.csv` | PSNR and SSIM values vs SNR |
| `exp5_rle_compression.csv` | RLE compression ratios for all patterns |
| `simulation_summary.txt` | Run parameters and output file list |

---

## Simulation Parameters

| Parameter | Value |
|-----------|-------|
| Sample rate | 44100 Hz |
| Symbol duration | 5 ms (200 bps) |
| FSK tones | 1000 Hz (bit 0), 2000 Hz (bit 1) |
| BPSK carrier | 1500 Hz |
| SNR range | -5 dB to 20 dB |
| Multipath delays | 0, 22, 44 samples |
| Multipath gains | 1.0, 0.25, 0.10 |
| Hamming code | (7,4), rate 4/7 |
| Simulation tool | Python 3.13, NumPy, SciPy, Matplotlib |
| Platform | Manjaro Linux, AMD Ryzen 9-8945HS |

---

## Key Results Summary

| Result | 16x16 | 32x32 |
|--------|-------|-------|
| Lossless SNR threshold (SSIM = 1.0) | 12 dB | 12 dB |
| Best RLE compression ratio (stripes) | 3.556 | 7.111 |
| Transmission time -- compressed | 630 ms | 1260 ms |
| Transmission time -- uncompressed | 2240 ms | 8960 ms |
| BPSK advantage over FSK (AWGN) | ~3 dB | ~3 dB |
| FSK multipath penalty | 1.5 dB | 1.5 dB |
| BPSK multipath penalty | 3.0 dB | 3.0 dB |

> [!NOTE]
> The lossless SNR threshold of **12 dB is stable across both image
> sizes** -- a key finding of this study termed the
> *ECC Threshold Stability Property*. The system does not require
> SNR re-optimisation as image resolution increases.



---

*Data generated: March 2026*
*Copyright (c) 2026 Kingsuk Majumdar*
