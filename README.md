# Tugas Besar Analisis Data Statistika
# Kelompok 4 – Kelas RB – 2025  
Kaleb Filbert Istel (124450053) · Helmy Surya Pratama (124450033) · Nabila Nur Azizah (124450048) · Rafa Sabina Fahimah (124450036)

## 1. Cara Menjalankan Script

1. Pastikan struktur folder repository sudah benar:
/data/
/code/
/output/
/poster/
README.md

2. Download dataset pada folder:
data/Dataset Tugas Besar ADS 2025.xlsx

3. Download script R utama pada folder:
code/codeR_6_RA.R

4. Buka script di RStudio lalu install paket yang dibutuhkan:
   
- install.packages(c("readr","dplyr","stringr","ggplot2","openxlsx","lmtest"))
- Pada bagian import data di Rmd "raw_df <- read_csv("C:/Main File Location/Downloads/ads-dataset.csv", show_col_types = FALSE)", jangan lupa untuk mengganti path sesuai dengan direktori masing-masing
- Jalankan script dengan menekan:
- Ctrl + Shift + Enter, atau
- klik Run All

## 2. Paket R yang Digunakan 

library(readr)      # Import dataset CSV
library(dplyr)      # Data cleaning, filtering
library(stringr)    # Ekstraksi pola teks (jam belajar & IPK)
library(ggplot2)    # Visualisasi (scatter, histogram, QQ plot)
library(openxlsx)   # Export data ke Excel
library(lmtest)     # Uji Breusch-Pagan (Homoskedastisitas)

## 3. Penjelasan Singkat Dataset

Dataset berasal dari Survei Karakteristik Mahasiswa ITERA (N = 458) , berisi informasi umum mahasiswa seperti IPK, data akademik, dan data sosial.
Dalam penelitian ini, fokus analisis diarahkan pada dua variabel utama:
- Jam belajar rata-rata per minggu (X) yang diekstraksi dari data teks dan dibersihkan menjadi nilai numerik jam/minggu.
- IPK (Y) yang dibersihkan dari berbagai format penulisan (3,25 / 3.25 / 3.)
Dataset kemudian diproses menjadi df_clean, yaitu data bersih yang hanya berisi:
- IPK valid (0–4)
- Jam belajar valid (1–84 jam/minggu)
Data ini digunakan untuk:
1. Analisis deskriptif
2. Korelasi Pearson
3. Regresi linear sederhana
4. Pengujian asumsi klasik OLS (linearitas, ekspektasi error = 0, homoskedastisitas, dan normalitas residual)

## 4. Struktur Repository

/data/     → dataset mentah & hasil cleaning  
/code/     → script R/Rmd (codeR_4_Rb.Rmd) serta knit pdf laporan Rmd 
/output/   → grafik, tabel, hasil olahan statistik  
/poster/   → poster A1 (PDF)  
README.md  → petunjuk 





