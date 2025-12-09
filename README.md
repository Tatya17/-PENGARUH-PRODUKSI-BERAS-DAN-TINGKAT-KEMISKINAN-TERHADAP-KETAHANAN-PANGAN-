# ANALISIS PENGARUH PRODUKSI BERAS DAN TINGKAT KEMISKINAN TERHADAP KETAHANAN PANGAN ANTAR PROVINSI DI INDONESIA TAHUN 2024

# DESKRIPSI SINGKAT PROJECT
Ketahanan pangan menjadi isu strategis di Indonesia karena beras merupakan makanan pokok lebih dari 95% penduduk. Meskipun Indonesia termasuk produsen beras besar, distribusi produksi antarprovinsi belum merata sehingga memunculkan kerentanan pangan di wilayah tertentu. Selain ketersediaan, tingkat kemiskinan juga berperan penting karena memengaruhi kemampuan masyarakat dalam mengakses pangan. Provinsi dengan kemiskinan lebih tinggi umumnya memiliki tingkat ketahanan pangan lebih rendah. Proyek ini menganalisis pengaruh produksi beras dan tingkat kemiskinan terhadap Indeks Ketahanan Pangan (IKP) menurut provinsi tahun 2024 sebagai dasar penyusunan rekomendasi peningkatan ketahanan pangan nasional berbasis data.

# TUJUAN
1. Mengetahui pengaruh produksi beras terhadap ketahanan pangan antar provinsi di Indonesia tahun 2024.
2. Mengetahui pengaruh tingkat kemiskinan terhadap ketahanan pangan antar provinsi di Indonesia tahun 2024.
3. Mengetahui pengaruh produksi beras dan tingkat kemiskinan secara simultan terhadap IKP 2024.

# PENJELASAN HASIL FINAL INTEGRASI
Dataset hasil integrasi merupakan gabungan dari tiga dataset berbeda:
1. Dataset Produksi Padi dan Beras Menurut Provinsi 2024,
2. Dataset Jumlah dan Persentase Penduduk Miskin Menurut Provinsi 2024, dan
3. Dataset Indeks Ketahanan Pangan (IKP).

Ketiga dataset tersebut telah melalui proses preprocessing (rename kolom, filter data IKP tahun 2024, seleksi kolom relevan, standarisasi format isi kolom provinsi, filtering provinsi valid/menyamakan jumlah baris, pengecekan missing value, duplikasi, cek tipe data, analisis outlier). Setelah itu dilakukan proses integrasi berdasarkan kolom provinsi sehingga menghasilkan satu tabel final yang berisi 5 variabel yang relevan untuk analisis:

<img width="839" height="631" alt="image" src="https://github.com/user-attachments/assets/5493abd9-03a1-4c8d-af51-1c4e87f8aae7" />
<img width="840" height="478" alt="image" src="https://github.com/user-attachments/assets/a764d51c-e39e-4242-a8f5-74051bf3dae0" />

Dibawah ini merupakan penjelasan mengenai 5 variabel yang ada pada hasil final project:
| Variabel | Satuan | Sumber Resmi | Catatan Penting |
|---------|--------|--------------|------------------|
| provinsi | - | Semua dataset (Kaggle – Produksi Beras, BPS – SUSENAS, Badan Pangan Nasional – IKP) | Provinsi diseragamkan penulisannya (lowercase) agar integrasi data berhasil. Total 34 provinsi. | 
| produksi_beras (ton) | Ton | Kaggle – Produksi Padi & Beras Menurut Provinsi 2019–2024 (https://www.kaggle.com/datasets/daniakhmadmaulana/produksi-padi-dan-beras-menurut-provinsi-2019-2024) | Produksi beras diperoleh dari hasil konversi produksi padi menjadi beras dengan menggunakan angka konversi gabah ke beras dan mempertimbangkan proporsi gabah/beras yang susut/tercecer dan untuk penggunaan nonpangan. | 
| jumlah_miskin_maret (ribu) | Ribu jiwa | BPS – Jumlah & Persentase Penduduk Miskin Menurut Provinsi (SUSENAS Maret 2024) https://www.bps.go.id/en/statistics-table/3/UkVkWGJVZFNWakl6VWxKVFQwWjVWeTlSZDNabVFUMDkjMyMwMDAw/jumlah-dan-persentase-penduduk-miskin-menurut-provinsi.html?year=2024 | Menggambarkan **jumlah penduduk miskin pada bulan Maret 2024**. Data diperoleh dari **SUSENAS Maret**. SUSENAS Maret dibangun dari sampel baru, hasil survei Maret yang hanya menggambarkan kondisi kemiskinan bulan tersebut. Pendataan lapangan dilakukan **19 Februari – 9 Maret 2024** di seluruh Indonesia. | 
| persen_miskin_maret (%) | Persen (%) | BPS – Jumlah & Persentase Penduduk Miskin Menurut Provinsi (SUSENAS Maret 2024) https://www.bps.go.id/en/statistics-table/3/UkVkWGJVZFNWakl6VWxKVFQwWjVWeTlSZDNabVFUMDkjMyMwMDAw/jumlah-dan-persentase-penduduk-miskin-menurut-provinsi.html?year=2024 | Menggambarkan **persentase penduduk miskin pada bulan Maret 2024**. Data diperoleh dari **SUSENAS Maret**. SUSENAS Maret dibangun dari sampel baru, hasil survei Maret yang hanya menggambarkan kondisi kemiskinan bulan tersebut. Pendataan lapangan dilakukan **19 Februari – 9 Maret 2024** di seluruh Indonesia. | 
| ikp | Skor indeks (0–100) | Badan Pangan Nasional – IKP Provinsi 2024 (https://data.badanpangan.go.id/datasetpublications/2dd/ikp-prov-2024) | IKP adalah indeks komposit yang menggambarkan level ketahanan pangan provinsi. Semakin tinggi skor, semakin kuat ketahanan pangannya. Digunakan sebagai variabel dependen dalam analisis. |

Project ini dikerjakan untuk memenuhi UAS mata kuliah Data Wrangling  
Program Studi Sains Data – Universitas Negeri Surabaya  
Kelompok 18
