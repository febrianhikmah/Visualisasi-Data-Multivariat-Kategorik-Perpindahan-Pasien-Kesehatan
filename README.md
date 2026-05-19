# Visualisasi Data Multivariat Kategorik: Perpindahan Pasien Kesehatan

Project ini menganalisis data perpindahan pasien kesehatan menggunakan visualisasi multivariat kategorik. Fokus utama analisis adalah memahami distribusi jumlah pasien, rata-rata lama rawat, status BPJS, jenis penyakit, serta pola perpindahan pasien antar kota.

## Dataset

Dataset yang digunakan:

- `data_perpindahan_pasien_kesehatan.xlsx`

Dataset berisi 100 baris observasi dan 12 kolom:

- `Tahun`
- `Jenis_Kelamin`
- `Usia_Kelompok`
- `Rumah_Sakit_Asal`
- `Rumah_Sakit_Tujuan`
- `Kota_Asal`
- `Kota_Tujuan`
- `Jenis_Penyakit`
- `Jenis_Perawatan`
- `Lama_Rawat_Hari`
- `BPJS_Status`
- `Jumlah_Pasien`

Kolom `Jumlah_Pasien` digunakan sebagai ukuran volume pasien. Karena satu baris dapat merepresentasikan lebih dari satu pasien, beberapa analisis menggunakan agregasi total pasien atau rata-rata lama rawat berbobot.

## Tujuan Analisis

Project ini bertujuan untuk:

- Menganalisis distribusi pasien berdasarkan jenis kelamin dan status BPJS.
- Membandingkan rata-rata lama rawat antar kelompok usia dan jenis kelamin.
- Mengidentifikasi segmen pasien berdasarkan volume pasien dan rata-rata lama rawat.
- Memvisualisasikan alur pasien dari jenis kelamin ke status BPJS dan jenis penyakit.
- Melihat pola perpindahan pasien antar kota.

## Visualisasi yang Digunakan

Notebook menggunakan beberapa jenis visualisasi:

- **Mosaic Plot** untuk melihat proporsi jumlah pasien berdasarkan jenis kelamin dan status BPJS.
- **Grouped Bar Chart** untuk membandingkan rata-rata lama rawat berbobot berdasarkan usia dan jenis kelamin.
- **Treemap** untuk menampilkan volume pasien dan rata-rata lama rawat pada segmen usia, gender, dan penyakit.
- **Sankey Diagram** untuk melihat alur jumlah pasien dari jenis kelamin ke status BPJS dan jenis penyakit.
- **Chord Diagram** untuk menggambarkan perpindahan pasien antar kota.

## Insight Utama

Beberapa insight dari analisis:

- Analisis jumlah pasien perlu menggunakan `Jumlah_Pasien`, bukan hanya menghitung jumlah baris.
- Distribusi pasien berdasarkan jenis kelamin dan status BPJS lebih tepat dibaca dari total jumlah pasien.
- Rata-rata lama rawat berbeda antar kelompok usia dan jenis kelamin, namun tidak selalu meningkat secara linear mengikuti usia.
- Segmen dengan volume pasien besar tidak selalu memiliki rata-rata lama rawat tertinggi.
- Pola perpindahan pasien antar kota menunjukkan beberapa rute dengan volume pasien lebih dominan dibanding rute lain.

## Struktur Project

```text
.
|-- data_perpindahan_pasien_kesehatan.xlsx
|-- Febrian_Tugas_Visualisasi_Data_Multivariate_Kategorik (1).ipynb
`-- README.md
```

## Cara Menjalankan Project

1. Buka notebook:

   `Febrian_Tugas_Visualisasi_Data_Multivariate_Kategorik (1).ipynb`

2. Pastikan file dataset berada di folder yang sama dengan notebook:

   `data_perpindahan_pasien_kesehatan.xlsx`

3. Jalankan semua cell dari atas ke bawah.

## Library yang Digunakan

Project ini menggunakan beberapa library Python:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly`
- `statsmodels`

## Catatan

Analisis ini bersifat deskriptif. Insight yang dihasilkan digunakan untuk membaca pola dalam dataset, bukan untuk menyimpulkan hubungan sebab-akibat.
