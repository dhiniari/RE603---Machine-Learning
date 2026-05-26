# 🍷 Wine Quality Clustering — Unsupervised Learning with K-Means

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📋 Deskripsi Project

Proyek ini merupakan **Tugas Week 8** mata kuliah Robotika yang membahas implementasi algoritma **K-Means Clustering** sebagai metode *unsupervised learning* untuk mengelompokkan data kualitas wine berdasarkan fitur kimiawi, yaitu **alcohol** dan **volatile acidity**.

Tujuan utama dari proyek ini adalah:
- Memahami konsep dan implementasi K-Means Clustering
- Menentukan jumlah cluster (K) optimal menggunakan **Metode Elbow** dan **Via Score Plot (Yellowbrick)**
- Membandingkan hasil clustering dengan label kualitas wine dari anotator

---

## 📁 Dataset

**File:** `WineQT.csv`

Dataset berisi informasi kualitas wine merah dengan fitur-fitur kimiawi. Fitur yang digunakan dalam clustering:

| Fitur | Deskripsi |
|---|---|
| `alcohol` | Kadar alkohol dalam wine |
| `volatile acidity` | Tingkat keasaman volatil wine |
| `quality` | Label kualitas wine (dari anotator, digunakan sebagai pembanding) |

---

## 🔧 Teknologi & Library

| Library | Kegunaan |
|---|---|
| `numpy` | Komputasi numerik |
| `pandas` | Manipulasi dan analisis data |
| `matplotlib` | Visualisasi data |
| `seaborn` | Visualisasi statistik |
| `scikit-learn` | Implementasi K-Means dan StandardScaler |
| `yellowbrick` | Visualisasi Via Score Plot untuk menentukan K optimal |

---

## 🚀 Alur Kerja

### 1. Load Dataset
Memuat dataset `WineQT.csv` dan melakukan eksplorasi awal.

### 2. Exploratory Data Analysis (EDA)
- Scatter plot hubungan `alcohol` vs `quality`
- Box plot dan histogram untuk fitur `alcohol` dan `volatile acidity`
- Statistik deskriptif dataset

### 3. Feature Engineering
- **Drop duplikat** — memastikan tidak ada baris data yang terduplikasi
- **Feature Scaling** menggunakan `StandardScaler` agar skala setiap fitur seimbang sebelum proses clustering

### 4. K-Means Clustering
Dua metode digunakan untuk menentukan jumlah cluster optimal:

#### 🔵 Metode Elbow
Menghitung *inertia* (Within-Cluster Sum of Squares) untuk K = 1 hingga 10 dan memilih titik "siku" grafik sebagai K optimal.
- **K optimal:** `3`
- **Pemetaan cluster:**
  - Cluster 0 → Kualitas Rendah *(Low Quality)*
  - Cluster 1 → Kualitas Sedang *(Medium Quality)*
  - Cluster 2 → Kualitas Tinggi *(High Quality)*

#### 🔴 Via Score Plot (Yellowbrick)
Menggunakan `KElbowVisualizer` dari library Yellowbrick untuk menghitung skor distorsi secara otomatis.
- **K optimal:** `4`
- Pemisahan cluster lebih granular, mencerminkan variasi kualitas wine yang lebih detail

### 5. Evaluasi & Perbandingan
Hasil clustering dibandingkan secara visual dengan label kualitas asli dari anotator menggunakan scatter plot.

---

## 📊 Hasil & Interpretasi

**Feature Scaling:**
Sebelum scaling, fitur `alcohol` dan `volatile acidity` memiliki rentang nilai yang berbeda jauh. Setelah `StandardScaler`, keduanya memiliki rata-rata 0 dan standar deviasi 1, sehingga tidak ada fitur yang mendominasi perhitungan jarak K-Means.

**Perbandingan Metode:**
- **Elbow (K=3):** Hasil clustering cukup representatif dan mendekati distribusi label quality dari anotator.
- **Via Score Plot (K=4):** Memberikan pemisahan yang lebih granular. Meskipun label quality memiliki 6 kategori, pola distribusi antar cluster cukup mencerminkan tingkat kualitas wine secara umum.

---

## 📂 Struktur File

```
📦 Week_8_Unsupervised_Learning
 ┣ 📓 Week_8_Assignment_Unsupervised_learning_KMeans.ipynb
 ┣ 📊 WineQT.csv
 ┗ 📄 README.md
```

---

## ▶️ Cara Menjalankan

1. **Clone / unduh** repositori ini
2. Pastikan semua library sudah terinstall:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn yellowbrick
   ```
3. Letakkan file `WineQT.csv` di direktori yang sama dengan notebook
4. Jalankan Jupyter Notebook:
   ```bash
   jupyter notebook Week_8_Assignment_Unsupervised_learning_KMeans.ipynb
   ```
5. Jalankan semua sel secara berurutan (*Run All*)

---

## 👤 Author

| Info | Detail |
|---|---|
| **Nama** | Dhini Ari Minarti |
| **NIM** | 4222311022 |
| **Kelas** | Robotika A Malam |
| **Tugas** | Week 8 — Unsupervised Learning: K-Means Clustering |

---

## 📝 Lisensi

Proyek ini dibuat untuk keperluan akademik. Seluruh hak cipta milik penulis.