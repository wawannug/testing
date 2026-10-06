# Wadimar Playground 🎮

Koleksi game kecil yang bisa dimainkan langsung di browser. Buka `index.html` untuk menu awal, lalu pilih game.

| Game | Folder | Status |
| --- | --- | --- |
| Farmora | `games/farmora/` | Bisa dimainkan |
| LADAGO | `games/ladago/` | Bisa dimainkan |
| Fotoin | `games/fotoin/` | Bisa dipakai |

Untuk menambah game baru, buat folder `games/<nama-game>/index.html`, lalu tambahkan kartunya di `index.html`. Sediakan juga tautan kembali ke `../../index.html`.

---

# Farmora 🌾

Game peternakan mungil 3D bergaya lembut dan membulat, terinspirasi dari Stardew Valley, Coral Island, dan Story of Seasons. Dibuat dengan [Three.js](https://threejs.org/) dalam satu file `games/farmora/index.html`, tanpa proses build.

## Isi peternakan
- 🏠 Rumah, kotak pengiriman, ladang sayur, kolam, dan orang-orangan sawah
- Sepasang hewan jantan ♂ dan betina ♀ untuk setiap jenis ternak, masing-masing dengan kandang sendiri (kandang ayam, lumbung sapi, kandang kambing, kandang domba):
  - 🐔 Ayam: Jago (jantan) dan Kiki (betina),
  - 🐄 Sapi: Bento (jantan) dan Mimi (betina)
  - 🐐 Kambing: Gogo (jantan) dan Bimbi (betina)
  - 🐑 Domba: Wolly (jantan) dan Kapas (betina)
- 🐱 🐶 Hewan peliharaan: Oyen si kucing oren dan Bruno si anjing yang suka mengikutimu

## Cara main
| Kontrol | Aksi |
| --- | --- |
| WASD / panah | Berjalan (tahan Shift untuk lari) |
| E / Spasi | Elus hewan, ambil hasil ternak, jual, tidur |
| Scroll | Zoom kamera |
| H | Bantuan |

Di HP muncul joystick dan tombol aksi ✋.

- Elus hewan setiap hari agar hatinya (♥) bertambah. Hewan ternak yang tidak dielus seharian akan sedikit sedih.
- Setiap pagi ayam, sapi, dan kambing betina menghasilkan telur atau susu, dan kedua domba menghasilkan wol. Hewan jantan tetap bisa dielus. Ikon di atas kepala menandakan hasilnya sudah siap.
- Jual hasil ternak di kotak pengiriman 📦 di dekat rumah.
- Masuk ke pintu rumah untuk tidur. Kalau masih di luar sampai pukul 02:00, kamu akan pingsan.
- Progres tersimpan otomatis di browser.

## Menjalankan
Buka `index.html` di browser (perlu internet untuk memuat Three.js dari CDN), atau jalankan server lokal:

```bash
npx http-server .
```

---

# LADAGO 💞

Ular tangga 3D kooperatif untuk pasangan: papan klasik 10×10 berisi 100 kotak di atas pulau yang ceria, tentang perjalanan hubungan dari kenalan sampai masa depan. Kamera otomatis zoom mengikuti pion saat bergerak, dan bisa diganti ke tampilan seluruh papan. Satu pion dipakai bersama, dan pemain melempar dadu bergantian. Setiap kotak membuka kartu yang dijawab secara rahasia lalu dibuka bersamaan.

- **5 chapter × 20 kotak:** Pertemuan Pertama ☕, Makin Dekat 🌳, Ujian Hubungan 🌧️, Membangun Bersama 🏠, dan Masa Depan Kita ✈️. Kotak 🌼 adalah kotak santai tanpa kartu, supaya permainan tetap mengalir.
- **Jenis kartu:** Love, Fun, Deep Talk, Guess Me, Future, Relationship Event, Our Decision (sepakati keputusan bersama kalau pilihan berbeda), Cerita Yuk, dan Future Letter (surat yang disimpan).
- 🪜 **8 tangga:** samakan jawaban untuk naik. 🐍 **8 ular:** kalau jawaban berbeda, kalian turun.
- **Akhir permainan:** skor Connection, Communication, Trust, Compatibility, dan Future Alignment, ditambah profil pasangan seperti *The Dream Builders*.
- **Cerita Kita:** riwayat perjalanan dan surat masa depan, tersimpan di browser.

## Cara main
- **Berdua di 1 HP:** jalan di mana saja. Jawaban rahasia diisi bergiliran, dengan layar "jangan intip".
- **Online berdua:** memakai fitur ruangan real-time milik artifact claude.ai. Satu orang membuat ruangan, pasangannya bergabung dengan kode 4 huruf. Hanya bisa dipakai saat dibuka lewat link claude.ai: kedua pemain harus login, dan link harus sudah dibagikan ke pasangan. Di GitHub Pages, mode ini nonaktif.

---

# Fotoin 📸

Photobooth online di browser.

1. **Pilih bentuk:** Strip 4 (klasik), Strip 3, Kotak 2×2, atau Polaroid. Atur juga hitung mundur (3/5/10 detik) dan jeda antarfoto.
2. **Masuk booth:** kamera menghitung mundur, ada kilatan flash dan bunyi rana, lalu foto diambil otomatis sampai semua kotak terisi. Ketuk foto kecil untuk mengambil ulang satu foto. Filter bisa dilihat langsung di kamera.
3. **Hias:** warna bingkai (termasuk warna bebas), motif (polkadot, garis, kotak-kotak, hati), 7 filter, 24 stiker emoji yang bisa digeser, diperbesar, dan diputar, tulisan dengan 3 gaya huruf, tanggal, dan logo.
4. **Simpan:** unduh PNG resolusi tinggi, bagikan lewat menu share HP (kalau didukung), atau simpan ke galeri di perangkat.

Tanpa kamera, misalnya saat dibuka lewat link claude.ai yang tidak mengizinkan kamera, setiap kotak bisa diisi dengan unggah foto. Di HP, cara ini langsung membuka kamera bawaan.

