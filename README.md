# Kebun Kecil 🌾

Game peternakan mungil 3D low-poly yang bisa dimainkan langsung di browser, terinspirasi dari Stardew Valley, Coral Island, dan Story of Seasons. Dibuat dengan [Three.js](https://threejs.org/) dalam satu file `index.html`, tanpa proses build.

## Isi peternakan
- 🏠 Rumah, kotak pengiriman, ladang sayur, kolam, dan orang-orangan sawah
- 🐔 Kandang ayam: Kiki, Popo, dan Ciko
- 🐄 🐐 🐑 Lumbung dan padang: sapi (Mimi, Moli), kambing (Gogo, Bimbi), domba (Wolly, Kapas)
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
- Setiap pagi hewan ternak menghasilkan telur, susu sapi, susu kambing, atau wol. Ikon di atas kepala menandakan hasilnya sudah siap.
- Jual hasil ternak di kotak pengiriman 📦 di dekat rumah.
- Masuk ke pintu rumah untuk tidur. Kalau masih di luar sampai pukul 02:00, kamu akan pingsan.
- Progres tersimpan otomatis di browser.

## Menjalankan
Buka `index.html` di browser (perlu internet untuk memuat Three.js dari CDN), atau jalankan server lokal:

```bash
npx http-server .
```
