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

- **Lantai 1:** 🚪 ruang tamu, 🛋️ ruang keluarga (sofa, TV, dan **komputer toko online** 🖥️), 🍳 dapur (44 resep masakan + 4 olahan bahan, lihat bagian Memasak) dan 🍽️ ruang makan, 🚿 kamar mandi/WC, serta 🕌 **mushola** dengan 2 sajadah. Di mushola kamu ditanya mau beribadah atau tidak; kalau ya, muncul ayat harian (bergiliran tiap hari) lalu pesan *"Kamu anak pintar! Kamu sudah melaksanakan ibadah hari ini."* Saat beribadah, karakter menghadap kiblat (ke kiri/barat) dan bergerak sholat 1 rakaat (sekitar 10 menit waktu game): takbir, berdiri bersedekap, rukuk, i'tidal, sujud, duduk di antara dua sujud, sujud, lalu tasyahud dan salam ke kanan dan kiri. Setelah itu karakter langsung berdiri dan ayat harian muncul. Saat sujud dahi dan kedua telapak tangan menempel di sajadah di samping kepala dengan siku terbuka ke samping; saat duduk di antara dua sujud dan tasyahud telapak tangan diletakkan di atas paha dekat lutut. Karakter perempuan memakai mukena putih selama ibadah. Kalau berhenti di tengah, ibadahnya tidak dihitung.
- 🚿 **Mandi:** di kamar mandi lantai 1, karakter masuk ke kotak shower, melepas baju (tertutup kaca buram dan uap, jadi diblur), menggosok rambut sambil air mengalir, lalu berpakaian lagi setelah ±7 detik (atau tekan *Selesai mandi*). Mandi memberi +5 energi.
- 🚽 **Kloset:** pilih *Pakai kloset*, karakter duduk dan bagian bawah tubuh tertutup sensor buram (seperti saat mandi); setelah ±5 detik (atau *Selesai, siram*) terdengar air disiram dan karakter berpakaian lagi.
- **Lantai 2:** tangga turun tepat di atas tangga ruang keluarga, tangga ke rooftop, lorong yang menghubungkan semua ruangan, 🛏️ kamar utama (tidur di sini untuk ganti hari, ada lemari baju untuk ganti warna), 🧸 2 kamar anak yang disiapkan untuk nanti, dan 🌇 balkon untuk bersantai.
- **Rooftop (lantai 3):** taman atap dengan pergola, kursi santai, keran air, dan rak untuk 24 pot. Ada 15 sayuran dan 15 tanaman hias; siram setiap hari dan tanaman siap dijual dalam 3–10 hari sesuai jenisnya. Pupuk 🧪 mempercepat tumbuh 1,5×. Tanaman hias dijual bersama potnya.
- **Toko online:** beli pot, pupuk, benih, dan bibit lewat komputer. Kurir mengantar paket 📦 ke depan rumah sekitar 2 jam (waktu game) kemudian. Rumah baru juga datang dengan hadiah: 4 pot terpasang, dan pot, pupuk, serta benih di tas masing-masing.
- 🌿 Teras depan punya bangku untuk duduk santai.
- **Duduk & rebahan:** sofa depan TV, bangku teras, bangku balkon, dan bangku pergola muat 2 orang berjejer; kursi ruang makan bisa diduduki (sekalian makan). Duduk di sofa ruang keluarga otomatis menyalakan TV. Di rooftop ada 2 kursi santai untuk rebahan. Di kasur ada pilihan **Rebahan saja**; bergerak berarti bangun.
- **Hewan tidur** mulai pukul 20:00 sampai pagi: diam di tempat dengan 💤. Anjing tidak lagi terus mengikuti pemain.

