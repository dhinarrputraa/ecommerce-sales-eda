# E-Commerce User Interaction Analysis

## Deskripsi Proyek
Proyek ini berisi Exploratory Data Analysis (EDA) pada data interaksi pengguna di platform e-commerce (like, view, purchase). Tujuannya adalah memahami tren interaksi dari waktu ke waktu dan mengukur tingkat pembelian (purchase rate).

## Dataset
- **Sumber:** `E-commerece sales data 2024.csv` (nama file memuat "2024", tetapi tanggal pada data berkisar dari 28 Desember 2022 hingga 28 Desember 2023)
- **Data mentah:** 3.294 baris, 5 kolom
- **Data bersih:** 2.871 baris, 4 kolom

## Proses Analisis Data
- **Data Cleaning:** Menghapus 295 baris kosong, 1 kolom kosong (`Unnamed: 4`), dan 128 baris tanpa `Interaction type`. Mengubah `user id` ke integer dan `Time stamp` ke format datetime (format hari/bulan/tahun). Validasi akhir: tidak ada nilai kosong maupun duplikat.
- **Eksplorasi Data:** Menganalisis distribusi jenis interaksi (like 1.145, view 871, purchase 855).
- **Data Visualization:** Memetakan interaksi harian, interaksi bulanan, pembelian bulanan, dan tren per jenis interaksi.

## Teknologi yang Digunakan
- **Python**
- **Pandas** (manipulasi data)
- **Matplotlib** (visualisasi data)

## Insight Utama
- **Tingkat pembelian:** 29,8% dari seluruh interaksi berupa pembelian.
- **Puncak interaksi:** November 2023 adalah bulan tersibuk (565 interaksi). Kuartal 4 2023 (Oktober sampai Desember) menyumbang 51,5% dari seluruh interaksi (1.478 dari 2.871).
- **Sumber lonjakan:** Purchase rate tetap sekitar 30% (29,4% sampai 30,2%) pada tiga bulan tersibuk, sehingga lonjakan berasal dari kenaikan jumlah interaksi, bukan dari kenaikan konversi.
- **Catatan:** Januari 2023 juga tergolong ramai (415 interaksi), sehingga diperlukan data lebih dari satu tahun untuk memastikan apakah polanya musiman.

## Keterbatasan Data
Setiap `user id` dan `product id` hanya muncul satu kali, sehingga analisis per produk (produk terlaris) dan per pengguna (pengguna paling aktif) tidak dapat dilakukan. Analisis difokuskan pada jenis interaksi dan tren waktu.

## Struktur Repository
- `ecommerce_sales_analysis.ipynb` : notebook analisis
- `E-commerece sales data 2024.csv` : data mentah

## Cara Menjalankan
1. Instal library: `pip install pandas matplotlib`
2. Letakkan file CSV dan notebook di folder yang sama
3. Buka notebook di Jupyter atau Google Colab, lalu jalankan semua sel
