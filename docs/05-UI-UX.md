# 05 — Pedoman UI/UX

Prinsip utama dari riset: **visual yang membantu ya, hiasan tidak** (T-10, T-11, T-21).

## 1. Prinsip Desain

1. **Satu layar, satu tugas.** Tidak ada layar yang meminta dua hal sekaligus.
2. **Gambar dan angka menyatu.** Label ukuran ditempel pada rusuk bangun, bukan di keterangan terpisah.
3. **Polos tapi rapi.** Latar putih/terang polos; warna hanya untuk makna (p/l/t, benar/salah).
4. **Kendali di tangan siswa.** Tidak ada animasi otomatis yang berjalan terus; ada *Lanjut*, *Ulangi*, *Jeda*.
5. **Teks hemat.** Kalimat ≤ 15 kata, maksimal 3 kalimat per layar belajar.
6. **Umpan balik segera dan spesifik**, tanpa suara/animasi yang mengejutkan.

## 2. Yang DILARANG di layar belajar
- Latar bergambar, pola, atau gradasi ramai.
- Maskot/karakter yang bergerak saat siswa sedang mengerjakan.
- Pop-up iklan, notifikasi, atau konfeti berulang.
- Lebih dari 1 animasi berjalan bersamaan.
- Teks berjalan (marquee) atau teks berkedip.

## 3. Palet Warna

| Token | Warna | Fungsi |
|---|---|---|
| `--bg` | #FFFFFF / (gelap: #121417) | latar |
| `--text` | #1F2328 / (gelap: #E6E6E6) | teks utama |
| `--primary` | #3B5BDB | tombol utama |
| `--p-panjang` | #1C7ED6 (biru) | panjang |
| `--l-lebar` | #2F9E44 (hijau) | lebar |
| `--t-tinggi` | #E8590C (oranye) | tinggi |
| `--s-sisi` | #7048E8 (ungu) | sisi kubus |
| `--benar` | #2B8A3E | umpan balik benar (+ ikon ✓) |
| `--salah` | #C92A2A | umpan balik salah (+ ikon ✕) |

Semua pasangan teks/latar wajib kontras ≥ 4.5:1. Warna p/l/t selalu disertai hurufnya.

## 4. Tipografi
- Huruf sans-serif yang jelas (mis. *Nunito* atau *Inter*), ukuran dasar 18 px di HP.
- Angka di rumus memakai huruf tebal dan ukuran lebih besar (24 px).
- Simbol kali memakai "×", bukan "x" atau "*".

## 5. Tata Letak Layar Utama

### Beranda
```
┌──────────────────────────┐
│  RuangKu                 │
│                          │
│  ┌────────────────────┐  │
│  │  📘 Belajar        │  │  ← tombol besar, progres modul
│  │  Modul 3 dari 7    │  │
│  └────────────────────┘  │
│  ┌────────────────────┐  │
│  │  🧊 Lab 3D         │  │
│  └────────────────────┘  │
│  ┌────────────────────┐  │
│  │  🎯 Tantangan      │  │
│  └────────────────────┘  │
└──────────────────────────┘
```

### Layar Latihan Berpemandu (HP, potret)
```
┌──────────────────────────┐
│ ← Modul 4      ●●●○○ 3/5 │
├──────────────────────────┤
│   [ gambar balok 3D ]    │
│    t=3 (oranye)          │
│        l=4 (hijau)       │
│    p=8 (biru)            │
├──────────────────────────┤
│ Diketahui: p=8 l=4 t=3 ✓ │
│ Rumus    : V = p × l × t │
│ Substitusi: V = [ ]×[ ]×[ ]│  ← siswa isi
├──────────────────────────┤
│ [💡 Petunjuk]  [Cek ▶]   │
└──────────────────────────┘
```

### Alat Soal Cerita
```
┌──────────────────────────┐
│ Kotak pensil Rina        │
│ berbentuk balok.         │
│ Panjangnya [20 cm] ←sorot│
│ lebarnya [6 cm] ...      │
├──────────────────────────┤
│ Seret ke sini:           │
│  p: [20]  l: [  ]  t: [ ]│
└──────────────────────────┘
```

Layar lebar (tablet/proyektor): gambar di kiri, langkah di kanan.

## 6. Interaksi
- Target sentuh ≥ 48 × 48 dp; jarak antartombol ≥ 8 dp.
- Slider ukuran: rentang 1–20 satuan, bilangan bulat (desimal di fase berikutnya).
- Putar 3D: geser satu jari; reset sudut dengan tombol.
- Input angka memakai papan angka khusus (bukan keyboard penuh) agar tidak salah ketik.
- Animasi transisi ≤ 300 ms; hormati pengaturan *reduce motion*.

## 7. Bahasa & Nada
- Sapaan "kamu", kalimat aktif, positif.
- Umpan balik salah tidak menyalahkan: "Hampir! Cek lagi perkalian 8 × 4."
- Umpan balik benar singkat: "Benar! 96 cm³."

## 8. Daftar Periksa Sebelum Layar Dianggap Selesai
- [ ] Hanya ada satu tugas di layar ini.
- [ ] Label ukuran menempel pada gambar.
- [ ] Teks ≤ 3 kalimat.
- [ ] Ada tombol kembali/ulangi.
- [ ] Kontras lolos, nyaman di lebar 360 px.
- [ ] Tidak ada elemen dekoratif yang tidak berhubungan dengan materi.
