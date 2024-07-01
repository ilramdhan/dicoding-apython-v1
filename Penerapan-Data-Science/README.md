# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding (Background)

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. 

Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

Untuk mencegah hal ini semakin parah, manajer departemen HR ingin meminta bantuan Anda mengidentifikasi berbagai faktor yang mempengaruhi tingginya attrition rate tersebut. Selain itu, ia juga meminta Anda untuk membuat business dashboard untuk membantunya memonitori berbagai faktor tersebut.


### Permasalahan Bisnis

<!-- Tuliskan seluruh permasalahan bisnis yang akan diselesaikan. -->
Permasalahan bisnis yang akan diselesaikan mencakup identifikasi faktor-faktor yang mempengaruhi tingginya attrition rate di Jaya Jaya Maju dan memprediksi kemungkinan karyawan mengalami attrition. Selain itu, proyek ini akan menganalisis tingkat kepuasan dan keterlibatan karyawan serta pengaruh faktor demografis dan pekerjaan terhadap attrition. Serta membangun dashboard bisnis untuk memonitor dan melaporkan faktor-faktor attrition secara real-time, membantu manajer HR dalam pengambilan keputusan yang lebih baik.

### Cakupan Proyek
<!-- Tuliskan cakupan proyek yang akan dikerjakan. -->

1. Pengumpulan dan Pemahaman Data:
    - Pada proyek ini datset sudah tersedia, terlampir link dataset pada sub dibawah.
    - Memahami struktur dan karakteristik data, termasuk jenis variabel, jumlah data, dan nilai-nilai yang hilang atau tidak valid.

2. Eksplorasi Data Analysis (EDA):
    - Melakukan eksplorasi data awal untuk mengidentifikasi pola, tren, dan hubungan antar variabel.
    - Visualisasi data untuk memahami distribusi variabel dan mendeteksi anomali atau outlier.

3. Pembersihan dan Persiapan Data:
    - Menangani nilai-nilai yang hilang, duplikat, atau tidak valid dalam dataset.
    - Mengonversi variabel-variabel yang diperlukan menjadi format yang sesuai untuk analisis lebih lanjut.
    - Normalisasi atau standarisasi variabel numerik jika diperlukan.

4. Analisis Faktor-Faktor yang Mempengaruhi Attrition:
    - Melakukan analisis statistik untuk mengidentifikasi variabel-variabel yang paling signifikan mempengaruhi attrition.
    - Menggunakan teknik korelasi untuk menemukan hubungan antar variabel.

5. Pengembangan Model Prediksi Attrition:
    - Membagi dataset menjadi data latih dan data uji untuk pengembangan model prediksi.
    - Menggunakan resampling SMOTE, RAndom Under Sampling dan Tanpa Resampling
    - Membangun dan melatih model prediksi menggunakan algoritma machine learning. Model machine learning yang digunakan pada proyek ini:
        - random forest
        - logistic regression
        - decision tree
        - XGB
        - Gradien Boosting
        - SVM
    - Mengevaluasi performa model

6. Merancang dan membangun dashboard interaktif menggunakan `Metabase` yang terintegrasi dengan `Supabase`.

Dengan cakupan proyek yang jelas, diharapkan dapat memberikan hasil yang komprehensif dan actionable bagi Jaya Jaya Maju dalam mengurangi tingkat attrition dan meningkatkan manajemen karyawan.

### Persiapan

Sumber data: <a href="https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee">Dataset Employee Jaya Jaya Maju</a> 



### Setup environment:

Buka cmd as administrator

```bash
pip install -r requirements.txt
```


## Run Steamlit Prediction Apps

Untuk menjalankan aplikasi ini, kamu harus masuk ke folder (_directory_) yang sesuai dengan file `prediction.py` berada, kemudian masukkan command berikut dan tekan Enter:
```bash
streamlit run prediction.py
```
 Atau akses secara online: <a href="https://employee-attrition-prediction-ml.streamlit.app/">HR - Employee Attrition Prediction App</a> 



### Fitur:

1. Melakukan prediksi dengan mengupload data karyawan dalam format `.csv`, sudah ada juga contoh file yang bisa kamu coba di `dataset/sample_test.csv`. Terdapat slider untuk mengatur banyaknya data yang ingin dipratinjau.
2. Pemilihan model machine learning yang memungkinkan _user_ dapat beriteraksi dengan aplikasi menjadi lebih baik.
3. Hasil prediksi dapat didownload dalam format `.csv` sehingga menjadi lebih mudah diakses.


## Business Dashboard

Dashboard ini menyajikan score card yang menampilkan metrik penting seperti jumlah karyawan, attrition rate, departemen, rata-rata masa kerja, dan metrik lainnya dari dataset karyawan Perusahaan Jaya Jaya Maju. Terdapat juga line chart yang menggambarkan tingkat atau jumlah attrition berdasarkan kelompok usia dan jarak rumah ke tempat kerja. Selain itu, dashboard ini menampilkan jumlah karyawan berdasarkan tingkat pendidikannya serta job satisfaction rating untuk semua job role. Ada juga pie chart yang menunjukkan perbandingan tingkat attrition berdasarkan gender, department, dan marital status. Dashboard ini juga dilengkapi dengan filter.


## Conclusion

- Karyawan yang berusia 31-35 tahun memiliki tingkat attrition tertinggi, diikuti oleh kelompok usia 25-30 tahun sebagai yang kedua tertinggi. Hal ini mungkin menunjukkan bahwa karyawan dalam rentang usia ini mencari pengalaman baru atau upah yang lebih baik sebagai motivasi untuk berpindah.

- Tingkat attrition lebih tinggi di departemen Sales dibandingkan dengan departemen lainnya.

- Model machine learning Logistic Regression dan SVM tanpa resampling merupakan 2 model yang mempunyai tingkat stabilitas yang cukup baik dan akurasi yang tinggi. Sehingga kedua model tersebut digunakan sebagai acuan untuk melakukan prediksi data baru yang dapat dilakukan pada aplikasi prediksi Streamlit.



### Rekomendasi Action Items (Optional)

- Bagian departemen Sales memiliki tingkat attrition yang tinggi, evaluasi kembali apakah perusahaan memberikan kendaraan inventaris yang cukup kepada karyawan yang sering melakukan perjalanan dinas. Jika mereka harus menggunakan kendaraan pribadi tentu hal ini memberatkan karyawan dan memilih untuk keluar dari perusahaan. Tentu tidak hanya sebatas ini, terdapat faktor lain seperti kondisi kendaraan yang dinventariskan dan sebagainya.

- Memberikan promosi kepada karyawan yang berusia 31-35 tahun yang memiliki kemampuan kerja yang baik.

- Menyediakan fasilitas seperti ruang istirahat yang nyaman, gym, atau daycare. Sehingga karyawan dapat merilekskan diri sehingga tidak tegang dalam melakukan pekerjaan.

- Mengadakan acara dan kegiatan sosial untuk membangun rasa kebersamaan dan komunitas di antara karyawan. Hal ini dapat meningkatkan semangat dan motivasi karyawan.
