# Sistem Pakar Identifikasi Kemungkinan Pemicu Alergi dan Iritasi Kulit

Repositori ini berisi basis pengetahuan (*knowledge base*), dataset terstruktur, dan panduan edukasi sistem pakar berbasis **Forward Chaining** untuk mengidentifikasi kemungkinan pemicu keluhan pada kulit (alergi kontak, dermatitis iritan, urtikaria/biduran, dan fitofotodermatitis).

---

## 📁 Struktur Berkas

- `knowledge_base_extended.json`: Basis pengetahuan terstruktur format JSON yang memuat 16 kelompok pemicu alergi/iritasi, protokol keselamatan (*red flags*), kriteria sindrom klinis, dan aturan inferensi.
- `faq.html`: Halaman antarmuka web interaktif yang menyajikan tanya-jawab (FAQ) seputar keluhan kulit dengan bahasa yang ramah pengguna (*user-friendly*), fitur pencarian instan, dan filter kategori.
- `PPT identifikasi alergi kulit.pptx`: Materi presentasi tugas proyek kuliah semester 5.

---

## 🎯 Cakupan 16 Kelompok Pemicu dalam Basis Pengetahuan

1. **Logam & Aksesori:** Nikel dan kobalt pada jam tangan, anting imitasi, kancing jeans, dan gesper.
2. **Kosmetik & Skincare:** Pengawet (paraben, MI/MCI), pewangi, dan asam eksfoliasi pada produk perawatan wajah.
3. **Sabun & Pembersih Rumah Tangga:** Deterjen pakaian, sabun cuci piring, dan cairan pemutih (dermatitis iritan tangan).
4. **Sarung Tangan & Produk Lateks:** Akselerator karet (tiuram) dan protein lateks.
5. **Tanaman & Getah Liar:** Getah mangga, tanaman hias beracun, dan rumput liar.
6. **Parfum & Minyak Esensial:** Fragrance mix, balsam of Peru, dan minyak atsiri oles.
7. **Pakaian & Tekstil:** Serat sintetis poliester dan pewarna tekstil (disperse dyes).
8. **Lem & Perekat:** Lem bulu mata tiruan (*eyelash*), lem kuku akrilik, dan plester luka.
9. **Cat Rambut:** Senyawa p-Phenylenediamine (PPD) pada pewarna rambut dan henna hitam.
10. **Makanan Pemicu Biduran:** Seafood (udang/kepiting), telur, kacang tanah, dan susu sapi.
11. **Tungau Kasur & Hewan Peliharaan:** Kotoran tungau debu rumah dan bulu hewan peliharaan.
12. **Cuaca & Faktor Fisik:** Alergi suhu dingin, alergi keringat/panas, dan sinar matahari.
13. **Gigitan & Racun Serangga:** Kumbang Tomcat (dermatitis Paederus), kutu kasur (*bed bugs*), dan semut api.
14. **Salep Obat Oles:** Salep antibiotik neomisin bebas dan balsem panas.
15. **Produk Bayi:** Ruam popok (*diaper rash*) dan minyak telon berlebihan.
16. **Bahan Kimia Industri:** Semen basah (kromium), tinner, dan pelarut bengkel.

---

## 🛡️ Protokol Keselamatan (*Safety Red Flags*)

Sistem pakar memprioritaskan keselamatan pengguna. Inferensi otomatis akan mengarahkan pengguna segera ke Instalasi Gawat Darurat (IGD) jika terdeteksi:
- Kesulitan bernapas / napas berbunyi mengi (*stridor/wheezing*).
- Pembengkakan bibir, lidah, atau jalan napas (*angioedema*).
- Pusing berat mendadak, lemas lunglai, atau pingsan (*syok anafilaksis*).
- Ruam merah luas disertai demam tinggi di atas 38,5°C.
- Kulit melepuh luas seperti luka bakar atau sariawan parah pada bibir dan mata.

---

## 💻 Cara Menjalankan

### Melihat Halaman FAQ
Cukup buka berkas `faq.html` langsung di peramban web (Chrome, Firefox, Safari, atau Edge):
```bash
xdg-open faq.html
```

### Mengakses Dataset JSON di PHP
```php
<?php
$data = json_decode(file_get_contents('knowledge_base_extended.json'), true);
echo "Jumlah kelompok pemicu: " . count($data['trigger_groups']);
?>
```

---

*Catatan: Sistem ini dirancang sebagai instrumen skrining awal dan bahan edukasi perkuliahan, bukan sebagai pengganti diagnosis medis resmi oleh dokter spesialis dermatologi.*
