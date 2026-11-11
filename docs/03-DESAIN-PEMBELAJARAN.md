# 03 — Desain Pembelajaran (berbasis Cognitive Load Theory)

## 1. Tujuan Pembelajaran

Setelah menggunakan aplikasi, siswa dapat:

1. Menyebutkan unsur kubus dan balok (sisi, rusuk, titik sudut, panjang, lebar, tinggi).
2. Menjelaskan volume sebagai banyaknya kubus satuan yang mengisi bangun ruang.
3. Menghitung volume kubus (V = s × s × s = s³) dan balok (V = p × l × t).
4. Menyelesaikan soal cerita volume dengan langkah Diketahui–Ditanya–Rumus–Substitusi–Hitung–Simpulkan.
5. Menghitung volume sebagian (1/2, 2/3, 3/4) dari kubus/balok.
6. Memeriksa kewajaran jawaban (satuan, kecocokan data, perkiraan).

## 2. Prinsip CLT yang Dipakai

| Prinsip / efek | Apa artinya | Penerapan di aplikasi | Temuan |
|---|---|---|---|
| **Pretraining** | Kenalkan komponen sebelum prosedur | Modul 1: unsur bangun ruang sebelum rumus | T-20, T-06 |
| **Worked example** | Contoh lengkap lebih efektif dari soal langsung bagi pemula | Modul 3: contoh bertahap | T-12 |
| **Fading / completion** | Bantuan dikurangi bertahap | Modul 4: langkah kosong bertambah | T-05, T-18 |
| **Segmenting** | Pecah materi, kecepatan dikendalikan siswa | 1 langkah per layar, tombol *Lanjut* & *Ulangi* | T-12 |
| **Split-attention** | Jangan pisahkan gambar dan keterangannya | Ukuran ditulis langsung di rusuk gambar, bukan di legenda | T-10 |
| **Signaling** | Tandai informasi penting | Warna konsisten: p = biru, l = hijau, t = oranye | T-09 |
| **Redundancy** | Hindari info berulang/tidak perlu | Tanpa dekorasi, tanpa teks yang sama dengan narasi | T-21 |
| **Coherence** | Buang materi yang tidak relevan | Tidak ada latar bergambar / maskot di layar belajar | T-21 |
| **Modality** (opsional) | Gambar + suara lebih ringan dari gambar + teks panjang | Narasi suara opsional (F-22) | T-09 |
| **Expertise reversal** | Bantuan berlebih merugikan siswa mahir | Tes awal & bantuan adaptif | T-04 |
| **Self-explanation** (germane) | Menjelaskan memperkuat skema | "Jelaskan Kembali" setelah soal | T-17 |
| **Variability of practice** (germane) | Konteks bervariasi → transfer | Soal cerita dengan konteks beragam | T-18 |

## 3. Kode Warna Konsisten (signaling)

| Unsur | Warna | Dipakai di |
|---|---|---|
| Panjang (p) | Biru | rusuk 3D, angka di soal, rumus |
| Lebar (l) | Hijau | idem |
| Tinggi (t) | Oranye | idem |
| Sisi kubus (s) | Ungu | idem |
| Volume (V) | Abu gelap/tebal | hasil |

Warna yang sama muncul di gambar, teks soal, dan rumus sehingga siswa bisa "mengikuti" angka dari
soal ke rumus — langsung menyasar kesulitan substitusi (T-06).
*Catatan aksesibilitas:* warna selalu disertai huruf (p, l, t) agar tetap terbaca oleh siswa buta warna.

## 4. Struktur Modul

