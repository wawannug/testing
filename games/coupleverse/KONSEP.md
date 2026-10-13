# Coupleverse — Our Little World ❤️

Game papan online untuk dua orang (pasangan) dengan mekanisme ala Monopoli. Setiap pemain membangun aset pribadi, tetapi keduanya juga bekerja sama menyelesaikan misi untuk membeli Rumah Impian.

> Dua perjalanan, satu dunia.

## 1. Pilar desain
| Pilar | Artinya di game |
|---|---|
| **Bersaing secara ringan** | Ada uang dan properti pribadi, sewa, dan tukar-menukar aset. Tidak ada yang bangkrut: sewa maksimal setengah uang pemain. |
| **Menang bersama** | Tujuan akhirnya Rumah Impian yang dibeli dari celengan bersama. Kemenangan pribadi hanya berupa gelar. |
| **Ngobrol, bukan cuma lempar dadu** | Kartu Pasangan berisi pertanyaan, tebak kesukaan, dan aktivitas kecil. Boleh dilewati tanpa hukuman. |
| **Kenangan** | Jawaban kartu dan momen kencan tersimpan di Album. |

## 2. Alur satu sesi (sekitar 30–45 menit)
1. Pemain pertama membuat room dan mendapat kode, misalnya `K7Q2M`. Pasangan bergabung memakai kode itu.
2. Pemain bergantian melempar **satu dadu enam sisi**. Pion berjalan di **papan 40 petak**.
3. Di setiap petak ada aksinya sendiri: beli, renovasi, bayar sewa, ambil kartu, setor celengan, atau kencan.
4. Kapan saja, pemain boleh **menyetor ke celengan**, **mengirim bantuan**, atau **menawarkan properti** ke pasangan.
5. Setelah 4 misi pertama selesai dan celengan mencapai 2.000, kalian membeli **Rumah Impian** dan menang bersama. Di akhir, gelar dibagikan.

## 3. Papan 40 petak
- **Pojok:** 🏠 Rumah Kita (mulai, +200), 🚦 Macet, 🌳 Taman Kota (Kotak Kejutan), 🧭 Salah Jalan (ke Macet).
- **8 kelompok properti:**

  | Kelompok | Properti | Harga |
  |---|---|---|
  | Jajanan | Warung Kopi, Toko Roti | 60 |
  | Bunga & Foto | Toko Bunga, Kebun Mawar, Studio Foto | 100–120 |
  | Buku | Toko Buku, Perpustakaan, Kafe Buku | 140–160 |
  | Kuliner | Rumah Makan Padang, Kedai Bakso, Restoran Seafood | 180–200 |
  | Belanja | Butik, Salon, Mal | 220–240 |
  | Pantai | Penginapan Pantai, Kafe Pantai, Resor Mungil | 260–280 |
  | Kencan | Kafe Romantis, Toko Kue, Restoran Rooftop | 300–320 |
  | Bukit & Danau | Villa Bukit, Villa Danau | 350–400 |

- **Transportasi** (Halte Bus, Stasiun, Pelabuhan, Bandara): sewa 25 / 50 / 100 / 200 tergantung jumlah yang dimiliki.
- **Petak spesial:**
  - 💌 Kartu Pasangan (3 petak)
  - ❓ Kesempatan (3 petak)
  - 🐷 Celengan Bersama
  - 💑 Tempat Kencan
  - 💡📶 Tagihan Listrik dan Tagihan Internet, uangnya masuk Kotak Kejutan

## 4. Ekonomi
- **Modal dan bonus mulai:**
  - Modal awal 1.500 per pemain.
  - Lewat Rumah Kita: +200.
  - Pemain yang uangnya kurang dari setengah uang pasangan mendapat **+100 tambahan** (bantuan untuk yang tertinggal).
- **Sewa:** sekitar 10% dari harga, ×3 di ★★, dan ×7 di ★★★. Kalau satu kelompok warna dikuasai lengkap, sewa ×1,5.
- **Renovasi:** 50% dari harga, dilakukan saat mampir ke properti sendiri, sampai ★★★.
- **Batas sewa:** maksimal ½ uang pemain yang membayar (paling sedikit 20), jadi tidak ada yang bangkrut.
- **Kotak Kejutan:** tagihan masuk ke sini, dan siapa pun yang berhenti di Taman Kota mengambil isinya.

## 5. Dompet bersama dan misi
**Celengan bersama** terisi dari:
- setoran sukarela (+50 / +100 kapan saja);
- petak Celengan (setor 100, mendapat bonus 20);
- menjawab Kartu Pasangan (+60);
- kartu Kesempatan "investasi".

| # | Misi | Syarat |
|---|---|---|
| 1 | 💑 Kencan | Berhenti di Tempat Kencan dan pakai 100 dari celengan |
| 2 | 🐷 Tabungan | Celengan pernah berisi 500 |
| 3 | 🏘️ Properti | Berdua memiliki 3 jenis properti berbeda |
| 4 | 💌 Kartu | Menjawab 5 Kartu Pasangan |
| 5 | 🏡 Rumah Impian | Membeli dengan 2.000 dari celengan setelah misi 1–4 selesai → **menang bersama** |

**Gelar akhir:** Juragan Properti, Raja Sewa, Si Paling Menabung, Pujangga Hati.

## 6. Kartu
- **Kartu Pasangan (20 di prototipe).** Kategorinya: Deep Talk, Kenangan, Tebak Kesukaan, Masa Depan, Impian, dan Aktivitas. Jawaban boleh diketik (disimpan ke Album) atau cukup diobrolkan langsung. Kartu boleh dilewati tanpa hukuman.
- **Kesempatan (10).** Contohnya: bonus kerja, traktir atau diberi uang jajan oleh pasangan, investasi bersama, undian, maju ke Taman Kota, mundur 3 petak, macet, renovasi gratis, dan kupon diskon 30%.

## 7. Interaksi
- **Tawar properti:** tawarkan properti milikmu ke pasangan dengan harga tertentu, lalu pasangan menerima atau menolak.
- **Kirim bantuan:** kirim 50 atau 100 ke pasangan.
- **Obrolan:** pesan singkat dan reaksi emoji (❤️😆😭😡🤗🥺) yang muncul besar di layar pasangan.

## 8. Teknis prototipe (`coupleverse.html`)
- **Satu halaman web.**
  - Data room disimpan di database artifact (`games/<KODE>`).
  - Obrolan dan catatan ada di `games/<KODE>/feed`, album di `games/<KODE>/album`.
  - Kedua HP berlangganan dokumen yang sama secara langsung.
- **Mode cadangan "Main berdua di satu HP"** berjalan tanpa internet, dan progresnya tersimpan di browser.
- **Giliran:** hanya pemain yang sedang gilirannya yang melempar dadu dan memutuskan aksi. Animasi dadu dan pion diputar di kedua layar.
- **Batasan prototipe:**
  - Belum ada lelang dan belum ada gadai properti.
  - Kalau kedua pemain menekan tombol pada detik yang persis sama, simpanan yang terakhir yang dipakai.

## 9. Pengembangan berikutnya
1. Tema dan dekorasi kota yang berubah sesuai properti yang dibangun (kota tampak "tumbuh").
2. Lebih banyak Kartu Pasangan per kategori, dan kartu yang bisa ditulis sendiri oleh pasangan.
3. Mini-game duel saat kedua pion berada di petak yang sama.
4. Album berbentuk buku kenangan yang bisa diunduh.
5. Kejadian musiman (Hari Valentine, ulang tahun jadian) dengan misi khusus.
