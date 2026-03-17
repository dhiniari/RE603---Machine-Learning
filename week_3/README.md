# Machine-learning

# Feature Engineering - Machine Learning Preprocessing

Project ini berisi proses **Feature Engineering** untuk persiapan data sebelum dilakukan Machine Learning Modeling.

## Dataset

Dataset yang digunakan dalam project ini:

* California Housing Dataset
* Company Dataset
* Telco Customer Churn Dataset

---

## Feature Engineering Process

### 1. Outlier Handling

Metode yang digunakan: **Interquartile Range (IQR)**

Kolom yang dianalisis:

* MedInc
* HouseAge
* AveRooms
* AveBedrms
* AveOccup

Outlier di-handle pada kolom **MedInc** menggunakan metode **IQR**.

---

### 2. Missing Value Handling

Dataset: **company.csv**

Aturan handling:

| Data Type   | Method |
| ----------- | ------ |
| Numeric     | Median |
| Categorical | Mode   |

Kolom **Headquarters** memiliki missing value yang diisi menggunakan **modus**.

---

### 3. Encoding

Encoding dilakukan untuk mengubah data kategorikal menjadi numerik.

#### One Hot Encoding

Kolom:

* gender

#### Label Encoding

Kolom:

* Partner
* Dependents
* StreamingMovies
* StreamingTV
* TechSupport
* DeviceProtection
* OnlineBackup
* OnlineSecurity
* MultipleLines

#### Mean Encoding

Kolom:

* Contract

Mean encoding dilakukan berdasarkan rata-rata nilai **Churn**.

---

## Libraries Used

Project ini menggunakan beberapa library Python berikut:

```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

## Author

**Moh Syuril Iswan**