| No | Modul | Aktivitas utama | Jenis beban yang ditangani | Durasi |
|---|---|---|---|---|
| 0 | Tes Awal | 5 soal diagnostik | — (penentuan titik mulai) | 3 mnt |
| 1 | Unsur Kubus & Balok | Ketuk bagian bangun → nama muncul; jaring-jaring | Intrinsic (pretraining) | 5 mnt |
| 2 | Dari Kubus Satuan ke Rumus | Isi balok dengan kubus 1 cm³ lapis demi lapis; temukan pola p × l × t | Germane | 7 mnt |
| 3 | Contoh Soal Bertahap | 2 contoh (kubus, balok) satu langkah per layar | Extraneous ↓ | 5 mnt |
| 4 | Latihan Berpemandu | 6–8 soal, bantuan memudar | Intrinsic dikelola | 10 mnt |
| 5 | Soal Cerita | Sorot info → seret ke "Diketahui" → selesaikan | Extraneous ↓ | 10 mnt |
| 6 | Volume Sebagian | Simulasi air 1/2, 2/3, 3/4; hitung | Intrinsic (konsep baru) | 8 mnt |
| 7 | Latihan Akhir | 10 soal campuran + Jelaskan Kembali | Germane | 10 mnt |
| — | Tantangan | Mini-game (opsional, setelah modul 4) | Motivasi | bebas |

## 5. Pola Langkah Baku (skema penyelesaian)

Dipakai di semua soal agar menjadi kebiasaan (T-05, T-18):

```
1. Diketahui   : p = 8 cm, l = 4 cm, t = 3 cm
2. Ditanya     : Volume balok (V)
3. Rumus       : V = p × l × t
4. Substitusi  : V = 8 × 4 × 3
5. Hitung      : 8 × 4 = 32  →  32 × 3 = 96
6. Simpulkan   : Jadi, volume balok adalah 96 cm³
7. Cek ulang   : angka sesuai soal? satuan cm³? masuk akal?
```

## 6. Aturan Pemudaran Bantuan (fading)

| Level | Yang diisi aplikasi | Yang diisi siswa | Naik level bila |
|---|---|---|---|
| L1 | Langkah 1–4 | Langkah 5–6 | 2 benar berturut |
| L2 | Langkah 1–3 | Langkah 4–6 | 2 benar berturut |
| L3 | Langkah 1 | Langkah 2–6 | 2 benar berturut |
| L4 | — | Semua langkah | — |

Bila salah 2 kali berturut-turut → turun 1 level (bantuan bertambah).

## 7. Petunjuk Bertingkat (F-10)

Contoh untuk soal "Balok p = 8, l = 4, t = 3":

1. **Arahan:** "Coba lihat lagi rumus volume balok. Ukuran apa saja yang dibutuhkan?"
2. **Langkah spesifik:** "Ganti p dengan 8, l dengan 4, t dengan 3. Kalikan dua angka dulu."
3. **Contoh serupa:** tampilkan contoh terselesaikan dengan angka berbeda (mis. 5 × 2 × 3).

## 8. Diagnosis Kesalahan (F-11)

| Jenis kesalahan | Contoh jawaban | Umpan balik |
|---|---|---|
| Rumus luas, bukan volume | 2(pl + pt + lt) = 136 | "Itu luas permukaan. Volume = banyak kubus satuan di dalamnya." |
| Kubus: s × 3, bukan s³ | 6 × 3 = 18 | "s³ artinya s × s × s, bukan s × 3." |
| Salah substitusi | 8 × 4 × 4 | Sorot angka yang tidak sesuai soal dengan warnanya. |
| Salah kali | 8 × 4 × 3 = 86 | "Cek langkah perkalian: 8 × 4 = ? lalu × 3." |
| Salah/tanpa satuan | 96 cm² atau 96 | "Volume memakai satuan kubik (cm³)." |
| Volume sebagian terbalik | 1/3 × V padahal 2/3 | Tampilkan simulasi air pada pecahan yang ditulis siswa vs yang diminta. |

## 9. Pedoman Penulisan Soal Cerita

- Maksimal **3 kalimat**, tiap kalimat ≤ 15 kata (T-09).
- Satu kalimat = satu informasi ukuran.
- Pertanyaan selalu di kalimat terakhir, ditebalkan.
- Konteks dekat dengan siswa: kotak pensil, kotak hadiah, akuarium, bak mandi, kardus, lemari (T-01).
- Setiap soal cerita memiliki ilustrasi berlabel (T-10).
