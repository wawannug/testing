# Farmora — Konsep Peta Wilayah

Dunia Farmora diperluas menjadi 5 wilayah plus pulau bonus. Setiap fungsi gameplay hanya ada di satu tempat.

## 1. Geografi

Air mengalir dari gunung ke laut. Sungai menyambung semua wilayah dan jadi penunjuk arah.

```
                 🏔️ DESA PEGUNUNGAN  (hulu sungai, mata air, kawah)
                        │  sungai
                 🌳 DESA HUTAN        (lereng)
                        │
   [🏡 FARM] ── 🌾 LEMBAH PERSAWAHAN  (desa utama, Desa Lembah Sari)   ✅ sudah dibuat
                        │
                 🏙️ KOTA              (dataran rendah, dekat muara)
                        │
                 🏖️ DESA PANTAI       (muara dan laut)  ──⛴️── 🏝️ Pulau Bonus
```

## 2. Wilayah dan fasilitas

### 🌾 Lembah Persawahan ✅
Toko Tani, Penggilingan Padi, Pasar Tani, Lumbung Desa, Balai Desa, Gereja Katolik, Musala.
Sementara di sini juga: Toko Hewan, Toko Bangunan, Warung Makan, Klinik (nanti pindah ke wilayahnya).

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
1. ✅ **Lembah Persawahan + sistem NPC** (selesai: 11 bangunan + 7 rumah dengan interior, 13 warga dengan jadwal dan dialog, gabah → beras, lumbung, jual di pasar).
2. Rumah Peternakan, Tambang, Pandai Besi.
3. Penggergajian Kayu, Terminal + angkot, Rumah Sakit.
4. Pantai: Pasar Ikan, Galangan Perahu, mancing di laut.
5. Pengolahan & Warung Kopi, Danau Pegunungan, Rumah Madu, Rumah Herbal, Kantor Pos, Supermarket.
6. Pelelangan, Warung Seafood, Pusat Kerajinan, Bank, Salon, Sekolah, tempat ibadah lainnya.
7. Pelabuhan dan Pulau Bonus.

## 5. Teknis
- Setiap wilayah adalah area terpisah; interior bangunan memakai sistem seperti rumah dan kandang.
- Posisi NPC dihitung dari jam game di kedua HP, jadi tidak menambah data online; yang disinkron hanya keakraban dan isi lumbung.
- NPC hanya digambar kalau berada di tempat yang sama dengan pemain.
