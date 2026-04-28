<<<<<<< HEAD
Supervised Learning: Linear Regression

📁 USA Housing Price Prediction

Deskripsi
Project ini bertujuan untuk memprediksi harga rumah menggunakan metode **Linear Regression**, salah satu algoritma dalam *supervised learning*. Model ini digunakan untuk memahami hubungan antara beberapa variabel (fitur) dengan harga rumah, sehingga dapat digunakan untuk melakukan prediksi pada data baru.
Fitur yang digunakan dalam model meliputi:

* Rata-rata pendapatan area
* Usia rata-rata rumah
* Jumlah rata-rata ruangan
* Jumlah kamar tidur
* Populasi area
Dataset yang digunakan adalah **USA Housing Dataset**, yang berisi data numerik terkait kondisi perumahan di berbagai area.

Dataset
**File:** `USA_Housing.csv`
**Variabel Independen (X):**

* Avg. Area Income
* Avg. Area House Age
* Avg. Area Number of Rooms
* Avg. Area Number of Bedrooms
* Area Population

Teknologi & Library
Project ini dikembangkan menggunakan bahasa Python dengan library berikut:

* `numpy` → perhitungan numerik
* `pandas` → manipulasi dan analisis data
* `matplotlib` & `seaborn` → visualisasi data
* `scikit-learn` → pembuatan dan evaluasi model machine learning
* `scipy` → analisis statistik

Metodologi
### 1. Data Preparation
* Dataset dimuat menggunakan **pandas**
* Kolom yang tidak relevan dihapus
* Data dipisahkan menjadi:

**Fitur (X)** sebagai input model
**Target (y)** sebagai output yang diprediksi

### 2. Exploratory Data Analysis (EDA)
Tahap ini dilakukan untuk memahami karakteristik data:
* Analisis statistik deskriptif (mean, median, standar deviasi)
* Visualisasi distribusi data menggunakan histogram dan density plot
* Analisis hubungan antar variabel:

**Pairplot** untuk melihat pola hubungan
**Heatmap** untuk melihat tingkat korelasi

### 3. Data Splitting
Dataset dibagi menjadi:
**70% data training** → untuk melatih model
**30% data testing** → untuk evaluasi performa model

### 4. Model Training
Model yang digunakan adalah:
**Linear Regression (scikit-learn)**
Model menghasilkan:
**Intercept** → nilai dasar prediksi
**Koefisien** → besarnya pengaruh masing-masing fitur terhadap harga rumah

### 5. Evaluasi Model
Performa model dievaluasi menggunakan data testing dengan metrik berikut:
**MAE (Mean Absolute Error)**
  Mengukur rata-rata kesalahan absolut antara nilai prediksi dan aktual
**RMSE (Root Mean Squared Error)**
  Mengukur kesalahan dengan penalti lebih besar pada error yang tinggi
**R² Score (R-squared)**
  Menunjukkan kemampuan model dalam menjelaskan variasi data (semakin mendekati 1 semakin baik)

Hasil & Analisis
**R² ≈ 0.92**
  Model mampu menjelaskan sekitar 92% variasi data, yang menunjukkan performa sangat baik
**MAE rendah**
  Menunjukkan bahwa rata-rata kesalahan prediksi relatif kecil
**RMSE lebih besar dari MAE**
  Mengindikasikan adanya beberapa nilai ekstrem (*outlier*) dalam data
**Pengaruh fitur terhadap harga:**
**Avg. Area House Age** dan **Avg. Area Number of Rooms**
  → Memiliki pengaruh paling besar
**Avg. Area Income**
  → Stabil dan signifikan
**Avg. Area Number of Bedrooms**
  → Pengaruh relatif kecil

Uji Asumsi Regresi
Untuk memastikan model valid, dilakukan beberapa pengujian:
**Normalitas Residual**
  Residual mengikuti distribusi normal (cukup terpenuhi berdasarkan uji Shapiro-Wilk)
**Homoskedastisitas**
  Tidak ditemukan pola tertentu pada residual plot (variansi error stabil)
**Outlier**
  Terdapat beberapa data ekstrem yang mempengaruhi performa model

