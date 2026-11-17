# Peta Fasilitas Publik Kota Medan

Proyek Tahap 1 — Pengembangan SIG Web (Sub-CPMK 7: Implementasi SIG Web dengan Leaflet)

- **Nama / NIM:** Fathul Khair / 241712073
- **Mata kuliah:** Pengembangan SIG Web
- **Dosen:** Dr. Syahriol Sitorus, M.IT
- **Live demo:** https://khair222.github.io/sigweb-fasilitas-medan/

## 1. Tema dan tujuan

Peta web interaktif yang menampilkan sebaran fasilitas publik di Kota Medan (kesehatan, pendidikan, ruang terbuka, dan transportasi).

**Masalah spasial:** warga dan perencana kota sulit mengetahui letak dan jarak fasilitas dasar secara cepat. Peta ini menyajikan informasinya dalam satu halaman yang dapat dibuka di ponsel maupun komputer.

## 2. Kaitan dengan SDG

| SDG | Kontribusi |
|---|---|
| **SDG 11** — Kota & Permukiman Berkelanjutan | Akses warga ke layanan dasar (target 11.2) dan ruang publik terbuka (target 11.7). Fitur "Lokasi Saya" menunjukkan fasilitas terdekat. |
| **SDG 9** — Industri, Inovasi & Infrastruktur | Memakai teknologi terbuka (Leaflet, OpenStreetMap) yang murah, ringan, dan dapat direplikasi pemerintah daerah. Memuat simpul transportasi (stasiun, terminal, bandara). |

## 3. Fitur

- **Basemap & tile layer:** OpenStreetMap, CARTO Terang, dan citra satelit Esri.
- **Marker & popup:** 14 fasilitas, tiap penanda berisi nama, kategori, keterangan, dan koordinat.
- **Layer control:** menyalakan/mematikan 4 layer tematik dan berganti basemap.
- **Data spasial terikat:** data GeoJSON (titik dan satu poligon kawasan Lapangan Merdeka).
- **Pencarian & daftar fasilitas:** klik nama untuk terbang ke lokasi dan membuka popup.
- **Event & geolocation:** `map.on('click')` dan `map.locate()`; menampilkan fasilitas terdekat dari posisi pengguna.
- **Alat ukur jarak:** memakai rumus Haversine.
- **Tambah titik:** pengguna dapat menandai titik baru dan melihat koordinatnya.
- **Legenda, skala, dan atribusi** sumber data.
- **Responsif & aksesibel:** layout menyesuaikan layar 375 px, kontras warna memadai, tombol dapat diakses keyboard, serta label ARIA.

## 4. Struktur berkas

```
proyek-sigweb/
├── index.html   # seluruh kode (HTML, CSS, JavaScript, data GeoJSON)
└── README.md
```

## 5. Cara menjalankan

1. Unduh atau *clone* repositori ini.
2. Buka `index.html` di browser (butuh koneksi internet untuk memuat Leaflet dan tile peta).

## 6. Publikasi dengan GitHub Pages

1. Buat repositori baru di GitHub (publik), misalnya `sigweb-fasilitas-medan`.
2. Unggah `index.html` dan `README.md` ke cabang `main`.
3. Buka **Settings → Pages**, pilih **Deploy from a branch**, cabang `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu 1–2 menit; alamat tampil di halaman yang sama. Salin ke bagian *Live demo* di atas.

## 7. Sumber data dan atribusi

- Koordinat fasilitas diambil secara perkiraan dari OpenStreetMap dan perlu diverifikasi di lapangan.
- Basemap: © OpenStreetMap contributors, © CARTO, © Esri.
- Library: [Leaflet 1.9.4](https://leafletjs.com) (lisensi BSD-2-Clause).

## 8. Pemetaan terhadap rubrik penilaian

| Kriteria | Bobot | Bukti pada proyek |
|---|---|---|
| Peta tampil & stabil | 20% | Basemap OSM termuat, pusat dan zoom awal ditentukan |
| Data spasial terikat | 25% | GeoJSON titik & poligon, popup informatif |
| Interaktivitas | 25% | Layer control, event klik, geolocation, ukur jarak |
| Desain & aksesibilitas | 15% | Responsif, legenda, atribusi, kontras |
| Dokumentasi & publikasi | 15% | README ini dan live demo GitHub Pages |

## 9. Pengembangan lanjutan

Memuat data dari file GeoJSON/API terpisah, clustering untuk data lebih banyak, analisis radius layanan (buffer), dan mode partisipatif untuk pelaporan warga.