## Perkakas 🧰
- **Kotak perkakas** (kotak merah di samping kotak penyimpanan, depan rumah) berisi 2 buah dari tiap alat, satu untuk masing-masing pemain. Ambil alat dari sini; alat langsung masuk ke toolbar (barang lain di toolbar digeser ke tas kalau penuh). Kembalikan alat ke kotak ini kalau tasmu penuh. **Penyiram** selalu ada di tasmu, jadi tidak disimpan di kotak.
- 🪴 **Pot di farm:** pegang pot dari tas, lalu tekan tombol aksi untuk menaruhnya di mana saja di farm (juga di jalan setapak), asal tidak di air, di dalam kandang, atau menabrak benda. Pot bisa ditanami **sayur dan tanaman hias saja** (pohon tidak bisa), disiram, dipupuk, dan dipanen seperti pot rooftop. Dengan ✋ tangan, pot berisi tanaman bisa **diangkat dan dipindah** ke tempat lain kapan saja; pot kosong yang diangkat kembali ke tas. Maksimal 40 pot.
- 🪏 **Cangkul:** cangkul tanah kosong di mana saja selama masuk akal (bukan di jalan setapak, kandang, kolam, bangunan, atau dekat pohon kebun; rumput liar dipotong dulu). Kotak di depan karakter diberi bingkai hijau (bisa) atau merah (tidak bisa). Tanah yang dicangkul lalu bisa ditanami lewat menu **🥬 Sayur / 🌸 Tanaman hias / 🌳 Pohon buah**, atau langsung dengan memilih benih/bibit di tas. Tanaman di tanah disiram, dipupuk, dan dipanen seperti pot rooftop; hujan ikut menyiramnya. Tanah yang dibiarkan kosong 3 hari kembali jadi rumput. Maksimal 60 kotak olahan.
- 🌳 **Bibit buah:** dijual di laptop (tab "🌳 Bibit buah"). **Pohon buah besar** (mangga, durian, alpukat, jeruk, apel, rambutan, kelapa, pisang, pepaya, anggur, dll.) butuh lahan **3×3 kotak**: kotak tengah dicangkul dan 8 kotak di sekelilingnya kosong. **Tanaman buah kecil** (salak, nanas, stroberi, semangka, melon) cukup **1 kotak**. Dari bibit sampai berbuah pertama butuh waktu lama: paling cepat **1 bulan** (30 hari, stroberi) dan paling lama **1 tahun** (180 hari = 6 musim, misalnya durian, kelapa, manggis), asal disiram tiap hari. Hari tanpa siraman tidak dihitung. Bibit tetap tumbuh di musim dingin; pohon yang sudah dewasa berbuah seperti kebun buah dan istirahat di musim dingin. Pohon bisa ditebang dengan kapak. Maksimal 12 pohon tanaman sendiri.
  - Lama tumbuh sampai berbuah pertama: stroberi 30 hari · semangka, melon 35 · pepaya, pisang, buah naga 60 · jambu 75 · anggur, markisa 90 · nanas 100 · salak, jeruk, belimbing, jambu air 120 · apel, pir 140 · alpukat, mangga, rambutan, sawo, sirsak, kelengkeng 150 · kelapa, durian, manggis, duku, nangka 180.
