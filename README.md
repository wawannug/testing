# Wadimar Playground 🎮

Koleksi game kecil yang bisa dimainkan langsung di browser. Buka `index.html` untuk menu awal, lalu pilih game.

**Masuk dengan nama:** sebelum menu dan setiap game terbuka, pemain harus mengetik nama yang terdaftar (2 akun). Nama diingat selama sesi tab browser itu; tab baru akan bertanya lagi. Karena hanya 2 akun itu yang bisa main, game tidak lagi meminta nama: nama diambil dari akun yang masuk. Cerita Kita Ladago dan galeri Fotoin tersimpan per akun (kunci `…@nama` di localStorage), sedangkan Farmora memakai satu farm bersama untuk berdua. Catatan: ini gerbang sederhana di sisi browser, bukan pengamanan sungguhan, karena kodenya bisa dibaca siapa pun yang membuka sumber halaman.

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

## Kebun buah 🌳
Ada 20 tanaman buah khas Indonesia di **Kebun Barat**, **Kebun Utara**, dan bedengan ladang:
🍌 Pisang · 🍉 Semangka · 🍊 Jeruk · 🥭 Mangga · 🍎 Apel · 🍈 Melon · 🥑 Alpukat · 🍍 Nanas · 🥥 Kelapa · 🍈 Pepaya · 🍇 Anggur · 🍓 Stroberi · 🥭 Durian · 🥝 Salak · 🟣 Manggis · 🍐 Pir · 🍉 Jambu biji · 🟡 Rambutan · 🟠 Duku/Langsat · 🟤 Sawo.

- Setiap tanaman dibuat mirip aslinya: pohon berkanopi, palem kelapa yang condong, pisang dengan tandan dan jantungnya, pepaya, rumpun salak berduri, anggur di para-para, serta bedengan semangka, melon, stroberi, dan nanas.
- **Siram sekali sehari.** Ember berisi 10 siraman dan bisa diisi ulang di dua sumur 🪣. Tanaman yang disiram tumbuh setiap malam dan berbuah sesuai sifatnya, dari stroberi (setiap hari) sampai durian, manggis, duku, dan nanas (setiap 5 hari). Tanaman yang tidak disiram berhenti tumbuh, dan daunnya pelan-pelan menguning.
- Buah yang siap panen terlihat di tanaman, dan ikon 💧 menandai tanaman yang belum disiram. Hasil panen masuk tas dan bisa dijual di kotak pengiriman.

## Rumah 🏠
Pintu depan rumah sekarang membawa masuk ke dalam rumah (seperti di Stardew Valley atau Coral Island). Bagian dalam adalah scene tersendiri yang baru dibangun saat pertama kali masuk dan hanya digambar ketika kamu di dalam, jadi farm luar tidak digambar bersamaan dan memori tetap hemat.

- **Lantai 1:** 🚪 ruang tamu, 🛋️ ruang keluarga (sofa, TV, dan **komputer toko online** 🖥️), 🍳 dapur (masak 7 resep dari hasil kebun & ternak) dan 🍽️ ruang makan, 🚿 kamar mandi/WC, serta 🕌 **mushola** dengan 2 sajadah. Di mushola kamu ditanya mau beribadah atau tidak; kalau ya, muncul ayat harian (bergiliran tiap hari) lalu pesan *"Kamu anak pintar! Kamu sudah melaksanakan ibadah hari ini."* Saat beribadah, karakter menghadap kiblat (ke kiri/barat) dan bergerak sholat 1 rakaat (sekitar 10 menit waktu game): takbir, berdiri bersedekap, rukuk, i'tidal, sujud, duduk di antara dua sujud, sujud, lalu tasyahud dan salam ke kanan dan kiri. Setelah itu karakter langsung berdiri dan ayat harian muncul. Saat sujud dahi dan kedua telapak tangan menempel di sajadah di samping kepala dengan siku terbuka ke samping; saat duduk di antara dua sujud dan tasyahud telapak tangan diletakkan di atas paha dekat lutut. Karakter perempuan memakai mukena putih selama ibadah. Kalau berhenti di tengah, ibadahnya tidak dihitung.
- **Lantai 2:** tangga turun tepat di atas tangga ruang keluarga, tangga ke rooftop, lorong yang menghubungkan semua ruangan, 🛏️ kamar utama (tidur di sini untuk ganti hari, ada lemari baju untuk ganti warna), 🧸 2 kamar anak yang disiapkan untuk nanti, dan 🌇 balkon untuk bersantai.
- **Rooftop (lantai 3):** taman atap dengan pergola, kursi santai, keran air, dan rak untuk 24 pot. Ada 15 sayuran dan 15 tanaman hias; siram setiap hari dan tanaman siap dijual dalam 3–10 hari sesuai jenisnya. Pupuk 🧪 mempercepat tumbuh 1,5×. Tanaman hias dijual bersama potnya.
- **Toko online:** beli pot, pupuk, benih, dan bibit lewat komputer. Kurir mengantar paket 📦 ke depan rumah sekitar 2 jam (waktu game) kemudian. Rumah baru juga datang dengan hadiah: 4 pot terpasang, dan pot, pupuk, serta benih di tas masing-masing.
- 🌿 Teras depan punya bangku untuk duduk santai.
- **Duduk & rebahan:** sofa depan TV, bangku teras, bangku balkon, dan bangku pergola muat 2 orang berjejer; kursi ruang makan bisa diduduki (sekalian makan). Duduk di sofa ruang keluarga otomatis menyalakan TV. Di rooftop ada 2 kursi santai untuk rebahan. Di kasur ada pilihan **Rebahan saja**; bergerak berarti bangun.
- **Hewan tidur** mulai pukul 20:00 sampai pagi: diam di tempat dengan 💤. Anjing tidak lagi terus mengikuti pemain.

