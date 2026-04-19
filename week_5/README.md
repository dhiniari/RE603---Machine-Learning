Versi kamu sebenarnya sudah bagus—tinggal sedikit dipoles supaya lebih **lebih profesional, mengalir, dan enak dibaca** (cocok untuk laporan atau GitHub). Ini versi yang sudah diperhalus:

---

## 📊 Supervised Learning: Linear Regression

## 📁 USA Housing Price Prediction

### 📌 Deskripsi

Project ini bertujuan untuk memprediksi harga rumah menggunakan metode **Linear Regression**, salah satu algoritma dalam *supervised learning*. Model ini digunakan untuk memahami hubungan antara beberapa variabel (fitur) dengan harga rumah, sehingga dapat digunakan untuk melakukan prediksi pada data baru.

Fitur yang digunakan dalam model meliputi:

* Rata-rata pendapatan area
* Usia rata-rata rumah
* Jumlah rata-rata ruangan
* Jumlah kamar tidur
* Populasi area

Dataset yang digunakan adalah **USA Housing Dataset**, yang berisi data numerik terkait kondisi perumahan di berbagai area.

---

### 📂 Dataset

**File:** `USA_Housing.csv`

**Variabel Independen (X):**

* Avg. Area Income
* Avg. Area House Age
* Avg. Area Number of Rooms
* Avg. Area Number of Bedrooms
* Area Population

**Variabel Dependen (y):**

* Price (Harga rumah)

**Catatan:**
Kolom **Address** dihapus karena tidak memiliki nilai numerik dan tidak berkontribusi secara langsung terhadap proses pemodelan.

---

### ⚙️ Teknologi & Library

Project ini dikembangkan menggunakan bahasa Python dengan library berikut:

* `numpy` → perhitungan numerik
* `pandas` → manipulasi dan analisis data
* `matplotlib` & `seaborn` → visualisasi data
* `scikit-learn` → pembuatan dan evaluasi model machine learning
* `scipy` → analisis statistik

---

### 🔍 Metodologi

#### 1. Data Preparation

* Dataset dimuat menggunakan **pandas**
* Kolom yang tidak relevan dihapus
* Data dipisahkan menjadi:

  * **Fitur (X)** sebagai input model
  * **Target (y)** sebagai output yang diprediksi

---

#### 2. Exploratory Data Analysis (EDA)

Tahap ini dilakukan untuk memahami karakteristik data:

* Analisis statistik deskriptif (mean, median, standar deviasi)
* Visualisasi distribusi data menggunakan histogram dan density plot
* Analisis hubungan antar variabel:

  * **Pairplot** untuk melihat pola hubungan
  * **Heatmap** untuk melihat tingkat korelasi

---

#### 3. Data Splitting

Dataset dibagi menjadi:

* **70% data training** → untuk melatih model
* **30% data testing** → untuk evaluasi performa model

---

#### 4. Model Training

Model yang digunakan adalah:

* **Linear Regression (scikit-learn)**

Model menghasilkan:

* **Intercept** → nilai dasar prediksi
* **Koefisien** → besarnya pengaruh masing-masing fitur terhadap harga rumah

---

#### 5. Evaluasi Model

Performa model dievaluasi menggunakan data testing dengan metrik berikut:

* **MAE (Mean Absolute Error)**
  Mengukur rata-rata kesalahan absolut antara nilai prediksi dan aktual

* **RMSE (Root Mean Squared Error)**
  Mengukur kesalahan dengan penalti lebih besar pada error yang tinggi

* **R² Score (R-squared)**
  Menunjukkan kemampuan model dalam menjelaskan variasi data (semakin mendekati 1 semakin baik)

---

### 📈 Hasil & Analisis

* **R² ≈ 0.92**
  Model mampu menjelaskan sekitar 92% variasi data, yang menunjukkan performa sangat baik

* **MAE rendah**
  Menunjukkan bahwa rata-rata kesalahan prediksi relatif kecil

* **RMSE lebih besar dari MAE**
  Mengindikasikan adanya beberapa nilai ekstrem (*outlier*) dalam data

**Pengaruh fitur terhadap harga:**

* **Avg. Area House Age** dan **Avg. Area Number of Rooms**
  → Memiliki pengaruh paling besar
* **Avg. Area Income**
  → Stabil dan signifikan
* **Avg. Area Number of Bedrooms**
  → Pengaruh relatif kecil

---

### 🧪 Uji Asumsi Regresi

Untuk memastikan model valid, dilakukan beberapa pengujian:

* **Normalitas Residual**
  Residual mengikuti distribusi normal (cukup terpenuhi berdasarkan uji Shapiro-Wilk)

* **Homoskedastisitas**
  Tidak ditemukan pola tertentu pada residual plot (variansi error stabil)

* **Outlier**
  Terdapat beberapa data ekstrem yang mempengaruhi performa model

---

### ✅ Kesimpulan

Model **Linear Regression** mampu memberikan prediksi harga rumah dengan akurasi tinggi dan dapat menjelaskan sebagian besar variasi dalam dataset.

Namun, performa model masih dipengaruhi oleh keberadaan **outlier**. Untuk pengembangan selanjutnya, dapat dilakukan:

* Penanganan atau pembersihan outlier
* Feature engineering untuk meningkatkan kualitas fitur
* Penggunaan model yang lebih kompleks untuk perbandingan

