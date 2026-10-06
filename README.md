# Wadimar Playground 🎮

Koleksi game kecil yang bisa dimainkan langsung di browser. Buka `index.html` untuk menu awal, lalu pilih game.

| Game | Folder | Status |
| --- | --- | --- |
| Farmora | `games/farmora/` | Bisa dimainkan |
| Ladago | `games/ladago/` | Bisa dimainkan |
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

## Karakter, simpan, dan main berdua
- **Pilih petani** sebelum main: nama, laki-laki atau perempuan, dan warna baju.
- **Progres tersimpan otomatis** setiap 20 detik, saat tidur, dan saat berjualan. Tombol 💾 menyimpan saat itu juga. Layar awal menawarkan **Lanjutkan Hari X** atau **Farm baru**.
- **Main berdua online:** satu orang memilih *Buat farm online* dan mendapat kode 4 huruf, temannya memilih *Gabung*. Kalian bermain bersama di farm milik pembuat: hewan, waktu, inventori, dan uang dipakai bersama. Aksi teman (mengelus, memerah, menjual) tampil di kedua layar, dan saat salah satu tidur, hari berganti untuk berdua. Progres disimpan di perangkat pembuat farm.
  - Di link claude.ai: memakai fitur ruangan real-time milik artifact. Keduanya harus login, dan link harus sudah dibagikan ke teman.
  - Di versi web (GitHub Pages): memakai PeerJS (WebRTC). Ketuk badge kode untuk menyalin link undangan.

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

# Ladago 💞

Ular tangga 3D kooperatif untuk pasangan: papan klasik 10×10 berisi 100 kotak di atas pulau yang ceria, tentang perjalanan hubungan dari kenalan sampai masa depan. Kamera otomatis zoom mengikuti pion saat bergerak, dan bisa diganti ke tampilan seluruh papan. Satu pion dipakai bersama, dan pemain melempar dadu bergantian. Setiap kotak membuka kartu yang dijawab secara rahasia lalu dibuka bersamaan.

- **5 chapter × 20 kotak:** Pertemuan Pertama ☕, Makin Dekat 🌳, Ujian Hubungan 🌧️, Membangun Bersama 🏠, dan Masa Depan Kita ✈️. Kotak 🌼 adalah kotak santai tanpa kartu, supaya permainan tetap mengalir.
- **Jenis kartu:** Love, Fun, Deep Talk, Guess Me, Future, Relationship Event, Our Decision (sepakati keputusan bersama kalau pilihan berbeda), Cerita Yuk, dan Future Letter (surat yang disimpan).
- 🪜 **8 tangga:** samakan jawaban untuk naik. 🐍 **8 ular:** kalau jawaban berbeda, kalian turun.
- **Akhir permainan:** skor Connection, Communication, Trust, Compatibility, dan Future Alignment, ditambah profil pasangan seperti *The Dream Builders*.
- **Cerita Kita:** riwayat perjalanan dan surat masa depan, tersimpan di browser.

## Cara main
- **Berdua di 1 HP:** jalan di mana saja. Jawaban rahasia diisi bergiliran, dengan layar "jangan intip".
- **Online berdua:** satu orang membuat ruangan, pasangannya bergabung dengan kode 4 huruf.
  - Di link claude.ai: memakai fitur ruangan real-time milik artifact. Kedua pemain harus login, dan link harus sudah dibagikan ke pasangan.
  - Di versi web (GitHub Pages): memakai PeerJS (WebRTC). Ada tombol untuk menyalin link undangan.

---

# Fotoin 📸

Photobooth online di browser.

1. **Pilih bentuk:** Strip 4 (klasik), Strip 3, Kotak 2×2, atau Polaroid. Atur juga hitung mundur (3/5/10 detik) dan jeda antarfoto.
2. **Masuk booth:** kamera menghitung mundur, ada kilatan flash dan bunyi rana, lalu foto diambil otomatis sampai semua kotak terisi. Ketuk foto kecil untuk mengambil ulang satu foto. Filter bisa dilihat langsung di kamera.
3. **Hias:** warna bingkai (termasuk warna bebas), motif (polkadot, garis, kotak-kotak, hati), 7 filter, 24 stiker emoji yang bisa digeser, diperbesar, dan diputar, tulisan dengan 3 gaya huruf, tanggal, dan logo.
4. **Simpan:** unduh PNG resolusi tinggi, bagikan lewat menu share HP (kalau didukung), atau simpan ke galeri di perangkat.

Tanpa kamera, misalnya saat dibuka lewat link claude.ai yang tidak mengizinkan kamera, setiap kotak bisa diisi dengan unggah foto. Di HP, cara ini langsung membuka kamera bawaan.

## Foto berdua online
Pilih **Mode → Berdua online 💞**. Satu orang menekan **Buat ruang foto** lalu mengirim kode 4 huruf atau link undangan. Pasangannya menekan **Gabung**. Setelah itu:
- kalian saling melihat lewat video, dan bisa saling mendengar kalau mikrofon diizinkan;
- pembuat ruang memilih bentuk strip, lalu kalian berdua masuk booth bersama;
- siapa pun boleh menekan jepret, dan hitung mundurnya berjalan serempak di kedua HP;
- setiap foto berisi kalian berdua berdampingan: pembuat ruang di kiri, pasangan di kanan;
- masing-masing bisa menghias dan mengunduh stripnya sendiri.

Koneksinya memakai WebRTC melalui [PeerJS](https://peerjs.com/): server perantara gratis, dan video mengalir langsung antar perangkat. Di sebagian jaringan seluler atau kantor yang ketat, koneksi langsung bisa gagal. Mengatasinya butuh server TURN, yang belum dipasang.

**Penting:** kamera dan mode berdua tidak jalan di link artifact claude.ai, karena link itu memblokir kamera dan WebRTC. Pakai versi web, misalnya GitHub Pages:
1. Buka **Settings → Pages** di repo ini.
2. Di **Source**, pilih *Deploy from a branch*, branch `claude/cloud-ldok5v` (atau `main` setelah digabung), folder `/ (root)`, lalu **Save**.
3. Setelah 1–2 menit, Fotoin bisa dibuka di https://wawannug.github.io/testing/games/fotoin/

