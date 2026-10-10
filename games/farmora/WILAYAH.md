# Farmora — Konsep Peta Wilayah

Dunia Farmora diperluas menjadi 5 wilayah plus pulau bonus. Setiap fungsi gameplay hanya ada di satu tempat.

## 1. Geografi

Air mengalir dari gunung ke laut. Sungai menyambung semua wilayah dan jadi penunjuk arah.

```
                                   🏙️ KOTA SENTOSA (utara)
                                          │
  🏔️ DESA PEGUNUNGAN ── 🌳 DESA HUTAN ── [🏡 FARM + jalan lingkar] ── 🏖️ DESA PANTAI ── 🌊 laut ──⛴️── 🏝️ PULAU KENCANA
     (danau, tambang)                            │
                                   🌾 LEMBAH PERSAWAHAN (selatan)

  Semua wilayah ✅ sudah dibuat dan tersambung langsung (tanpa pindah layar).
```

## 2. Wilayah dan fasilitas

### 🌾 Lembah Persawahan ✅
Toko Tani, Penggilingan Padi, Pasar Tani, Lumbung Desa, Balai Desa, Gereja Katolik, Musala.
Toko Hewan pindah ke Rumah Peternakan (Pegunungan), Toko Bangunan ke Penggergajian Kayu (Hutan), Klinik ke Rumah Sakit (Kota).

### 🏔️ Desa Pegunungan
Rumah Peternakan (menggantikan Toko Hewan), Tambang, Pandai Besi (upgrade alat), Pengolahan Kopi, Warung Kopi, Masjid, Danau (ikan air dingin).

### 🌳 Desa Hutan
Penggergajian Kayu (sekaligus toko bangunan), Rumah Herbal, Rumah Madu, Pusat Kerajinan, Gereja Protestan.

### 🏙️ Kota
Rumah Sakit (menggantikan Klinik), Bank, Supermarket (hanya menjual), Sekolah, Salon, Kantor Pos (paket online), Terminal (angkutan antarwilayah), Vihara.

### 🏖️ Desa Pantai
Pelabuhan, Pasar Ikan (siang), Pelelangan Ikan (subuh, harga tinggi), Galangan Perahu (mancing di laut), Warung Seafood, Kelenteng.

### 🏝️ Pulau Bonus
Pura, Tempat Snorkeling, Penginapan, Toko Suvenir.

## 3. Siapa membeli apa
| Barang pemain | Dijual ke |
|---|---|
| Sayur, buah, gabah, beras | Pasar Tani ✅ |
| Ikan | Pasar Ikan / Pelelangan (langka, subuh) |
| Kopi, madu, jamu, kerajinan | tempat pembuatnya masing-masing |
| Semua barang (harga lebih rendah) | Kotak pengiriman di farm |

## 4. Prioritas
1. ✅ **Lembah Persawahan + sistem NPC**.
2. ✅ **Semua wilayah** (Kota, Hutan, Pegunungan, Pantai, Pulau) dengan 60 bangunan berinterior dan 43 warga.
3. Berikutnya: event musiman, pertemanan lebih dalam, dan perluasan pulau.

## 5. Teknis
- Setiap wilayah adalah area terpisah; interior bangunan memakai sistem seperti rumah dan kandang.
- Posisi NPC dihitung dari jam game di kedua HP, jadi tidak menambah data online; yang disinkron hanya keakraban dan isi lumbung.
- NPC hanya digambar kalau berada di tempat yang sama dengan pemain.