## Karakter, farm bersama, dan turu 💤
- **Karakter sesuai akun:** adindayn bermain sebagai petani perempuan, wawantn sebagai petani laki-laki. Warna baju bisa dipilih (juga di lemari kamar).
- **Satu farm untuk berdua.** Di layar awal pilih **Buat farm baru** atau **lanjutkan salah satu save game**. Kalau pasanganmu sudah main, tombolnya jadi **Gabung ke farm** dia. Hewan, waktu, kebun, kotak penyimpanan, dan uang dipakai bersama.
- **Tidak harus main bareng.** Kalau pasanganmu sedang tidak membuka game, dia dianggap lagi **turu** 💤 dan terlihat tidur di kasur kamar utama (adindayn di kiri, wawantn di kanan).
- Perangkat yang sedang menjalankan farm (badge 🏡) menjaga waktu dan hewan; perangkat lainnya mengikuti (badge 🔗). Kalau yang menjalankan farm pamit, perangkat satunya otomatis mengambil alih.

## Karakter dan pakaian 👗
- Karakter bertubuh proporsional seperti manusia (wajah, rambut, leher, lengan dan kaki terpisah).
- **Pakaian bisa dipadu:** atasan + bawahan, atau satu pakaian terusan/setelan. Ditambah sepatu dan penutup kepala (boleh juga tanpa alas kaki / tanpa penutup kepala).
  - Atasan: kaos lengan pendek & panjang, kemeja lengan pendek & panjang, hoodie, jaket, sweater, kemeja batik, kebaya, jas.
  - Bawahan: rok, rok panjang (termasuk batik), jeans, celana pendek, celana panjang.
  - Terusan & setelan: dress, overall, jumpsuit, piyama, baju olahraga, seragam, baju renang, baju adat Jawa (beskap + jarik), baju adat kebaya + kain.
  - Sepatu: sneakers, sepatu olahraga, sandal, sandal jepit, boots, pantofel, flat shoes, sepatu hak tinggi.
  - Penutup kepala: topi jerami, topi, peci, kupluk, dan hijab (5 warna).
- Pakaian dibeli lewat **laptop** di ruang keluarga (tab 👕 Pakaian), diantar kurir bersama paket, lalu langsung masuk ke lemari pemiliknya. Ganti pakaian di **lemari kamar utama** atau lewat tombol *Ganti pakaian* di layar awal. Pakaian dan baju yang sedang dipakai ikut tersimpan di save game dan terlihat oleh pasangan.