- ⛏️ **Beliung:** pecahkan 6 batu besar di sebelah barat (selatan rumah, dekat kandang ayam). Dapat 🪨 batu, kadang 🟠 bijih tembaga, ⚙️ besi, atau 🟡 emas. Batu yang pecah sebagian muncul lagi tiap pagi.
- 🪓 **Kapak:** tebang 6 pohon kayu (pojok barat laut, pojok tenggara, dan dekat ladang). 3 ayunan untuk menumbangkan pohon (🪵 kayu ×3), lalu bersihkan tunggulnya (🪵 kayu ×1). Pohon tumbuh lagi setelah beberapa hari.
- 🎣 **Pancing:** pegang pancing di dekat kolam besar atau kolam bebek, **tahan** tombol pancing di kanan bawah (atau E/Spasi): meteran di atas kepala naik-turun, makin lama ditahan makin jauh lemparannya; lepas untuk melempar. Kalau kail mendarat di darat (terlalu dekat atau terlalu jauh), kail langsung kembali dan harus dilempar lagi. Tidak ada jendela saat menunggu: pelampung merah-putih mengapung di air. Saat ikan makan umpan, pelampung tenggelam-timbul dengan riak besar, muncul tanda ❗ di atas kepala (HP bergetar), dan kamu harus segera menekan tombol pancing lagi. Terlalu cepat atau terlambat, ikannya kabur; berjalan menjauh menggulung kail. Setelah itu muncul **panel tarik ikan** kecil di samping karakter (tanpa jendela/pop-up), seperti Stardew Valley: ikan bergerak naik-turun dan ada bar hijau. **Tahan tombol pancing** di kanan bawah (di komputer: tahan Spasi/E atau tombol mouse di tombol pancing) supaya bar naik, lepas supaya turun. Selama ikan berada di dalam bar, meteran tangkapan di kanan naik; kalau ikan keluar, meteran turun. Meteran penuh = ikan tertangkap, kosong = ikan lepas. Tombol ✕ kecil di panel untuk melepas ikan. Disimulasikan dengan pemain yang salah langkah 20%: ikan biasa hampir selalu tertangkap, ikan sedang 80–95%, ikan sulit (udang galah, gabus, belut) 25–50%, dan ikan langka (toman, sidat, arwana) sekitar 12–22%, jadi butuh latihan. Kadang yang tersangkut cuma 👢 sepatu bot tua.
- 🌊 **Danau** tempat memancing tidak bisa dilewati karakter (kolam bebek tetap seperti biasa).
- **Jenis ikan** (makin langka makin sulit, gerakannya berbeda: tenang, campuran, melesat, suka di dasar, atau suka di atas): wader, sepat, mujair, ikan mas, nila, lele, tawes, betok, bawal, patin, gurame, baung, udang galah, gabus, belut, toman, sidat, dan ⭐ **arwana** (paling langka, 1.500 G). Kolam besar punya ikan besar (bawal, patin, gurame, toman, arwana…); kolam bebek punya ikan kecil, betok, dan belut. Lele, baung, belut, dan sidat lebih sering menggigit malam hari; gabus pagi hari; ikan langka lebih sering muncul saat hujan.
- Resep ikan baru: pecel lele, udang goreng tepung, pindang patin (selain ikan bakar, pepes ikan, dan gurame goreng).
- 🌾 **Sabit:** potong rumput liar yang tumbuh di sekitar farm (bertambah tiap malam). Dapat 🌿 rumput, kadang benih kangkung liar.
- Semua hasilnya bisa dijual di kotak pengiriman atau diberikan ke pasangan. Kerja dengan alat memakai energi: cangkul/tanam 2, beliung 4, kapak 4, pancing 2, sabit 1.
- Alat yang dipilih terlihat di tangan kanan karaktermu (juga oleh pasangan) dan diayunkan saat dipakai. Ikon alat di toolbar dan tombol aksi digambar khusus, termasuk penyiram baru berbentuk gembor.

## Cara bergerak 🕹️👆
- Ada 2 pilihan, ganti dengan tombol di kanan atas (di samping 💾). Pilihan tersimpan di perangkat masing-masing.
  - **🕹️ Joystick:** geser joystick di kiri bawah (di komputer: WASD atau tombol panah).
  - **👆 Ketuk tujuan:** joystick disembunyikan. Ketuk tanah atau tempat yang ingin dituju, lalu muncul lingkaran putih di sana dan karaktermu berjalan sendiri ke situ (berlari kalau jauh). Berhenti sendiri kalau sudah sampai atau terhalang pagar/dinding; ketuk tempat lain untuk mengganti tujuan.

