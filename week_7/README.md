# Supervised Learning - Classification (Titanic Dataset)

## Deskripsi Project
Project ini merupakan hands-on supervised learning untuk kasus **classification** menggunakan dataset Titanic. Notebook ini berisi proses lengkap mulai dari:

- Import library
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data preprocessing
- Training model machine learning
- Evaluasi model klasifikasi

Dataset yang digunakan adalah dataset Titanic untuk memprediksi apakah penumpang selamat (**Survived**) atau tidak.

---

# Tools dan Library
Beberapa library yang digunakan pada project ini:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Model machine learning yang digunakan meliputi:

- Logistic Regression
- K-Nearest Neighbor (KNN)
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- Naive Bayes

---

# Dataset
Dataset yang digunakan:

- `titanic.csv`

Dataset berisi informasi penumpang Titanic seperti:

| Feature | Deskripsi |
|---|---|
| PassengerId | ID penumpang |
| Survived | Status selamat atau tidak |
| Pclass | Kelas penumpang |
| Name | Nama penumpang |
| Sex | Jenis kelamin |
| Age | Umur |
| SibSp | Jumlah saudara/pasangan |
| Parch | Jumlah orang tua/anak |
| Ticket | Nomor tiket |
| Fare | Harga tiket |
| Cabin | Nomor kabin |
| Embarked | Pelabuhan keberangkatan |

---

# Alur Project

## 1. Import Library
Notebook dimulai dengan mengimpor library yang dibutuhkan untuk analisis data, visualisasi, dan machine learning.

## 2. Load Dataset
Dataset Titanic dibaca menggunakan `pandas.read_csv()`.

```python
train = pd.read_csv('titanic.csv')
```

## 3. Exploratory Data Analysis (EDA)
Tahapan EDA dilakukan untuk memahami data.

Analisis yang dilakukan:

- Informasi dataset (`info()`)
- Statistik deskriptif (`describe()`)
- Visualisasi jumlah penumpang selamat
- Analisis hubungan antara:
  - Survived vs Sex
  - Survived vs Pclass
  - Survived vs SibSp
- Distribusi umur penumpang
- Distribusi umur berdasarkan kelas penumpang

Visualisasi menggunakan:

- Histogram
- Countplot
- Barplot
- Boxplot

---

## 4. Feature Engineering
Pada tahap ini dilakukan preprocessing data seperti:

- Mengisi missing value pada kolom `Age`
- Menghapus kolom yang tidak digunakan
- Encoding data kategorikal
- Membersihkan data

Contoh imputasi umur:

```python
def impute_age(cols):
    Age = cols[0]
    Pclass = cols[1]

    if pd.isnull(Age):
        if Pclass == 1:
            return 37
        elif Pclass == 2:
            return 29
        else:
            return 24
    else:
        return Age
```

---

## 5. Data Splitting
Dataset dibagi menjadi:

- Data training
- Data testing

Menggunakan:

```python
train_test_split()
```

---

## 6. Training Model
Beberapa model klasifikasi dilatih menggunakan dataset Titanic.

Tujuan model:

- Memprediksi apakah penumpang selamat atau tidak.

---

## 7. Evaluasi Model
Model dievaluasi menggunakan beberapa metric seperti:

- Accuracy
- Confusion Matrix
- Classification Report

Evaluasi dilakukan untuk membandingkan performa masing-masing model.

---

# Output Project
Output yang dihasilkan dari notebook ini:

- Visualisasi data Titanic
- Dataset yang telah diproses
- Model machine learning classification
- Hasil evaluasi performa model

---

# Cara Menjalankan Project

## 1. Install Library
Pastikan seluruh library telah terinstall.

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## 2. Jalankan Notebook
Buka notebook menggunakan:

- Jupyter Notebook
- Google Colab
- VS Code

Lalu jalankan seluruh cell secara berurutan.

---

# Struktur File

```bash
├── Week_5_6_7_Supervised_Learning_Hands_On_Classification_All_tanpa_tuning.ipynb
├── titanic.csv
└── README.md
```

---

# Tujuan Pembelajaran
Project ini membantu memahami:

- Dasar supervised learning
- Classification pada machine learning
- Exploratory Data Analysis
- Data preprocessing
- Training dan evaluasi model
- Penggunaan scikit-learn

---

# Kesimpulan
Notebook ini menunjukkan proses lengkap pembuatan model supervised learning untuk kasus classification menggunakan dataset Titanic. Mulai dari analisis data, preprocessing, training model, hingga evaluasi performa model machine learning.

---

# Author
Dhini Ari Minarti  
Robotics Engineering - Politeknik Negeri Batam

