# Machine-learning

# EDA & Feature Engineering Project
  Repository ini berisi implementasi Exploratory Data Analysis (EDA) dan Feature Engineering menggunakan Python dalam bentuk Jupyter Notebook. Project ini bertujuan untuk mempersiapkan data sebelum digunakan dalam proses Machine Learning agar menghasilkan model yang lebih optimal.

## Deskripsi
  Pada project ini, dilakukan analisis awal terhadap dataset untuk memahami struktur dan karakteristik data. Proses ini mencakup identifikasi tipe data, pengecekan missing values, serta eksplorasi distribusi data menggunakan berbagai teknik visualisasi.
  Setelah tahap eksplorasi, dilakukan proses Feature Engineering untuk meningkatkan kualitas dataset. Tahapan ini meliputi pembersihan data, transformasi fitur, encoding data kategorikal, serta normalisasi atau scaling data agar siap digunakan dalam model Machine Learning.

## Tools & Libraries
Project ini menggunakan beberapa library utama Python, yaitu:
- Pandas → manipulasi dan analisis data
- NumPy → operasi numerik
- Matplotlib & Seaborn → visualisasi data
- Scikit-learn → preprocessing (scaling & encoding)

## Workflow
1. Data Loading & Understanding
Dataset dibaca menggunakan Pandas, kemudian dilakukan eksplorasi awal seperti:
- Melihat struktur data (head, info, describe)
- Mengetahui tipe data tiap kolom

2. Data Cleaning
Dilakukan pembersihan data untuk memastikan kualitas dataset:
- Menangani missing values (fill atau drop)
- Menghapus data duplikat
- Membersihkan data yang tidak relevan

3. Exploratory Data Analysis (EDA)
Analisis dilakukan untuk memahami pola dalam data:
- Visualisasi distribusi data (histogram)
- Deteksi outlier (boxplot)
- Analisis korelasi antar fitur (heatmap)

4. Feature Engineering
🔹 Handling Outlier
    Outlier ditangani menggunakan metode statistik seperti IQR atau pendekatan tertentu sesuai kebutuhan data.
🔹 Encoding
    Data kategorikal diubah menjadi numerik menggunakan:
    - Label Encoding
    - One Hot Encoding
  
5. Feature Scaling
Dilakukan normalisasi agar semua fitur berada dalam skala yang sama:
- StandardScaler → untuk data dengan distribusi normal
- MinMaxScaler → untuk rentang [0, 1]

# Kesimpulan
  EDA dan Feature Engineering merupakan tahap penting dalam Machine Learning. Dengan memahami data dan melakukan preprocessing yang tepat, performa model dapat meningkat secara signifikan. Tanpa proses ini, model berpotensi menghasilkan prediksi yang kurang akurat.

# Author
4222311022_Dhini Ari Minarti