✅ Kesimpulan
Model **Linear Regression** mampu memberikan prediksi harga rumah dengan akurasi tinggi dan dapat menjelaskan sebagian besar variasi dalam dataset.
Namun, performa model masih dipengaruhi oleh keberadaan **outlier**. Untuk pengembangan selanjutnya, dapat dilakukan:
=======
## 📊 Supervised Learning – Classification (Iris Dataset)

### 📌 Deskripsi Project

Project ini bertujuan untuk mengimplementasikan algoritma **K-Nearest Neighbors (KNN)** dalam melakukan klasifikasi pada dataset Iris. Model digunakan untuk memprediksi spesies bunga Iris berdasarkan karakteristik fisiknya.

Dataset yang digunakan adalah **Iris Dataset**, yang terdiri dari beberapa fitur numerik seperti panjang dan lebar sepal serta petal.

---

### 📂 Dataset

* **Nama file**: iris.csv
* **Jumlah data**: 150 sampel
* **Jumlah fitur**: 4 fitur numerik

---

### 🔢 Fitur (Independent Variables)

* Sepal Length (cm)
* Sepal Width (cm)
* Petal Length (cm)
* Petal Width (cm)

---

### 🎯 Target (Dependent Variable)

* Species:

  * Setosa
  * Versicolor
  * Virginica

---

### ⚙️ Library yang Digunakan

Project ini menggunakan beberapa library Python berikut:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

---

### 🔍 Tahapan Project

#### 1. Data Loading

Dataset dimuat menggunakan library pandas:

```python
train = pd.read_csv('iris.csv')
```

#### 2. Exploratory Data Analysis (EDA)

Analisis dilakukan untuk memahami karakteristik dan distribusi data, meliputi:

* Informasi dataset (`info()`)
* Statistik deskriptif (`describe()`)
* Visualisasi data:

  * Countplot untuk distribusi spesies
  * Histogram Sepal Length
  * Boxplot untuk melihat sebaran fitur

---

#### 3. Data Preprocessing

Tahapan preprocessing meliputi:

* Pengecekan missing values
* Encoding label menggunakan **LabelEncoder**
* Pembagian dataset:

  * 70% data training
  * 30% data testing

---

#### 4. Feature Scaling

Karena algoritma KNN sensitif terhadap skala data, dilakukan normalisasi menggunakan **StandardScaler**:

```python
from sklearn.preprocessing import StandardScaler
```

---

#### 5. Model Training (KNN)

Model KNN dilatih menggunakan:

```python
from sklearn.neighbors import KNeighborsClassifier
```

Parameter default serta beberapa variasi parameter digunakan untuk membandingkan performa model.

---

#### 6. Hyperparameter Tuning

Optimasi parameter dilakukan menggunakan **GridSearchCV** dengan parameter berikut:

* `n_neighbors`: [3, 5, 7]
* `weights`: ['uniform', 'distance']
* `metric`: ['euclidean', 'manhattan']

Evaluasi model dilakukan menggunakan beberapa metrik:

* Accuracy
* Precision
* Recall
* F1-Score

---

#### 7. Evaluasi Model

Model dievaluasi menggunakan:

* Accuracy Score
* Confusion Matrix
* Classification Report

---

### 📈 Hasil

Model KNN menunjukkan performa yang sangat baik dalam mengklasifikasikan data Iris, dengan tingkat akurasi yang tinggi (mendekati 100%, tergantung pada parameter yang digunakan).

Hasil terbaik diperoleh dari kombinasi parameter optimal yang dihasilkan oleh GridSearch.
>>>>>>> 720a409 (update)

---

### 🔮 Prediksi Data Baru

Model yang telah dilatih dapat digunakan untuk memprediksi data baru, contohnya:

```python
new_data = np.array([[5.1, 3.5, 1.4, 0.2]])
prediction = best_model.predict(new_data)
```

Hasil prediksi akan berupa label spesies bunga Iris.

---

### 📁 Output

Hasil proses GridSearch disimpan dalam file:
**hasil_gridsearch_knn.xlsx**

---