# Laporan Proyek Machine Learning - Nama Anda

## Project Overview

Anime merupakan salah satu jenis konten multimedia yang sangat populer di dunia, terutama di negara-negara Asia seperti Jepang dan negara-negara lain di Asia Tenggara. Penggemar anime sangat banyak dan beragam, mulai dari anak-anak hingga dewasa. Namun, dengan banyaknya anime yang tersedia, seringkali penggemar anime kesulitan untuk menemukan anime yang sesuai dengan keinginan mereka. Oleh karena itu, diperlukan sebuah sistem rekomendasi yang dapat memberikan rekomendasi anime yang sesuai dengan preferensi pengguna.

Untuk menyelesaikan masalah ini, kami akan menggunakan metode machine learning yang disebut Neural Collaborative Filter (NCF) dan Multi Layer Perceptron (MLP). NCF adalah metode rekomendasi yang menggabungkan teknik deep learning dengan collaborative filtering, yang dapat memprediksi rating anime yang akan diberikan oleh pengguna berdasarkan interaksi pengguna dengan anime lainnya. Sementara itu, MLP adalah metode deep learning yang dapat digunakan untuk memprediksi hasil yang diinginkan dengan menggunakan beberapa lapisan dari neuron.

## Business Understanding

Masalah yang diidentifikasi dari latar belakang tersebut adalah kesulitan dalam menemukan anime yang sesuai dengan preferensi pengguna. Penggemar anime sering mengalami kesulitan dalam menemukan anime yang sesuai dengan keinginan mereka karena banyaknya anime yang tersedia. Oleh karena itu, diperlukan sebuah sistem rekomendasi yang dapat memberikan rekomendasi anime yang sesuai dengan preferensi pengguna.

### Problem Statements

Menjelaskan pernyataan masalah:
- Berapa nilai RMSE yang mampu dihasilkan oleh model rekomendasi?
- Berapa nilai *loss* yang mampu dihasilkan oleh model rekomendasi?

### Goals

Menjelaskan tujuan proyek yang menjawab pernyataan masalah:
- Mendapatkan nilai RMSE dari model rekomendasi.
- Mendapatkan nilai *loss* dari model rekomendasi.

### Solution statements
Secara keseluruhan, masalah yang akan diselesaikan dalam project ini adalah menciptakan sebuah sistem rekomendasi anime yang dapat memberikan rekomendasi anime yang sesuai dengan preferensi pengguna dengan menggunakan metode machine learning Neural Collaborative Filter (NCF) dan Multi Layer Perceptron (MLP). Dalam project ini, data yang akan digunakan adalah data rating anime yang diberikan oleh pengguna. Data ini akan digunakan untuk melakukan analisis dan menentukan pola preferensi pengguna. Metode NCF akan digunakan untuk menentukan korelasi antara pengguna dan anime yang mereka rating, serta menentukan rekomendasi anime yang sesuai dengan preferensi pengguna. Sedangkan metode MLP akan digunakan untuk melakukan analisis data dan memberikan rekomendasi anime yang sesuai dengan preferensi pengguna.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai jumlah data, kondisi data, dan informasi mengenai data yang digunakan. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya, uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data beserta insight atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model sisten rekomendasi yang Anda buat untuk menyelesaikan permasalahan. Sajikan top-N recommendation sebagai output.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menyajikan dua solusi rekomendasi dengan algoritma yang berbeda.
- Menjelaskan kelebihan dan kekurangan dari solusi/pendekatan yang dipilih.

## Evaluation
Pada bagian ini Anda perlu menyebutkan metrik evaluasi yang digunakan. Kemudian, jelaskan hasil proyek berdasarkan metrik evaluasi tersebut.

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

## Kesimpulan

## Daftar Referensi

