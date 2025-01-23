# Rekomendasi Rute

Proyek yang dibuat untuk menjawab salah satu permasalahan optimasi rute distribusi, yaitu membuat dan memetakan rute rekomendasi untuk distributor.
- Tujuan: Membuat rekomendasi rute sebenarnya di lapangan yang digambarkan ke dalam peta dengan mempertimbangkan profil kendaraan, preferensi rute, radius pencarian rute, dan fitur-fitur lainnya
- Menggunakan Open-source tools, yaitu
1. OR-TOOLS by Google untuk memperoleh titik kunjungan optimal berdasarkan kapasitas kendaraan, jumlah kendaraan, jarak antar titik, hingga jumlah permintaan antar titik
2. Open Route Service, memperoleh rute sebenarnya di peta menggunakan geojson untuk memperoleh geometri titik lokasi latitude dan longitude dan dapat di gambarkan secara langsung ke dalam peta

## Quickstart

Step by step untuk menjalankan app atau API yang menjadi output dari proyek yang dikerjakan.

- Versi Python: **3.11.10**

```
pip install -r requirements.txt
```
File Code untuk menjalankan skrip perhitungan
- preprocessing.ipynb, berguna untuk menggabungkan berbagai data dan melakukan perhitungan untuk memperoleh kolom yang diperlukan. Dalam proyek ini, data yang digabungkan adalah data desa Jawa Tengah, data alokasi pupuk yang diperoleh dari alokasai per kabupaten/kota dibagi dengan jumlah desa, dan data realisasi penjualan yang berasal dari Goods Issue Januari hingga Oktober 2024.
- generate.ipynb, berguna untuk memperoleh jumlah optimal *clustering* data menggunakan algoritma K-Means, dimana variabel yang dihitung adalah nilai latitude dan longitude ditambah alokasi per bulan yang menjadi bobot
- ORS_TOOLS_ALL_DATA, berguna untuk memperoleh rekomendasi titik kunjungan melalui OR-TOOLS per kendaraan dan penggambaran rute titik kunjungan tersebut ke dalam peta untuk memperoleh jarak sebenarnya di lapangan menggunakan data jalan yang diperoleh dari Open Route Service

**Catatan**: Kode harus mengikuti template penamaan kolom excel yang dipakai masing-masing file kode supaya kode dapat berjalan dengan lancar
- preprocessing.ipynb (desa_8264.xlsx + alokasi_jawa_tengah.xlsx + GI_Jateng_Jan_Okt_2024.xlsx = desa_aws_8264.csv)
- generate_cluster.ipynb (desa_aws_8264.csv -> desa_{dc} + distance_list_{dc}.json)
- ORS_TOOLS_ALL_DATA (desa_{dc} + distance_list_{dc}.json)
