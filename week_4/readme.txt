📊 Supervised Learning: Linear Regression

📁 USA Housing Price Prediction

Deskripsi

Project ini bertujuan untuk memprediksi harga rumah menggunakan metode **Linear Regression**, yaitu salah satu algoritma dalam *supervised learning*. Model ini mempelajari hubungan antara beberapa faktor (fitur) dengan harga rumah, sehingga dapat digunakan untuk memperkirakan harga berdasarkan data baru.

Faktor yang digunakan meliputi:

* Rata-rata pendapatan area
* Usia rata-rata rumah
* Jumlah rata-rata ruangan
* Jumlah kamar tidur
* Populasi area

Dataset yang digunakan adalah **USA Housing Dataset**.
📂 Dataset
**File:** `USA_Housing.csv`
**Fitur (Variabel Independen / X):**

* Avg. Area Income
* Avg. Area House Age
* Avg. Area Number of Rooms
* Avg. Area Number of Bedrooms
* Area Population

### ⚙️ Teknologi & Library
Project ini menggunakan beberapa library Python, yaitu:

* `numpy` → operasi numerik
* `pandas` → pengolahan data
* `matplotlib` & `seaborn` → visualisasi data
* `scikit-learn` → pembuatan model machine learning
* `scipy` → analisis statistik

Metodologi
### 1. Data Preparation

* Dataset dibaca menggunakan **pandas**
* Kolom yang tidak diperlukan (Address) dihapus
* Data dipisahkan menjadi:

  * **X (fitur)** → variabel input
  * **y (target)** → harga rumah

### 2. Exploratory Data Analysis (EDA)
Tahap ini bertujuan untuk memahami data sebelum modeling:

* Analisis statistik deskriptif (mean, median, dll)
* Visualisasi distribusi data menggunakan histogram & density plot
* Analisis hubungan antar variabel:

  * **Pairplot** → melihat hubungan antar fitur
  * **Heatmap** → melihat korelasi antar variabel

### 3. Data Splitting
Dataset dibagi menjadi:
*70% data training** → untuk melatih model
*30% data testing** → untuk menguji performa model

### 4. Model Training
Model yang digunakan adalah:
*Linear Regression (scikit-learn)**
Output dari model:

**Intercept** → nilai dasar prediksi
**Koefisien** → pengaruh masing-masing fitur terhadap harga

### 5. Evaluasi Model
Model diuji menggunakan data testing dengan metrik berikut:
**MAE (Mean Absolute Error)**
  → Mengukur rata-rata selisih antara nilai prediksi dan nilai asli
**RMSE (Root Mean Squared Error)**
  → Mengukur error dengan penalti lebih besar untuk kesalahan besar
**R² Score (R-squared)**
  → Menunjukkan seberapa baik model menjelaskan variasi data (nilai mendekati 1 berarti sangat baik)

### 📈 Hasil & Analisis
**R² ≈ 0.92**
  → Model mampu menjelaskan sekitar 92% variasi harga rumah (sangat baik)
**MAE rendah**
  → Rata-rata kesalahan prediksi kecil
**RMSE > MAE**
  → Menunjukkan adanya beberapa data dengan error besar (*outlier*)

**Pengaruh Fitur:**
* **Avg. Area House Age** & **Avg. Area Number of Rooms**
  → Paling berpengaruh terhadap harga
* **Avg. Area Income**
  → Berpengaruh signifikan dan stabil
* **Avg. Area Number of Bedrooms**
  → Pengaruh relatif kecil

Uji Asumsi Regresi
Untuk memastikan model valid, dilakukan beberapa pengujian:
**Normalitas Residual**
  → Residual (error) mengikuti distribusi normal (cukup terpenuhi, diuji dengan Shapiro-Wilk)
**Homoskedastisitas**
  → Tidak ada pola tertentu pada plot residual (variansi error stabil)
**Outlier**
  → Masih terdapat beberapa data ekstrem yang mempengaruhi hasil model

Kesimpulan
Model **Linear Regression** mampu memprediksi harga rumah dengan akurasi yang tinggi dan memberikan hasil yang cukup baik dalam menjelaskan hubungan antar variabel.
Namun, masih terdapat beberapa **outlier** yang dapat mempengaruhi performa model. Untuk peningkatan ke depan, dapat dilakukan:

* Penanganan outlier
* Feature engineering
* Mencoba model lain yang lebih kompleks
