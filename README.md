# Wadimar Playground 🎮

Koleksi game kecil yang bisa dimainkan langsung di browser. Buka `index.html` untuk menu awal, lalu pilih game.

| Game | Folder | Status |
| --- | --- | --- |
| Farmora | `games/farmora/` | Bisa dimainkan |

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