## Energi, makan, dan interaksi berdua ⚡🤗
- **Energi ⚡ (0–200)** tampil di bawah jumlah gold. Kerja di farm memakai energi: siram atau panen pohon dan pot (2), elus, perah, atau cukur hewan (2), ambil telur (1), isi ember (1), dan memasak (3). Kalau energi habis, kamu tidak bisa bekerja dan jalan lebih pelan; makan atau tidur dulu.
- **Tidur** di kasur mengisi energi penuh. Kalau tertidur otomatis pukul 00:00, energi terisi minimal 140.
- **Makan masakan:** pilih masakan di toolbar, lalu tekan tombol **🍽️ Makan** (atau F, atau tombol aksi kalau tidak ada yang lain di dekatmu). Telur dadar +20, puding susu +25, tumis kangkung +30, salad segar +30, jus mangga susu +25, sambal tomat +15, sayur sop +45, ikan bakar +35; masakan lain memberi energi sesuai harganya (nasi putih +10 sampai rendang +45).
- **Memasak 🍳:** di kompor dapur, layarnya seperti membuka tas: kiri **alat masak** (pilih satu) dan isi wajan/panci, kanan **bahan** dari tas dan kulkas. Ketuk bahan untuk memasukkan, ketuk lagi di wajan untuk mengeluarkan. Kalau kombinasi alat + bahan cocok dengan resep, muncul "✨ Jadi: …" dan tombol **Masak**; kalau belum pas, ada petunjuk resep yang mirip dan bahan yang kurang. Tab **📖 Buku resep** berisi semua resep, dikelompokkan per kategori (🍚 makanan berat, 🍗 lauk & sayur, 🍟 camilan, 🍮 penutup, 🥤 minuman, 🫚 olahan bahan, atau 📚 semua); tombol **Pakai** langsung mengisi kombinasinya.
- **Resep lokal Indonesia:** nasi putih, nasi goreng, nasi uduk, bubur ayam, mi goreng, mi ayam, soto ayam, opor ayam, rendang, sate ayam, gado-gado, sayur lodeh, tempe goreng, bakwan sayur, martabak telur, pisang goreng, kolak pisang, pepes ikan, gurame goreng, rujak buah, es teh manis, kopi susu, jus alpukat, perkedel jagung, jagung bakar, bubur jagung manis, singkong goreng, getuk, tape singkong, kolak ubi, sayur asem, tumis buncis, gudeg, nasi kuning, wedang jahe, es buah, ditambah resep lama (telur dadar, puding, tumis kangkung, salad, jus mangga, sambal tomat, sayur sop, ikan bakar). Harga jual masakan sekitar 1,5× harga bahan mentahnya.
- **Alat masak** (tab "🍳 Alat masak" di laptop, sekali beli dan tidak habis): pisau & talenan 60 G, wajan 150 G, panci 180 G (tiga ini sudah ada sejak awal), cobek & ulekan 120 G, kukusan 220 G, panggangan arang 300 G, penanak nasi 450 G, blender 500 G. Alat disimpan di **🗄️ rak alat masak** dapur (dipakai berdua) atau di tas.
- **Bahan masak** (tab "🧂 Bahan masak"): bahan pasar seperti beras, bawang merah/putih, garam, gula, minyak goreng, kecap, tepung, tahu, tempe, mi, kacang tanah, bumbu rempah, daging ayam/sapi, teh, kopi, plus hasil kebun & ternak (telur, susu, sayur, ikan, buah). Harga beli online **lebih mahal** daripada harga jualnya di kotak pengiriman (misalnya beras beli 40 G, dijual lagi 24 G; telur beli 80 G, dijual 50 G), jadi bahan dari kebun sendiri paling untung.
- **Olahan bahan:** jahe + kunyit + lengkuas + serai → 🫚 bumbu rempah ×2 (cobek), tebu ×2 → gula ×2 (panci), kedelai ×2 → tempe ×2 (kukusan), kedelai ×2 + garam → tahu ×2 (panci). Panen 🌾 padi langsung jadi beras.
- **Tanaman bahan dapur** (benihnya di tab sayur): bawang merah, bawang putih, jahe, kunyit, lengkuas, serai, padi, jagung, singkong, ubi jalar, kacang tanah, kedelai, tebu, kacang panjang, buncis, labu siam, kemangi, teh, dan kopi. Bawang, kacang tanah, teh, dan kopi hasil kebun sama dengan bahan pasar, jadi tidak perlu dibeli lagi. Tanaman hias baru: sedap malam dan kenanga.
- **Buah baru dari bibit** (tidak ada di kebun buah, hanya ditanam sendiri): nangka, sirsak, belimbing, kelengkeng, jambu air (pohon 3×3), markisa (merambat di para-para, 3×3), dan buah naga (1 kotak).
- **Peluk 🤗:** dekati pasanganmu lalu tekan tombol aksi (**Peluk / beri hadiah**). Kalian berdua melangkah mendekat, saling berhadapan, dan berpelukan dengan hati beterbangan, terlihat di kedua layar. Setiap pelukan menambah +5 ⚡ untuk berdua.
- **Beri hadiah 🎁:** dari menu yang sama, pilih satu barang dari tasmu (hasil panen, telur, masakan, pot, benih…); barangnya pindah ke tas pasanganmu, dan pasanganmu kegirangan: melompat kecil sambil melambaikan kedua tangan, dikelilingi hati dan ikon 🎁 (terlihat di kedua layar).

