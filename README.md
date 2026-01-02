# 🏦 Bank Customer Churn Analysis & Prediction

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis faktor-faktor utama yang menyebabkan nasabah berhenti menggunakan layanan bank (**churn**) dan membangun model prediktif untuk mengidentifikasi nasabah yang berisiko tinggi. Dengan prediksi yang akurat, bank dapat mengambil langkah proaktif untuk meningkatkan retensi pelanggan.

## 📊 Dataset
Dataset terdiri dari 10.000 data nasabah dengan fitur-fitur utama seperti:
- **Demografi**: Usia, Jenis Kelamin, Negara Asal.
- **Finansial**: Skor Kredit, Saldo (*Balance*), Estimasi Gaji.
- **Relasi Bank**: Jumlah Produk, Status Member Aktif, Kepemilikan Kartu Kredit.
- **Target**: `churn` (1 = Berhenti, 0 = Bertahan).

## 🛠️ Alur Kerja
1. **Exploratory Data Analysis (EDA)**: Menemukan pola bahwa nasabah non-aktif dan nasabah dengan jumlah produk banyak memiliki kecenderungan churn yang lebih tinggi.
2. **Feature Engineering**: Menyiapkan data untuk model machine learning menggunakan *StandardScaler* dan *OneHotEncoder*.
3. **Modelling**: Membandingkan Logistic Regression dengan **XGBoost**.
4. **Optimization**: Melakukan tuning pada *threshold* klasifikasi dan menggunakan `scale_pos_weight` untuk menangani data yang tidak seimbang.

## 📈 Performa Model
Model terbaik menggunakan **XGBoost** dengan hasil evaluasi:
- **ROC-AUC Score**: 0.86.
- **Recall (Churn Class)**: 0.71 (setelah optimalisasi threshold).

## 🎯 Insight & Rekomendasi Bisnis
- **Masalah Produk**: Nasabah dengan jumlah produk tinggi justru berisiko churn, menunjukkan perlunya evaluasi harga atau manfaat produk.
- **Program Loyalitas**: Nasabah non-member sangat rentan churn; disarankan memberikan insentif untuk meningkatkan status keanggotaan aktif.
- **Edukasi Finansial**: Memberikan perhatian khusus atau layanan tambahan pada nasabah dengan skor kredit rendah.

## 💻 Library Utama
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-Learn
- XGBoost
