# 📍 GeoJSON Jalan Desa Kadumulya

Repositori ini berisi data jalan dalam format **GeoJSON (LineString)** dari wilayah **Desa Kadumulya**, Kecamatan Parongpong, Kabupaten Bandung Barat.

---

## 🎯 Tujuan

- Membuat data jalan (LineString) dari kampung masing-masing
- Validasi data melalui [geojson.io](https://geojson.io)
- Menyimpan data ke:
  - GitHub (repositori ini)
  - MongoDB (satu jalan satu record)

---

## 🗂️ Struktur Repo

geojson-repo/
├── data/
│ ├── jl-cihanjuang.geojson
│ ├── jl-bumi-hanjuang-4.geojson
│ ├── rt-02.geojson
│ ├── jl-cisintok-kadumulya.geojson
│ ├── gg-mushola-koi.geojson
│ └── gg-bu-pri.geojson
└── README.md

yaml
Copy code

---

## ✅ Validasi di geojson.io

Semua file telah divalidasi melalui [geojson.io](https://geojson.io):

- ✅ Tidak ada error sintaks
- ✅ Tipe geometri `LineString` dikenali
- ✅ Koordinat ditampilkan sesuai lokasi asli
- ✅ Properti `name` terbaca dengan baik

---

## 💾 Penyimpanan MongoDB

Data juga disimpan ke **MongoDB** dengan skema:

- Satu record per jalan
- Format mengikuti struktur `Feature` GeoJSON

Contoh:

```json
{
  "_id": ObjectId("..."),
  "type": "Feature",
  "properties": {
    "name": "Jl. Cihanjuang"
  },
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [107.56875311776862, -6.853554416027253],
      [107.5691550520118, -6.851697347235059]
    ]
  }
}
🛣️ Daftar Jalan (6 Jalan = 30 Poin)
No	Nama Jalan	Poin
1	Jl. Cihanjuang	5
2	Jl. Bumi Hanjuang 4	5
3	Rt. 02	5
4	Jl. Cisintok Kadumulya	5
5	Gg. Mushola Koi	5
6	Gg. Bu Pri	5
Total	30

🧾 Status Pengerjaan
Komponen	Status
Pembuatan GeoJSON jalan (maks. 30 poin)	✅
Validasi di geojson.io (30 poin)	✅
Upload ke GitHub & penjelasan (30 poin)	✅
Simpan ke MongoDB (maks. 10 poin)	✅

📌 Catatan
Semua file disusun dengan format Feature atau FeatureCollection

Penamaan file menggunakan kebab-case sesuai nama jalan

Data bersifat representatif dan tidak menggambarkan peta resmi

🙋‍♂️ Author
Nama: hadzikk
Email: hadzikmochammad@gmail.com
Wilayah: Desa Kadumulya, Parongpong, Kab. Bandung Barat
