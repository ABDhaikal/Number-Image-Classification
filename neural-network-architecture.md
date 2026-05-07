# Dokumentasi Arsitektur CNN MNIST

## Ringkasan
Model menggunakan arsitektur CNN sederhana untuk klasifikasi digit tulisan tangan MNIST dengan input grayscale 1x28x28 dan output 10 kelas (0-9).

## Detail Arsitektur
- Input: 1x28x28 (grayscale)
- Conv Block 1:
  - Conv2D: 32 filter, kernel 3x3, padding 1
  - BatchNorm2D (32)
  - ReLU
  - MaxPool 2x2
- Conv Block 2:
  - Conv2D: 64 filter, kernel 3x3, padding 1
  - BatchNorm2D (64)
  - ReLU
  - MaxPool 2x2
- Flatten: 64 x 7 x 7
- Fully Connected:
  - FC1: 64*7*7 -> 128, ReLU
  - Dropout: 0.5
  - FC2: 128 -> 10 (logits)

## Catatan Implementasi
- Fungsi aktivasi utama: ReLU
- Output layer menghasilkan logits untuk 10 kelas digit.
