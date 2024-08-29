# Capstone Project Modul 2: Analisis Data Listing Airbnb di Bangkok

## Gambaran Umum

Proyek ini merupakan bagian dari Proyek Akhir untuk Modul 2 dalam kursus Analisis Data. Fokus dari proyek ini adalah untuk menganalisis listing Airbnb di Bangkok guna menemukan wawasan terkait berbagai faktor seperti ketersediaan kamar, harga, dan pola ulasan.

## Dataset

Dataset yang digunakan untuk proyek ini adalah `Airbnb_Listings_Bangkok`, yang berisi informasi detail tentang berbagai listing Airbnb di Bangkok. Dataset ini mencakup kolom-kolom berikut:
- `id` : Identitas unik dari Airbnb
- `name` : nama properti
- `host_id` : id pemilik
- `host_name` : nama pemilik
- `neighbourhood`: Nama lingkungan tempat listing berada.
- `room_type`: Jenis kamar yang tersedia (misalnya, Entire home/apt, Private room, Shared room, Hotel room).
- `price`: Harga per malam untuk listing tersebut.
- `minimum_nights`: Jumlah malam minimum yang diperlukan untuk memesan listing.
- `number_of_reviews`: Total jumlah ulasan yang diterima listing.
- `availability_365`: Jumlah hari ketersediaan listing dalam satu tahun.
- `calculated_host_listings_count`: Jumlah properti yang dikelola oleh host.
- `number_of_reviews_ltm`: Jumlah ulasan yang diterima dalam 30 hari terakhir.

## Tujuan

Tujuan dari proyek ini adalah untuk mengeksplorasi dan menganalisis data listing Airbnb untuk menjawab beberapa pertanyaan utama berikut:

1. **Bagaimana pengaruh penetuan loaksi dengan ketersediaan kamar?**
2. **Bagaimana pengaruh jenis kamar, jumlah ulasan dan ketersediaan?**
3. **Apakah ada perbedaan signifikan dalam jumlah ulasan di berbagai lingkungan (neighbourhood)?**
4. **Apa saja faktor utama yang memengaruhi ketersedian kamar?**

## Metodologi

### 1. Pembersihan Data
- **Penanganan Nilai Kosong:** Imputasi dan penghapusan data yang hilang jika diperlukan.
- **Deteksi dan Penanganan Outliers:** Mengidentifikasi dan menangani outliers, terutama pada kolom `price` dan `number_of_reviews`.
- **Feature Engineering:** Membuat fitur baru seperti `price_per_night` dengan membagi `price` dengan `minimum_nights`.

### 2. Analisis Data Eksploratif (EDA)
- **Statistik Deskriptif:** Merangkum data menggunakan ukuran seperti mean, median, mode, dan standar deviasi.
- **Visualisasi:** Menggunakan diagram batang, box plot, dan matriks korelasi untuk mengeksplorasi hubungan antar variabel.
- **Analisis Crosstab:** Menganalisis distribusi jenis kamar,ketersedian kamar, jumlah ulasan  di berbagai lingkungan.

### 3. Statistik Inferensial
- **Uji Chi-Square:** Untuk menganalisis hubungan antara `neighbourhood` dan `room_type`.
- **Uji Kruskal-Wallis:** Untuk membandingkan `number_of_reviews` dan `availability_365` di berbagai `room_type`.
- **Analisis Korelasi:** Untuk memeriksa kekuatan hubungan antara `price` dan `calculated_host_listings_count`.

### 4. Pengujian Hipotesis
- **Hipotesis Nol (H0):** Tidak ada perbedaan signifikan dalam ketersediaan kamar di berbagai lingkungan.
- **Hipotesis Alternatif (H1):** Ada perbedaan signifikan dalam ketersediaan kamar di berbagai lingkungan.

### 5. Kesimpulan dan Rekomendasi
- **Interpretasi Hasil:** Menarik wawasan dari hasil analisis dan pengujian.
- **Rekomendasi:** Memberikan saran yang dapat ditindaklanjuti berdasarkan temuan, seperti pemilihan lokasi,strategi penetapan harga atau penawaran jenis kamar.

