<p align="center">
  <H3 align="center">Analisis Sentimen Ulasan Aplikasi Tokopedia Menggunakan IndoBERT</H3>
</p>

<p align="center">
  <strong>Faris Iftikhar Alfarisi</strong>
</p>
<p align="center">
  <i>faris.10122050@mahasiswa.unikom.ac.id</i> <br> <i>faris.workingspace@gmail.com</i> <br><i>@frs.alfrs_</i>
</p>


## Deskripsi Proyek
Proyek ini bertujuan untuk memahami persepsi pengguna terhadap aplikasi **Tokopedia** melalui analisis sentimen ulasan mereka menggunakan teknologi **Natural Language Processing (NLP)** dan model **IndoBERT**.  
Pendekatan ini diharapkan dapat mengungkap insight berharga tentang pengalaman pengguna yang dapat membantu Tokopedia meningkatkan layanannya.


## Alur Analisis
1. **Pengumpulan Data**
   - Mengambil ulasan pengguna Tokopedia dari Google Play menggunakan **Google Play Scraper**.

2. **Pra-Pemrosesan Data**
   - Pembersihan data dari karakter tidak relevan.
   - Konversi teks ke huruf kecil.
   - Normalisasi teks termasuk penanganan singkatan dan kata tidak baku.
   - Tokenisasi menggunakan **NLTK**.
   - Penghapusan stopwords dengan kombinasi **NLTK** dan daftar custom.
   - Stemming menggunakan **Sastrawi** untuk mengubah kata ke bentuk dasar.

3. **Analisis Sentimen**
   Menggunakan model **IndoBERT** (`indobenchmark/indobert-base-p1`) untuk mengklasifikasikan sentimen menjadi **Positif**, **Netral**, dan **Negatif**. dengan menambahkan integrasi skor rating pengguna untuk meningkatkan akurasi pelabelan yang memberikan bobot lebih pada tensor yang dihasilkan dri confidence_score.

4. **Visualisasi**
   <img width="1589" height="433" alt="image" src="https://github.com/user-attachments/assets/02480cc0-3d17-4730-a010-864745c81004" />
   Visualisasi Wordcloud Sentimen Positif & Negatif

5. **Eksperimen Clustering**
   - Menggunakan **K-Means** dan **K-Medoids**.
   - Representasi numerik teks menggunakan **TF-IDF**.
   - Reduksi dimensi menggunakan **PCA** sebelum clustering.


## Temuan Utama
- Mayoritas pengguna memberikan **rating 5**, menunjukkan tingkat kepuasan tinggi.
- Terdapat ulasan bernilai **1**, menandakan area yang perlu perhatian.
- Model **IndoBERT** berhasil mengidentifikasi pola sentimen dengan baik.
- Ulasan dengan sentimen serupa membentuk **cluster yang terpisah**.
- Kata kunci negatif: `"pengiriman"`, `"voucher"` → area untuk perbaikan.
- Kata kunci positif: `"mudah"`, `"belanja"` → aspek aplikasi yang sudah baik.


## Kesimpulan
Proyek ini berhasil menyusun alur analisis sentimen yang komprehensif untuk memahami ribuan ulasan aplikasi Tokopedia. Hasilnya mengungkap cerita yang menarik - meskipun mayoritas pengguna menyampaikan kepuasan melalui ulasan positif, terdapat beberapa catatan penting yang layak diperhatikan, khususnya terkait proses pengiriman yang sering menjadi sorotan dan mekanisme penanganan keluhan yang masih perlu penyempurnaan.

Yang lebih menarik lagi, melalui eksperimen clustering, kami menemukan pola-pola tersembunyi dalam data ulasan yang membuka peluang baru untuk analisis lebih mendalam. Pendekatan ini tidak hanya membantu memahami sentimen secara umum, tetapi juga memungkinkan identifikasi kelompok-kelompok spesifik pengguna dengan karakteristik unik, yang bisa menjadi dasar untuk pengembangan fitur yang lebih tepat sasaran di masa depan.


## Teknologi yang Digunakan
- **Python**  
- **NLTK** (Tokenisasi, Stopwords)  
- **Sastrawi** (Stemming Bahasa Indonesia)  
- **IndoBERT** (Model NLP Bahasa Indonesia)  
- **TF-IDF** & **PCA** (Representasi dan reduksi dimensi)  
- **K-Means** & **K-Medoids** (Clustering)  
- **Word Cloud** (Visualisasi)
- **Google Play Scrapper**

---

## Catatan
Proyek ini dibuat untuk tugas mata kuliah **Pembelajaran Mesin**, Program Studi Teknik Informatika, **Universitas Komputer Indonesia**.

Faris Iftikhar Alfarisi
