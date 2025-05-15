# Edutech-Jaya-Jaya-Institut-Classification

## Business Understanding
Jaya Jaya Institut merupakan salah satu institusi pendidikan perguruan yang telah berdiri sejak tahun 2000. Hingga saat ini ia telah mencetak banyak lulusan dengan reputasi yang sangat baik. Akan tetapi, terdapat banyak juga siswa yang tidak menyelesaikan pendidikannya alias dropout.

Jumlah dropout yang tinggi ini tentunya menjadi salah satu masalah yang besar untuk sebuah institusi pendidikan. Oleh karena itu, Jaya Jaya Institut ingin mendeteksi secepat mungkin siswa yang mungkin akan melakukan dropout sehingga dapat diberi bimbingan khusus.

### Permasalahan Bisnis
Jaya Jaya Insititut merupakan perusahaan pendidikan yang telah berdiri sejak tahun 2000, telah mencetak banyak lulusan dengan reputasi yang sangat baik. Namun, masih banyak siswa juga yang tidak menyelesaikan pendidikannya atau dropout. Jumlah dropout yang tinggi menjadi masalah yang besar untuk sebuah institusi pendidikan. Agar tetap membuat nama Jaya Jaya Institut lebih baik lagi, perusahaan berniat untuk mengidentifikasi faktor-faktor apa saja yang mempengaruhi siswa dropout di Jaya Jaya Institut, dan ingin segera mendeteksi kira-kira siswa mana saja yang berpotensi untuk dropout, sehingga dapat diantisipasi dengan memberikan bimbingan khusus. Oleh karena itu, Jaya Jaya Institut ingin memiliki sistem machine learning yang dapat membantu mereka dalam mengatasi hal tersebut dan membutuhkan dashboard yang dapat memonitor para siswa mereka, demi tercapainya penyelesaian masalah dari Jaya Jaya Institut.

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
Business Dashboard ini dibuat dengan tujuan memonitoring data siswa Jaya Jaya Insitut yang kemungkinan akan dropout, ada beberapa fitur yang ada dalam business dashboard yang telah dibuat yang mempengaruhi tingkat dropout siswa di Jaya Jaya Institut. Dashboard dibuat dengan bantuan tools looker studio.

Dashboard dapat diakses melalui: https://lookerstudio.google.com/reporting/fd718ad9-d855-41c9-913d-fa033c03696b

## Menjalankan Sistem Machine Learning
Langkah-langkah menjalankan sistem machine learning di lokal:
1. Pastikan semua environment, yaitu environment Anaconda dan Shell/Terminal sudah ada dan siap di jalankan
2. Clone Repositori: git clone https://github.com/hanafiiahmd/Edutech-Jaya-Jaya-Institut-Classification.git
cd Edutech-Jaya-Jaya-Institut-Classification
3. Aktifkan virtual environment:
   python -m venv venv
   venv\Scripts\activate
4. Install semua dependensi yang dibutuhkan:
   pip install -r requirements.txt
5. Pastikan file yang ada di repositori github tercantum file model, scaler, requirements, notebook dan app.py
6. Run: streamlit run app.py
7. Buka dan akses web: http://localhost:8501
8. Prototype machine learning berhasil dibuat

Langkah-langkah menjalankan sistem:
1. Akses streamlit app, lalu isi data sesuai data mahasiswa, seperti yang ada di tampilan app, seperti usia saat enrollment, jumlah kurikulum semester 1 diambil, dst...
2. Klik tombol prediksi
3. Hasil prediksi akan menampilkan: Siswa beresiko tinggi akan dropout / Siswa berpotensi akan graduate

Link streamlit app dapat diakses melalui link dibawah ini:
```
https://edutech-jaya-jaya-institut-classification-zyag2zmwr7nlxnbehkj5.streamlit.app/
```

## Conclusion
Kesimpulan dari proyek ini antara lain sebagai berikut:
1. Dari total 3630 siswa Jaya Jaya Institut, ada sebanyak 2209 siswa yang graduate dan 1421 siswa yang dropout, tingkat dropout rate mencapai 39,15%.
2. Dari 36 fitur yang ada, setelah dilakukan analisis didapat bahwa tingginya tingkat dropout di Jaya Jaya Institut di sebabkan oleh fitur-fitur berikut seperti admission grade, nilai previous qualification, jumlah mata kuliah yang di ambil pada semester 1 dan 2, jumlah mata kuliah yang disetujui semester 1 dan 2, nilai rata-rata semester 1 dan 2, jumlah mata kuliah yang lulus di semester 2 dan apakah pembayaran sudah dilakukan atau belum (tuition fees)
3. Untuk membantu tim Jaya Jaya Institut dalam memprediksi lebih awal kemungkinan siswa yang akan dropout, saya membuat model machine learning menggunakan model random forest dengan menggunakan 11 fitur yang mempengaruhi tingkat dropout/graduate siswa, dengan akurasi sebesar 89.80%.
4. Tingkat dropout menurut waktu kuliah terdapat pada waktu kuliah daytime mencapai 1214 siswa atau sekitar 85,43 % dari total siswa yang dropout di Jaya Jaya Institut
5. Mahasiswa International memiliki tingkat dropout yang sangat kecil dibandingkan yang bukan mahasiswa Internasional di Jaya Jaya Institut, dengan total hanya 32 siswa yang dropout.
6. Mahasiswa yang memiliki beasiswa juga tingkat dropoutnya sangat rendah dibandingkan siswa yang tidak memiliki beasiswa yaitu sebanyak 134 siswa dari total 1421 siswa yang dropout di Jaya Jaya Institut.

### Rekomendasi Action Items
Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.
- Memberikan bimbingan khusus untuk siswa yang mendapat nilai rata-rata yang rendah di semester 1, agar dapat memperbaiki nilai mereka serta memberikan kesempatan untuk memperbaiki nilai rata-rata kurikulum semester 2 untuk siswa yang mendapat nilai jelek, khususnya nilai 0.
- Memberikan persetujuan untuk mata kuliah yang diambil oleh siswa, sehingga siswa dapat menyelesaikan studi tepat waktu dan tidak terancam menambah semester yang mengakibatkan siswa terancam dropout. 
