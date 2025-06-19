# Analisis Pola Aktivitas Harian menggunakan Sequence Pattern Mining dan Clustering pada FitBit LifeSnaps

## Deskripsi Proyek
Proyek ini merupakan bagian dari tugas akhir mata kuliah *Penambangan Data* di Universitas Negeri Surabaya. Proyek ini bertujuan untuk menganalisis pola aktivitas harian pengguna wearable device Fitbit dengan menggabungkan pendekatan **Sequence Pattern Mining (SPM)** dan **Clustering**, menggunakan dataset **Fitbit LifeSnaps**.

## Tujuan
- Mengidentifikasi pola urutan aktivitas dan tidur pengguna menggunakan algoritma PrefixSpan.
- Mengelompokkan pengguna berdasarkan kemiripan perilaku aktivitas harian menggunakan teknik K-Means dan PCA.
- Menyediakan wawasan mengenai hubungan antara pola aktivitas, kepribadian, tingkat stres, dan motivasi olahraga pengguna.

## Dataset
Dataset yang digunakan berasal dari **LifeSnaps Fitbit Dataset**, yang mencakup:
- **Data Daily**: Aktivitas harian (langkah, kalori, detak jantung, waktu tidur, dll.)
- **Data Scored Surveys**: Survei psikologis (TTM, BREQ, STAI, PANAS, dan Big Five Personality).

Sumber Dataset: [https://www.kaggle.com/datasets/skywescar/lifesnaps-fitbit-dataset?resource=download]

## Metodologi

### 1. Exploratory Data Analysis (EDA)
- Visualisasi distribusi data numerik dan kategorik.
- Korelasi antar variabel.
- Penanganan missing values menggunakan KNN dan modus.
- Deteksi dan penanganan outlier menggunakan IQR.

### 2. Sequence Pattern Mining (PrefixSpan)
- Diskretisasi fitur numerik menjadi level (rendah, sedang, tinggi).
- Penyusunan urutan aktivitas per pengguna berdasarkan waktu.
- Penerapan algoritma PrefixSpan untuk menemukan pola aktivitas berulang.
- Segmentasi pengguna ke dalam 3 kategori:
  - Aktif & Sehat
  - Kurang Gerak
  - Stres / Kurang Istirahat

### 3. Clustering
- **Clustering 1** (Aktivitas): Berdasarkan fitur langkah, kalori, dan menit aktivitas berat. K=3 (Aktif, Sedang, Pasif).
- **Clustering 2** (Risiko Kesehatan): Berdasarkan fitur waktu sedentari, detak jantung istirahat, usia, dan BMI. PCA + K-Means digunakan untuk visualisasi dan penentuan risiko.

## Insight Tambahan
### Berdasarkan Data Survei:
- **TTM**: Segmen aktif & sehat memiliki skor tertinggi dalam pemberdayaan sosial.
- **STAI**: Aktivitas fisik berkorelasi negatif dengan tingkat stres.
- **Personality**: Intellect dan Conscientiousness tinggi terkait dengan segmen aktif & sehat.
- **PANAS**: Segmen stres memiliki emosi yang lebih intens dan variatif.
- **BREQ**: Segmen aktif didominasi oleh motivasi intrinsik dan teridentifikasi.

## Tools dan Library
- Python (Pandas, Numpy, Scikit-Learn, Matplotlib, Seaborn)
- PrefixSpan (SPM library)
- Google Colab

## Kontributor
- Alisha Deana Tabina – 23031554244
- Krisjen Fraulein Hutagalung – 23031554232
- Putri Manika Rukmamaya – 23031554091

---

> Proyek ini bertujuan tidak hanya untuk eksplorasi teknikal, tetapi juga memahami pola hidup dan mendukung upaya peningkatan kualitas hidup berbasis data.
