# Edutech-Jaya-Jaya-Institut-Classification

## Business Understanding
Jaya Jaya Institut merupakan salah satu institusi pendidikan perguruan yang telah berdiri sejak tahun 2000. Hingga saat ini ia telah mencetak banyak lulusan dengan reputasi yang sangat baik. Akan tetapi, terdapat banyak juga siswa yang tidak menyelesaikan pendidikannya alias dropout.

Jumlah dropout yang tinggi ini tentunya menjadi salah satu masalah yang besar untuk sebuah institusi pendidikan. Oleh karena itu, Jaya Jaya Institut ingin mendeteksi secepat mungkin siswa yang mungkin akan melakukan dropout sehingga dapat diberi bimbingan khusus.

### Permasalahan Bisnis
1. Mengatasi masalah jumlah dropout yang tinggi di Jaya Jaya Institut
2. Membuat Dashboard untuk memantau dan monitoring performa siswa
3. Membuat model machine learning yang dapat digunakan untuk mendeteksi lebih awal mengenai siswa yang kemungkinan akan dropout

### Cakupan Proyek
1. Business Understanding
   Memahami latar belakang bisnis, serta masalah yang dihadapi yang akan kita selesaikan melalui proyek ini
2. Data Understanding
   Memahami gambaran besar dari data yang akan diolah, seperti mengecek apakah ada missing value dalam data, apakah ada duplikasi data, korelasi antar fitur, EDA, dsb.
3. Data Preparation
   Melakukan pemrosesan data seperti mengatasi missing value dalam data jika ada, duplikat dalam data jika ada, melakukan drop untuk menghapus fitur-fitur yang dianggap tidak relevan untuk tahap modelling, splitting data dan scalling data, hingga data sudah bersih dan siap untuk di proses di tahap modelling.
4. Modelling
   Membuat model machine learning yang tepat untuk mengatasi masalah klasifikasi kasus ini, disini saya menggunakan model random forest, yang mana model akan berguna untuk mengantisipasi, memprediksi lebih awal, serta mencegah siswa yang akan drop out di Jaya Jaya Institut.
5. Evaluation
   Melakukan evaluasi model, untuk melihat seberapa baik model yang sudah kita bangun sebelumnya.
6. Deployment
   Membuat sistem prototype atau UI/UX sederhana untuk menjalankan model machine learning yang telah di buat melalui streamlit app. 


### Persiapan

Sumber data: https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/data.csv

Setup environment:
```
Setup environment Anaconda:
conda create --name dropout-prediction python=3.11.12
conda activate dropout-prediction
pip install -r requirements.txt

Setup environment Shell/Terminal:
mkdir dropout-prediction
cd dropout-prediction
pipenv install
pipenv shell
pip install -r requirements.txt
```
Proyek ini diselesaikan dengan menggunakan model random forest, berkas-berkas yang diperlukan antara lain:
- Model random forest: randomforest_model.joblib
- Scaler: scaler_jjinstitut.joblib
- file app.py

## Business Dashboard
Jelaskan tentang business dashboard yang telah dibuat. Jika ada, sertakan juga link untuk mengakses dashboard tersebut.

## Menjalankan Sistem Machine Learning

Langkah-langkah menjalankan sistem:
1. Akses streamlit app, lalu isi data sesuai data mahasiswa, seperti yang ada di tampilan app, seperti usia saat enrollment, jumlah kurikulum semester 1 diambil, dst...
2. Klik tombol prediksi
3. Hasil prediksi akan menampilkan: Siswa beresiko tinggi akan dropout / Siswa berpotensi akan graduate

Link streamlit app dapat diakses melalui link dibawah ini:
```
https://edutech-jaya-jaya-institut-classification-zyag2zmwr7nlxnbehkj5.streamlit.app/
```

## Conclusion
Jelaskan konklusi dari proyek yang dikerjakan.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- action item 1
- action item 2
