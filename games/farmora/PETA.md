# Farmora — Rancangan Peta

Peta ini mengikuti gambar rancangan pemilik game, disesuaikan dengan koordinat yang sudah ada di kode.
Satu satuan sama dengan satu langkah di game, dan satu kotak di template sama dengan 10 satuan.
X bertambah ke timur. Z bertambah ke **selatan**, dan bagian atas peta adalah utara.
Template koordinatnya ada di `peta-template.png`.

## 1. Cara koordinat jadi gambar peta
- Dunia game memakai `x` (barat–timur) dan `z` (utara–selatan) dalam satuan langkah.
- Peta dunia (`worldMap()`) menggambar area x −172 sampai 158 dan z −112 sampai 104.
  - Rumusnya: `piksel = (koordinat − batas) × K`, dengan `K = lebar / 330`.
  - Lebarnya 300 px, atau 780 px saat diperbesar.
- Tanah, warna, dan bukit di peta diambil dari mesh tanah yang sama dengan dunia 3D (`TERR`), jadi peta dan game selalu cocok.

## 2. Wilayah (tidak berubah)
| Wilayah | x | z |
|---|---|---|
| Farm | −24 … 24 | −23 … 23 |
| Kota Sentosa | −50 … 50 | −106 … −27 |
| Desa Hutan | −88 … −27 | −72 … 72 |
| Desa Pegunungan | −168 … −88 | −72 … 72 |
| Lembah Persawahan | −50 … 50 | 27 … 100 |
| Desa Pantai | 27 … 101 | −64 … 64 |
| Pulau Kencana | 117 … 145 | 60 … 96 |

Di antara wilayah ada daratan tambahan berbentuk elips (`BLOBS`), supaya garis pantainya melengkung.

## 3. Sungai (`RIVERS`)
- **Sungai besar**:
  - (−104, −66) → (−91, −54) → (−88, −30) → (−88, 8) → (−82, 26) → (−60, 30) → (−36, 31) → (0, 32) → (30, 33) → (58, 40) → (86, 48) → (110, 55), lalu ke laut timur.
  - Lebarnya 3 sampai 5.
- **Cabang barat sawah**:
  - (−34.6, 32.6) → (−32.3, 46) → (−32.6, 76) → (−33.4, 106), lalu ke laut selatan.
- Muka air selalu turun mengikuti tanah. Sungai tidak bisa dilewati; pemain harus lewat jembatan.

## 4. Jembatan (otomatis di setiap jalur yang menyeberang sungai)
| Di mana | Kira-kira | Menghubungkan |
|---|---|---|
| Gerbang selatan farm | (0.5, 31.8) | Farm ↔ Lembah Persawahan |
| Barat Desa Hutan | (−87.5, −4.6) | Desa Hutan ↔ Desa Pegunungan |
| Selatan Desa Hutan | (−48, 30.6) | Desa Hutan ↔ Lembah Persawahan |
| Timur sawah | (32.6, 33.7) | Lembah Persawahan ↔ Desa Pantai |
| Dalam desa sawah | (−32.8, 54.3), (−32.8, 79.7) | rumah warga ↔ sawah barat |

## 5. Jalan (`ROAD_MAIN`, `roadKind()`)
- **Jalan utama** (batu, lebar 3):
  - Jalan lingkar farm.
  - Gerbang utara → Kota.
  - Gerbang selatan → alun-alun Lembah Persawahan.
  - Gerbang barat → Desa Hutan → Desa Pegunungan.
  - Gerbang timur → Desa Pantai → Pelabuhan.
- **Jalan desa** (tanah, lebar 1.9): semua cabang ke rumah, toko, dan tempat ibadah, ditambah penghubung antardesa:
  - Hutan ↔ Sawah
  - Hutan ↔ Kota
  - Kota ↔ Pantai
  - Sawah ↔ Pantai
- **Jalan kota** (aspal, lebar 3.8): kisi jalan Kota Sentosa.
- Setiap pintu bangunan punya jalan pendek ke jalannya. Rute harian warga mengikuti jalur yang sama.

## 6. Bangunan
- Semua bangunan dan fungsinya tetap.
- Yang digeser sedikit supaya tidak kena sungai:
  - Penggilingan Padi ke z 38.8.
  - Gerbang desa dan halte Lembah Persawahan ke selatan jembatan.
- Bagian gambar rancangan yang belum dibuat (bisa ditambahkan nanti):
  - Balai Kota
  - Kebun Sayur di gunung
  - Pura dan Rumah Adat di sawah
  - Laguna barat daya
  - Mercusuar di timur laut

## 7. Untuk dikembangkan
- `MAP_PINS.push({ x, z, icon, label })` menampilkan penanda misi atau acara di peta dunia.

## 8. Pemeriksaan tata letak (otomatis)
Setiap jalan diperiksa setiap setengah langkah: tidak boleh menyentuh bangunan, sawah, objek padat (pohon, pondok, papan, lampu, mobil), atau sungai (kecuali di jembatan), dan harus bisa dilewati pemain. Selain itu diperiksa juga:
- bangunan yang terlalu rapat, berada di sawah, sungai, atau laut;
- objek di dalam bangunan;
- simpul jalan yang terputus;
- tempat kegiatan warga;
- halte.

Hasil awal 65 temuan, sekarang **0**. Perbaikannya:
- **Lengkungan jalan desa otomatis menghindari rintangan.** Tiap jalan memakai lengkungan lamanya selama tidak menabrak. Kalau menabrak, dipilih lengkungan terdekat yang bersih dari bangunan, sawah, blok gedung kota, beringin alun-alun, pos ronda, taman bermain, dan sarang lebah.
- **Simpul jalan tidak menempel ke bangunan.** Simpul yang terlalu dekat digeser keluar sedikit.
- **Jalan kota:** jalan samping barat pindah ke x −30.6 dan timur ke x 35.5, sehingga tidak lagi menembus Rumah Sakit, Sekolah, Terminal, dan Vihara.
- **Rute yang dulu menembus bangunan diputar:**
  - Desa Pegunungan: lewat samping Warung Kopi; Kebun Kopi lewat Rumah Peternakan.
  - Desa Pantai: lewat samping Galangan menuju Pelabuhan; Rumah Pak Somad lewat Warung Seafood.
  - Desa Hutan: rumah Pak Markus dicapai lewat samping Pusat Kerajinan.
  - Pulau Kencana: lewat samping Penginapan dan Toko Suvenir.
- **Lembah Persawahan:**
  - Jalan masuk dari jembatan selatan farm lurus melewati gerbang desa.
  - Alun-alun bergeser sedikit dari pohon beringin.
  - Sawah barat mundur sedikit, sehingga ada jalan di antara sawah dan cabang sungai menuju jembatan Hutan.
- **Objek kecil:**
  - Gapura selalu berdiri melintang di jalannya.
  - Papan penunjuk berdiri di sisi jalan yang kosong.
  - Sarang lebah, tiang bendera sekolah, satu mobil parkir, dan perahu galangan dipindah agar tidak menghalangi.
  - Tempat Kadek berdiri dipindah ke pasir.
