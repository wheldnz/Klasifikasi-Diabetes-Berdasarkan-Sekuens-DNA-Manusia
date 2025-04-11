# 🧬 Machine Learing Klasifikasi Diabetes Berdasarkan Sekuens DNA Menggunakan Support Vector Machine (SVM)

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

## 🔄 Preprocessing Data

Proses preprocessing data melibatkan beberapa tahap penting sebelum dilakukan pelatihan model:

### a. Pembersihan Data
Langkah ini bertujuan untuk memastikan data akurat, konsisten, dan layak digunakan untuk pemodelan. Beberapa langkah yang dilakukan adalah:

1. **Whitespace**  
   Menghapus spasi yang tidak perlu dalam sekuens DNA.

2. **Penghapusan Nucleotida yang Tidak Dikenal**  
   DNA yang mengandung karakter selain A, C, G, atau T (misalnya ‘N’) dihapus karena dianggap noise.

3. **Penghapusan Duplikasi**  
   Hanya satu salinan sekuens DNA yang disimpan jika ada data duplikat.

---

### b. Transformasi Data

Data DNA yang masih dalam bentuk teks diubah menjadi representasi numerik agar bisa diproses oleh algoritma machine learning. Proses ini menggunakan teknik **4-mers (tokenisasi 4 karakter berturut-turut)**.

Contoh representasi:

| 4-mers | Representasi Numerik |
|--------|----------------------|
| AAAC   | 12                   |
| AACA   | 13                   |
| ACGG   | 14                   |

---

### c. Oversampling Data

Untuk mengatasi ketidakseimbangan kelas, digunakan metode **SMOTE (Synthetic Minority Over-sampling Technique)**. Teknik ini menambahkan sampel sintetis ke kelas minoritas agar seimbang dengan kelas mayoritas.

---

### d. Pembagian Data

Dataset dibagi menjadi dua bagian:

- **Data Pelatihan (Training Set)**: digunakan untuk melatih model.
- **Data Pengujian (Testing Set)**: digunakan untuk mengevaluasi performa model.

Pembagian dilakukan secara acak dengan proporsi umum seperti 80:20 atau 70:30, tergantung strategi validasi.
di proyek kali ini memakai 80:20

---


## 🧪 Metodologi

### 1. **Pra-pemrosesan**
- Tokenisasi sekuens DNA menggunakan teknik **k-mers** (pengujian dengan k = 3, 4, dan 5).
- Ekstraksi fitur dengan menghitung frekuensi setiap k-mer sebagai representasi numerik dari DNA.

### 2. **Pemodelan**
- Menggunakan algoritma **Support Vector Machine (SVM)**.
- Kernel yang diuji:
  1. RBF (Radial Basis Function)
  2. Polinomial
  3. Sigmoid
- Pengujian nilai **C**:
  0.01, 0.1, 1, 10, 100

### 3. **Evaluasi**
- Menggunakan metrik:
- Akurasi
- Precision, Recall, F1-score
- 
<p align="center">
<img src="results/akurasi terbaik.png" width="450"/>
<br/>
<em> Akurasi Terbaik</em>
</p>

---

## 🏆 Hasil Terbaik

| Parameter        | Nilai         |
|------------------|---------------|
| Ukuran k-mer     | 4             |
| Kernel           | RBF           |
| Nilai C          | 10            |
| Akurasi          | **96%**       |

<p align="center">
<img src="results/confusion matrix terbaik.png" width="450"/>
<br/>
<em>Confusion Matrix - Model Terbaik</em>
</p>

---


## ✍️ Tentang Proyek Ini

Proyek ini dikembangkan sebagai bagian dari portofolio **Data Science** untuk menunjukkan penerapan machine learning dalam bidang bioinformatika dan kesehatan. Topik ini dipilih karena diabetes merupakan penyakit kronis dengan angka prevalensi tinggi, dan pendekatan berbasis DNA dapat memberikan kontribusi penting dalam deteksi dini penyakit.

---
## 🔍 Insight Penting

> Model Machine Learning berbasis **SVM** menunjukkan performa luar biasa dalam klasifikasi data genomik.

Beberapa insight penting:

- Representasi fitur sangat berpengaruh: penggunaan **4-mers** menghasilkan vektor fitur yang mampu membedakan antar kelas dengan sangat baik.
- Kernel **RBF** unggul karena mampu menangkap **pola non-linear** dalam data DNA yang kompleks.
- Pemilihan parameter **C = 10** memberikan keseimbangan terbaik antara bias dan variansi.
- **Akurasi 96%** menunjukkan bahwa model klasik seperti SVM dapat mengungguli deep learning dalam beberapa kasus — terutama ketika data **terstruktur dan bersih**.
- Model ini lebih cepat dilatih, ringan, dan mudah diimplementasikan.
---

📌 Lihat juga pendekatan deep learning untuk topik yang sama di sini:
👉 [Deep Learning untuk Klasifikasi DNA](https://github.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-)

---

## 👤 Kontributor

**Nama:** _M. Wildan Nuril Akmal 
**Minat:** Data Science, Machine Learning bioinformatika  


## 📬 Kontak

Ingin berdiskusi lebih lanjut atau membutuhkan file csv nya?

- 📧 Email: [wildanuril99@email.com]  
- 💼 LinkedIn: [www.linkedin.com/in/wildan-nuril]