## Kandang, bebek, musim, dan cuaca 🌦️
- **Kandang bisa dimasuki** (ayam, sapi, kambing, domba, bebek) lewat pintunya, sama seperti rumah. Semua kandang memakai model dalam yang sama: lantai jerami, tumpukan jerami, palung makan, dan sarang (untuk ayam/bebek) atau sekat kandang.
- **Hewan masuk kandang** mulai pukul 19:00 dan saat cuaca tidak cerah; besok pagi yang cerah mereka keluar lagi. Kucing dan anjing berteduh di ruang keluarga. Telur selalu muncul di sarang **di dalam kandang** ayam/bebek, jadi masuk kandang untuk mengambilnya.
- **Bebek** jantan (Kwek) dan betina (Bebi) tinggal di kandang berpagar tepat di bawah (selatan) kandang ayam, lengkap dengan rumah bebek dan kolam kecil; bebek betina bertelur 🥚 (Telur Bebek, 90 G).
- **Kolam dangkal**: kolam bebek dan kolam besar bisa dilewati pemain, jadi bebek yang sedang berenang tetap bisa didekati dan dielus.
- **Gerak karakter lebih luwes**: kaki punya lutut dan lengan punya siku. Saat berjalan, lutut menekuk ketika kaki diayun ke depan dan lengan berayun dengan siku sedikit menekuk. Saat duduk, betis menggantung ke bawah, dan saat duduk di sajadah karakter duduk bersimpuh di atas tumit.
- **6 musim**, masing-masing satu bulan (30 hari): 🌸 Semi → ☀️ Panas → 🏜️ Kemarau → 🍂 Gugur → 🌧️ Penghujan → ❄️ Dingin, lalu kembali ke Semi. Warna daun, rumput, dan tanah ikut berubah (daun jingga di musim gugur, salju di musim dingin).
- **Cuaca harian** sesuai peluang musimnya: cerah, hujan, salju (musim dingin), atau badai (dengan kilat dan guruh). Langit jadi kelabu saat hujan, dan suara hujan/angin terdengar.
- Saat **hujan**, pohon buah tersiram sendiri. Di **musim dingin** pohon buah beristirahat dan tidak berbuah. **Taman rooftop** tetap disiram setiap hari, kecuali saat hujan (tersiram sendiri). Di musim dingin rooftop ditutup atap kaca: salju tidak masuk dan tanaman tetap tumbuh, tapi harus disiram.

## Suara 🔊
- Semua suara dibuat langsung dengan Web Audio (tanpa file audio): suara sapi, kambing, domba, ayam, kokok ayam jago tiap pagi, kucing (mengeong/mendengkur), dan anjing saat dielus atau diperah; hewan di dekatmu juga sesekali bersuara sendiri. Ada juga cipratan air saat menyiram dan bunyi kecil saat memanen atau berjualan.
- **Lagu latar** berganti mengikuti waktu: ceria di pagi–siang, lebih santai saat sore, dan lembut di malam hari dengan suara jangkrik. Lagunya disusun acak per frasa, jadi tidak monoton. Suara dari luar terdengar lebih pelan saat di dalam rumah.
- Tombol 🎵 (musik) dan 🔊 (efek suara) di kanan atas untuk menyalakan/mematikan; pilihan diingat di perangkat.

## Tas, alat, dan penyimpanan
- **Tas pribadi 30 slot (3 baris × 10).** Baris paling atas adalah toolbar yang terlihat saat main (tombol 1–0); ketuk 🎒 untuk membuka semua isi tas, lalu tahan-geser (atau ketuk dua slot) untuk menukar tempat barang. Nama alat/barang muncul sebentar saat dipilih. Satu slot menumpuk sampai 99 barang yang sama.
- Isi tas: Hasil panen, telur, susu, benih, pot, dan pupuk masuk tas. Kalau penuh, simpan di 🧊 kulkas (dapur), 📦 kotak penyimpanan (samping kotak pengiriman), atau taruh di 🧺 kotak pengiriman.
- Membuka kulkas/kotak menampilkan isi kotak dan isi tas berdampingan seperti Stardew Valley: ketuk barang untuk memindahkannya (semua atau 1 buah).
- **Kotak pengiriman:** barang di dalamnya terjual saat kalian tidur.
- **Alat** (ada di toolbar): ✋ tangan, 🪣 penyiram (untuk menyiram), 🫙 pemeras susu (sapi dan kambing), ✂️ gunting bulu (domba).
- **Telur** tidak lagi diambil dari ayamnya: setiap pagi telur muncul di sarang di dalam kandang ayam/bebek.

## Menyimpan progres
- Tidak ada simpan otomatis. Simpan lewat tombol 💾, atau saat tidur pilih **Tidur dan simpan progres** lalu pilih slot (ada 10 slot). **Tidur tanpa menyimpan** juga bisa.
- Di link claude.ai, slot tersimpan di penyimpanan bersama artifact, jadi terlihat oleh berdua dan langsung muncul saat pasangan menyimpan (pasangan perlu dibagikan akses yang bisa mengedit). Save yang dulu hanya tersimpan di perangkat ikut diunggah ke penyimpanan bersama begitu tersambung.
- Saat kalian berdua online bersamaan (di claude.ai maupun versi web), daftar save juga saling dikirim lewat koneksi online: slot yang lebih baru di satu perangkat otomatis masuk ke perangkat yang lain. Di versi web tanpa penyimpanan bersama, inilah satu-satunya cara save berpindah, jadi buka game bersamaan sekali agar save tersinkron.

## Cara main
| Kontrol | Aksi |
| --- | --- |
| WASD / panah | Berjalan (tahan Shift untuk lari) |
| E / Spasi | Interaksi: elus hewan, siram, buka kotak, masuk rumah, duduk, tidur di kasur |
| 1–4 | Pilih alat: tangan, penyiram, pemeras susu, gunting bulu |
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