## Karakter, farm bersama, dan turu 💤
- **Karakter sesuai akun:** akun pertama bermain sebagai petani perempuan, akun kedua sebagai petani laki-laki. Pakaian dipilih di lemari kamar setelah masuk game (layar awal tidak lagi meminta memilih baju). Awalnya kedua pemain tidak memakai topi.
- **Satu farm untuk berdua.** Di layar awal pilih **Buat farm baru** atau **lanjutkan salah satu save game**. Kalau pasanganmu sudah main, tombolnya jadi **Gabung ke farm** dia. Hewan, waktu, kebun, kotak penyimpanan, dan uang dipakai bersama.
- **Tidak harus main bareng.** Kalau pasanganmu sedang tidak membuka game, dia dianggap lagi **turu** 💤 dan terlihat tidur di kasur kamar utama (pemain perempuan di kiri, pemain laki-laki di kanan).
- Perangkat yang sedang menjalankan farm (badge 🏡) menjaga waktu dan hewan; perangkat lainnya mengikuti (badge 🔗). Kalau yang menjalankan farm pamit, perangkat satunya otomatis mengambil alih.

## Desa 🏘️ dan crafting 🔨
- **Pagar keliling farm.** Seluruh batas farm dipagari kayu. Di sisi selatan (bawah) ada **gerbang "Ke Desa"**; dekati lalu tekan tombol aksi. Desa ada di selatan farm: kamu masuk dari gerbang di **atas** desa, berjalan turun lewat jalan di antara toko ke jalan utama, dan pulang lewat gerbang atas itu lagi (masuk farm dari gerbang selatan).
- 🗺️ **Peta:** tombol *🗺️ Peta* di bawah jam (atau tombol M) menampilkan farm, jalan ke selatan, dan desa, beserta posisimu dan pasanganmu (panah = arah hadap). Kalau sedang di dalam rumah atau kandang, posisinya ditandai di bangunan itu.
- **Jalan setapak lama dihapus**; sekarang farm berumput. Jalan bisa dibuat sendiri (jalan batu / papan) di meja kerja.
- **Desa Farmora** punya jalan utama, air mancur, bangku, lampu, dan enam bangunan. Barang yang dibeli langsung masuk tas (tanpa kurir) dan lebih murah dari toko online:
  - 🌱 **Toko Bibit:** benih sayur, bibit hias, dan bibit pohon buah (±10% lebih murah).
  - 🐄 **Toko Hewan:** pakan ternak (±15% lebih murah), langsung masuk karung gudang kandang.
  - 🧺 **Pasar:** bahan masak (±10% lebih murah).
  - 🧱 **Toko Bangunan:** kayu, batu, tanah liat, bijih tembaga/besi, pot, dan pupuk untuk crafting.
  - 🍜 **Warung Makan:** masakan siap makan (untuk energi).
  - 🏥 **Klinik:** periksa & istirahat (150 G, energi penuh) atau pijat refleksi (60 G, +60 energi).
- 🔨 **Meja kerja** di sebelah kotak perkakas. Resep: pagar kayu (2 kayu), pagar batu (3 batu), jalan batu ×2 (2 batu), jalan papan ×2 (1 kayu), kursi kayu (4 kayu), bangku taman (4 kayu + 1 besi), lampu taman (kayu + batu + tembaga, menyala saat malam), orang-orangan sawah (3 kayu + 2 rumput), pot (2 tanah liat), dan pupuk kompos (3 rumput).
- **Memasang barang:** pegang barang hasil crafting di toolbar, hadapkan ke tanah, tekan tombol aksi. Pagar mengikuti arah hadapanmu. Barang tidak bisa dipasang di kandang, di air, di depan pintu atau gerbang, atau menabrak benda lain. Pagar, kursi, bangku, lampu, dan orang-orangan menghalangi jalan; jalan batu dan papan bisa diinjak. Ambil lagi dengan ✋ tangan.
- **Sumber daya:** kayu (kapak), batu dan bijih (beliung), rumput (sabit), dan baru: 🟤 **tanah liat** yang kadang muncul saat mencangkul (atau dibeli di Toko Bangunan).

