# 📊 Prediksi Pelanggan Gagal Bayar (Credit Default Prediction)

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk memprediksi pelanggan yang berpotensi gagal bayar menggunakan pendekatan machine learning classification.
Model dibangun untuk membantu pengambilan keputusan berbasis data, khususnya dalam konteks manajemen risiko kredit.

Fokus utama evaluasi model adalah Recall, karena dalam kasus gagal bayar, false negative (pelanggan bermasalah tapi tidak terdeteksi) memiliki risiko bisnis yang lebih besar.

### 🎯 Objective

* Membangun model prediksi gagal bayar pelanggan
* Membandingkan performa beberapa algoritma klasifikasi
* Melakukan hyperparameter *tuning* menggunakan GridSearchCV
* Menentukan model dengan performa Recall terbaik


### 🧠 Business Context

Dalam industri keuangan, kesalahan mengklasifikasikan pelanggan berisiko sebagai pelanggan aman dapat menimbulkan kerugian besar.
Oleh karena itu, proyek ini memprioritaskan Recall, agar pelanggan berisiko dapat terdeteksi sebanyak mungkin.

### 📂 Dataset

Dataset berisi informasi pelanggan, antara lain:
* Informasi demografis
* Informasi cabang dan kota
* Riwayat kepemilikan kartu kredit per kuartal
* Riwayat saldo (Balance) per kuartal
* Label target: status gagal bayar

Dataset dibagi menjadi dua subset (df1 dan df2) untuk keperluan eksperimen dan validasi model.

## 🛠 Tools & Library
- Python
- Pandas – manipulasi data
- NumPy – komputasi numerik
- Matplotlib – visualisasi
- Scikit-learn - Preprocessing, modeling, dan evaluasi
- Jupyter Notebook

## 🔎 Tahapan Analisis
1. Data Understanding
   * Mengecek struktur data dan tipe variabel
   * Mengidentifikasi missing value dan inkonsistensi kolom
   * Memahami distribusi target
2. Data Preprocessing
   * Casting tipe data numerik & kategorikal
   * Feature engineering:
     * Mean Balance
     * Delta Balance
     * Vintage kepemilikan kartu kredit
   * Encoding variabel kategorikal
   * Pemisahan fitur numerik dan kategorikal

3. Feature Engineering
    Beberapa fitur baru yang dibuat:
   * Mean Balance: rata-rata saldo pelanggan
   * Delta Balance: perubahan saldo antar periode
   * Vintage_CR: lamanya pelanggan memiliki kartu kredit

## 🤖 Modeling

Model yang digunakan:
* Logistic Regression

Teknik yang diterapkan:
* Train-test split dengan stratifikasi
* GridSearchCV untuk hyperparameter tuning
* Evaluasi berbasis Recall Score

## 📈 Evaluasi Model

Alasan memilih Recall:

* Lebih penting mendeteksi pelanggan berisiko daripada menghindari false positive

* Cocok untuk konteks manajemen risiko kredit

Output evaluasi:

* Recall score terbaik dari GridSearch

* Parameter optimal Logistic Regression

## ✅ Kesimpulan

* Model mampu mengidentifikasi pelanggan berisiko gagal bayar dengan cukup baik

* Feature engineering memiliki kontribusi signifikan terhadap performa model

* Pendekatan ini dapat dijadikan dasar untuk sistem credit scoring yang lebih kompleks

🚀 Pengembangan Selanjutnya

* Menambahkan model lain (Random Forest, XGBoost)

* Feature selection & multicollinearity check

* Handling imbalance data (SMOTE / class weight)

* Model interpretability (coef analysis, SHAP)


👤 Author

Mario Baswara

Data Analyst Enthusiast | Aspiring Data Scientist