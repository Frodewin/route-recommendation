# Rekomendasi Rute

Buat summary dari proyek yang telah dikerjakan, sebaiknya memuat beberapa poin berikut.
Proyek yang dibuat untuk menjawab salah satu permasalahan optimasi rute distribusi, yaitu membuat dan memetakan rute rekomendasi untuk distributor.
- Tujuan: Membuat rekomendasi rute sebenarnya di lapangan yang digambarkan ke dalam peta dengan mempertimbangkan profil kendaraan, preferensi rute, radius pencarian rute, dan fitur-fitur lainnya
- Menggunakan Open-source tools, yaitu
1. OR-TOOLS by Google untuk memperoleh titik kunjungan optimal berdasarkan kapasitas kendaraan, jumlah kendaraan, jarak antar titik, hingga jumlah permintaan antar titik
2. Open Route Service, memperoleh rute sebenarnya di peta menggunakan geojson untuk memperoleh geometri titik lokasi latitude dan longitude dan dapat di gambarkan secara langsung ke dalam peta
3. 
## Quickstart

Step by step untuk menjalankan app atau API yang menjadi output dari proyek yang dikerjakan.

- Versi Python: **3.11.10**

```
pip install -r requirements.txt

```