## Karakter dan pakaian 👗
- Karakter bertubuh proporsional seperti manusia (wajah, rambut, leher, lengan dan kaki terpisah).
- **Pakaian bisa dipadu:** atasan + bawahan, atau satu pakaian terusan/setelan. Ditambah sepatu dan penutup kepala (boleh juga tanpa alas kaki / tanpa penutup kepala).
  - Atasan: kaos lengan pendek & panjang, kemeja lengan pendek & panjang, hoodie, jaket, sweater, kemeja batik, kebaya, jas, **baju koko** (putih, hitam, hijau, biru), **tunik muslimah**.
  - Bawahan: rok, rok panjang (termasuk batik), **sarung** kotak-kotak (4 warna), jeans, celana pendek, celana panjang.
  - Terusan & setelan: dress, overall, jumpsuit, piyama, baju olahraga, seragam, baju renang, baju adat Jawa (beskap + jarik), baju adat kebaya + kain, **gamis (baju muslim)** 5 warna, **setelan koko & sarung**.
  - Sepatu: sneakers, sepatu olahraga, sandal, sandal jepit, boots, pantofel, flat shoes, sepatu hak tinggi.
  - Penutup kepala: topi jerami, topi, **peci hitam (kopiah)**, kupluk, dan hijab (5 warna).
- Pakaian dibeli lewat **laptop** di ruang keluarga (tab 👕 Pakaian), diantar kurir bersama paket, lalu langsung masuk ke lemari pemiliknya. Ganti pakaian di **lemari kamar utama**. Pakaian dan baju yang sedang dipakai ikut tersimpan di save game dan terlihat oleh pasangan.

## Kandang, bebek, musim, dan cuaca 🌦️
- Pagar kandang punya bukaan tepat di depan pintu bangunan kandang, jadi tidak ada pagar atau wadah yang menghalangi pintu.
- **Kandang bisa dimasuki** (ayam, sapi, kambing, domba, bebek) lewat pintunya, sama seperti rumah. Semua kandang memakai model dalam yang sama: lantai jerami, tumpukan jerami, palung makan, dan sarang (untuk ayam/bebek) atau sekat kandang.
- 🌾 **Pakan ternak (diberi sendiri):** setiap kandang (ayam, bebek, sapi, kambing, domba) punya **gudang pakan** berupa karung di samping wadah, awalnya penuh **500 porsi**. Pakan tidak masuk wadah sendiri: masuk kandang, ambil pakan dari **karung** (tombol aksi, otomatis sejumlah hewan di kandang itu), lalu taruh di **wadah pakan** (1 porsi per hewan). Pakan juga bisa ditaruh di **wadah luar** dekat pagar kandang (isinya sama). Begitu wadah berisi, hewan yang belum makan hari itu **berjalan sendiri ke wadah dan makan** (kepala menunduk beberapa detik, 1 porsi per hewan); kalau di dalam kandang, mereka makan di wadah dalam. Yang belum sempat makan, makan sisa pakan di wadah malam harinya. Jadi wadah perlu diisi lagi setiap hari. Jerami di wadah menunjukkan isinya.
- Pakan dibeli di laptop (tab **🌾 Pakan ternak**), 10 porsi per bungkus, dan **langsung masuk karung gudang kandangnya** (tanpa kurir), maksimal 500. Harga per porsi ±25% dari hasil hewan per hari: ayam 125 G, bebek 225 G, sapi 315 G, kambing 565 G, domba 850 G per 10 porsi.
- 😞 **Hewan lapar** (wadahnya tidak diisi) sedih: muncul wajah sedih di atasnya, hatinya turun, dan besoknya tidak menghasilkan susu, wol, atau telur. Begitu wadahnya diisi, hewan yang lapar datang dan makan.
- 💩 **Kotoran:** tiap malam setiap hewan ternak meninggalkan kotoran di kandangnya (paling banyak 5 per kandang). Ambil 🧹 **sapu** di kotak perkakas, lalu sapu kotorannya; kadang jadi 🧪 pupuk. Kucing dan anjing peliharaan mandiri: tidak perlu diberi makan dan tidak meninggalkan kotoran. Kandang yang kotor membuat hewan kurang senang.
- ❤️ **Hati hewan 0–10:** naik kalau dielus (+2 per hari), diberi makan (+1,5 per malam), kandangnya bersih (+1), dan hasilnya diambil (+1); turun kalau tidak dielus, lapar, atau kandang kotor. Kalau dirawat telaten setiap hari, hati penuh 10 dalam ±1 tahun (180 hari).
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
- **Kotak pengiriman:** barang di dalamnya terjual saat kalian tidur. Saat hari baru dimulai, kedua pemain melihat **rekap penjualan** semalam: tiap barang, jumlah, harga, total penjualan, dan uang sekarang.
- **Ganti hari harus tidur berdua.** Kalau satu pemain memilih tidur di kasur, ia tidur 💤 dan muncul tulisan "menunggu … tidur juga". Hari baru dimulai setelah pemain kedua juga tidur. Pasangan yang sedang tidak membuka game dianggap sudah turu, jadi tidak perlu ditunggu. Bergerak membuatmu bangun lagi. **Rebahan saja** tidak mengganti hari, tapi kalau rebahan 1 jam (waktu game) tanpa bergerak, kamu ketiduran otomatis tanpa menyimpan. Pukul 00:00 kalian berdua tetap tidur otomatis.
- **Alat** (ada di toolbar): ✋ tangan, 🪣 penyiram (untuk menyiram), 🫙 pemeras susu (sapi dan kambing), ✂️ gunting bulu (domba).
- **Telur** tidak lagi diambil dari ayamnya: setiap pagi telur muncul di sarang di dalam kandang ayam/bebek.

