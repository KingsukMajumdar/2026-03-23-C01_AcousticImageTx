# 2026-03-23-C01_AcousticImageTx
# Acoustic Binary Image Transmission -- Simulation Data
### IEEE CIACON 2026

**Author:** Kingsuk Majumdar  
Department of Electrical Engineering  
Dr. B. C. Roy Engineering College, Durgapur 713206  
West Bengal, India

---

## About

This repository contains the simulation output data for the paper:

> K. Majumdar, "Acoustic Binary Image Transmission Using FSK and
> BPSK Modulation with RLE Compression and Hamming Error Correction:
> A Simulation Study," *IEEE CIACON 2026*, Durgapur, India, July 2026.

---

## Contents

| Folder | Description |
|--------|-------------|
| `Results_16x16/` | Figures and CSV data for 16x16 px simulation |
| `Results_32x32/` | Figures and CSV data for 32x32 px simulation |

---

## File Description

| File | Description |
|------|-------------|
| `Fig1_BER_SNR_AWGN.png` | BER vs SNR -- FSK vs BPSK (AWGN) |
| `Fig2_BER_SNR_Multipath.png` | BER vs SNR -- FSK vs BPSK (Multipath+AWGN) |
| `Fig3_ECC_Comparison.png` | Hamming(7,4) ECC benefit |
| `Fig4_Image_Quality_SNR.png` | PSNR and SSIM vs SNR |
| `Fig5_RLE_Compression.png` | RLE compression ratio |
| `Fig6_Image_Mosaic.png` | Image reconstruction at various SNR levels |
| `exp1..5_*.csv` | Raw numerical data for each experiment |
| `simulation_summary.txt` | Run summary and parameters |

---

## Simulation Parameters

| Parameter | Value |
|-----------|-------|
| Sample rate | 44100 Hz |
| Symbol duration | 5 ms (200 bps) |
| FSK tones | 1000 Hz, 2000 Hz |
| BPSK carrier | 1500 Hz |
| SNR range | -5 to 20 dB |
| Hamming code | (7,4), rate 4/7 |

---

*Data generated using Python 3.13 on Manjaro Linux.*  
*Copyright (c) 2026 Kingsuk Majumdar*
