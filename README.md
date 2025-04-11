# 🧬 Klasifikasi Diabetes Berdasarkan Sekuens DNA Menggunakan Support Vector Machine (SVM)

Proyek ini bertujuan untuk mengklasifikasikan jenis Diabetes Mellitus (Tipe 1, Tipe 2, dan Non-Diabetes) berdasarkan data sekuens DNA manusia. Klasifikasi dilakukan menggunakan algoritma Support Vector Machine (SVM) dengan berbagai jenis kernel dan pengujian parameter. Proyek ini menggabungkan pendekatan bioinformatika dan machine learning dalam pengembangan model prediktif di bidang kesehatan.

---

## 📌 Ringkasan Proyek

- **Masalah**: Prediksi jenis diabetes dari data sekuens DNA.
- **Pendekatan**: Mengubah DNA menjadi fitur numerik menggunakan teknik k-mers dan mengklasifikasikan menggunakan SVM.
- **Tujuan**: Menemukan kombinasi terbaik antara ukuran k-mer, jenis kernel, dan nilai parameter C untuk mendapatkan akurasi terbaik.

---

## 🧰 Teknologi yang Digunakan

- Python
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📁 Dataset

- **Total Data**: 2.967 sekuens DNA
- **Kelas**:
  | Kelas             | Jumlah |
  |------------------|--------|
  | DMT1 (Diabetes Tipe 1)   | 989    |
  | DMT2 (Diabetes Tipe 2)   | 989    |
  | NON-DM (Non-diabetes)    | 989    |

- **Contoh Format CSV**:
id,sequence,label 1,ATGCTAGCTAGCTAGCTA,DMT1 2,TGACTGATCGTACGTAGC,DMT2 ...

---

## 🧪 Metodologi

### 1. **Pra-pemrosesan**
- Tokenisasi sekuens DNA menggunakan teknik **k-mers** (pengujian dengan k = 3, 4, dan 5).
- Ekstraksi fitur dengan menghitung frekuensi setiap k-mer sebagai representasi numerik dari DNA.

### 2. **Pemodelan**
- Menggunakan algoritma **Support Vector Machine (SVM)**.
- Kernel yang diuji:
- RBF (Radial Basis Function)
- Polinomial
- Sigmoid
- Pengujian nilai **C**:
- 0.01, 0.1, 1, 10, 100

### 3. **Evaluasi**
- Menggunakan metrik:
- Akurasi
- Precision, Recall, F1-score
- Confusion Matrix
- ROC Curve

---

## 🏆 Hasil Terbaik

| Parameter        | Nilai         |
|------------------|---------------|
| Ukuran k-mer     | 4             |
| Kernel           | RBF           |
| Nilai C          | 10            |
| Akurasi          | **96%**       |

<p align="center">
<img src="results/confusion_matrix.png" width="450"/>
<br/>
<em>Confusion Matrix - Model Terbaik</em>
</p>

---

## 📊 Visualisasi

- Wordcloud fitur paling sering muncul untuk masing-masing kelas:

<p align="center">
<img src="results/wordcloud_positive.png" width="320"/>
<img src="results/wordcloud_negative.png" width="320"/>
<br/>
<em>Visualisasi Wordcloud k-mers dominan</em>
</p>

- Visualisasi ROC dan laporan klasifikasi lainnya tersedia di folder `/results/`.

---


## ✍️ Tentang Proyek Ini

Proyek ini dikembangkan sebagai bagian dari portofolio **Data Science** untuk menunjukkan penerapan machine learning dalam bidang bioinformatika dan kesehatan. Topik ini dipilih karena diabetes merupakan penyakit kronis dengan angka prevalensi tinggi, dan pendekatan berbasis DNA dapat memberikan kontribusi penting dalam deteksi dini penyakit.

---

## 📬 Kontak

Ingin berdiskusi lebih lanjut atau tertarik pada topik serupa?

- 📧 Email: [wildanuril99@email.com]  
- 💼 LinkedIn: [www.linkedin.com/in/wildan-nuril]