## Menyimpan progres
- **Satu save untuk berdua.** Tidak ada simpan otomatis. Simpan lewat tombol 💾, atau saat tidur pilih **Tidur dan simpan progres**; **Tidur tanpa menyimpan** juga bisa. Hanya ada satu save dan dipakai bersama: siapa pun yang menyimpan terakhir (pemain mana pun dari kalian berdua), save itulah yang muncul sebagai **▶ Lanjutkan** untuk kalian berdua besoknya. Membuat farm baru meminta konfirmasi dulu, karena menyimpannya akan mengganti save bersama.
- Di link claude.ai, save tersimpan di penyimpanan bersama artifact, jadi selalu tersinkron walau kalian main bergantian (pasangan perlu dibagikan akses yang bisa mengedit). Save yang dulu hanya tersimpan di perangkat ikut diunggah begitu tersambung. Dari 10 slot versi lama, save yang paling baru dipakai.
- Saat kalian berdua online bersamaan, save yang lebih baru juga dikirim lewat koneksi online ke perangkat yang lain.
- **Versi web (GitHub Pages):** main bareng memakai dua jalur sekaligus, yaitu relay lewat broker MQTT publik (broker.emqx.io dan broker.hivemq.com, websocket aman) dan koneksi langsung PeerJS. Jalur relay tetap jalan di data seluler maupun Wi-Fi yang ketat, di mana koneksi langsung WebRTC sering gagal. Relay juga menyimpan satu save bersama, jadi save terakhir sampai ke perangkat pasangan walau kalian main bergantian. Catatan: broker publik bisa dibaca siapa saja yang tahu nama topiknya, dan tidak menjamin data disimpan selamanya, jadi save juga tetap tersimpan di perangkat masing-masing.

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
- Hari dimulai pukul **04:00** saat langit masih gelap, lalu perlahan terang menjelang pagi (terang penuh pukul 07:00). Masuk ke pintu rumah untuk tidur; paling malam pukul **00:00**, saat itu kalian otomatis tidur (ada pengingat pukul 23:00). Peternakan baru aktif pukul **05:00**, ditandai ayam jago yang berkokok 🐓: sebelum itu hewan masih tidur di kandang, lalu keluar kalau cuaca cerah.
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
  - Di versi web (GitHub Pages): tersambung lewat dua jalur sekaligus, relay internet melalui broker MQTT publik (tetap jalan di data seluler dan Wi-Fi yang ketat) dan koneksi langsung PeerJS (WebRTC). Ada tombol untuk menyalin link undangan.

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

Video mengalir langsung antar perangkat lewat WebRTC melalui [PeerJS](https://peerjs.com/), dengan server TURN publik (Open Relay) sebagai cadangan. Bersamaan dengan itu, kedua HP juga tersambung lewat relay internet (broker MQTT publik). Jadi kalau koneksi langsung gagal, misalnya di data seluler, kalian tetap terhubung: hitung mundur dan foto berdua tetap jalan, dan pratinjau pasangan tampil sebagai gambar kecil yang diperbarui beberapa kali per detik.

**Penting:** kamera dan mode berdua tidak jalan di link artifact claude.ai, karena link itu memblokir kamera dan WebRTC. Pakai versi web, misalnya GitHub Pages:
1. Buka **Settings → Pages** di repo ini.
2. Di **Source**, pilih *Deploy from a branch*, branch `claude/cloud-ldok5v` (atau `main` setelah digabung), folder `/ (root)`, lalu **Save**.
3. Setelah 1–2 menit, Fotoin bisa dibuka di https://wawannug.github.io/testing/games/fotoin/

